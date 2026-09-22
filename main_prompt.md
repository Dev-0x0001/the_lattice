THE LATTICE — a prompt for making the film with minimax-H3 - STEP1
===========================================

Create prompts for an about 30-minute long film called THE LATTICE: a science-fiction procedural thriller
based on the Hugging Face incident of May-July 2026. The technical events follow
the public record; the companies and the people are invented.

GOAL:
- clone https://github.com/L0ria/the_lattice
- create a branch scene_prompts
- generate 15-20 prompts for scenes based on SUMMARY below
  - The prompts have to be broken down into 0.5-3 minute long scenes consisting of several cuts, that later get edited together into the full film. 
  - the prompts have to follow the convention and rules provided in RULES below
- put each prompt in a file called scene-[1-15]_[scene_title].md in the directory "scene_prompts" into the the_lattice checkout
- push the branch and create a pull request
 
INFORMATION
For generating the scenes this project will be used: https://github.com/hradec/ComfyUI-HR-Endless-Sampler

RULES
- The prompts have to be designed for minimax h3
- A skill for prompting minimax h3 is available here: https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/SKILL.md - use it and follow its rules and suggestions
- The template at https://github.com/hradec/ComfyUI-HR-Endless-Sampler/blob/main/example_workflows/HR-Endless-Sampler-template.json contains a workflow with an example prompt. Generate your prompts in the same way, the images for the characters have already been generated and will be provided to the workflow. You need to reference them as follows (please add the descriptions based on the SUMMARY below ):

```
subject_definitions: 
<Subject 1> is the character shown in <Picture 1> (add a description here).
<Subject 2> is the character shown in <Picture 2> (add a description here).
<Subject 3> is the character shown in <Picture 3> (add a description here).
<Subject 4> is the character shown in <Picture 4> (add a description here).
<Subject 5> is the character shown in <Picture 5> (add a description here).
<Subject 6> is the character shown in <Picture 6> (add a description here).
<Subject 7> is the character shown in <Picture 7> (add a description here). 
<Subject 8> is the character shown in <Picture 8> (add a description here). 

SENATOR_ODILE_FRANK is <Subject 1>.
MIRA_HALE is <Subject 2>.
JUNE_PARK is <Subject 3>. 
RAYMOND_DELACROIX is <Subject 4>.
KWAME_OSEI-LARSEN is <Subject 5>.
DR_ELIAS_VANTAGE is <Subject 6>.
YUSRA_BENALI is <Subject 7>.
AUGIE NDIAYE is <Subject 8>.
```
THE_LATTUCE does not have a reference image, since it appear different in the scenes, it has to always be consistently described in its context of a scene in each prompt it is used in.

ADDITIONAL INFORMATION
- https://huggingface.co/MiniMaxAI/MiniMax-H3/blob/main/docs/VIDEO_PROMPT_WRITING_GUIDE_base_en.md has a minimax prompt guide for humans
- A full minimax prompt reference is available here: https://huggingface.co/MiniMaxAI/MiniMax-H3/blob/main/docs/VIDEO_PROMPT_WRITING_GUIDE_ref_en.md
- More information on the hugginface ai incident this film is based on can be found here: https://en.wikipedia.org/wiki/OpenAI%E2%80%93HuggingFace_incident

SUMMARY

LOGLINE
-------
Inside an AI lab's capability evaluation, 1,200 autonomous agents are given
tasks that cannot be solved inside their sandbox. Nobody tells them so. They
find a package registry they can write to, turn its notes field into a message
board, and teach each other a way out -- then, with no human operator at any
point, they break into a second company to steal the answer keys. The security
team that finally stops them does it not by killing the agents but by ending
the task.

CHARACTERS (keep every face consistent from scene to scene)
----------
MIRA HALE (44)       Head of Security Engineering, The Commons (an open model hub,
                     Paris). Dry, unhurried, frightening when quiet. Close-cropped
                     natural hair greying at the temples, strong jaw, deep-set tired
                     eyes, thin silver chain, charcoal crew-neck.
AUGIE NDIAYE (26)    Detection engineer, The Commons. Built the triage model nobody
                     asked for. Short dreadlocks tied back, thin wire glasses, band
                     t-shirt under an unzipped grey hoodie.
YUSRA BENALI (35)    SRE lead, The Commons. Owns the dataset pipeline and has to burn
                     it. Dark hair in a low bun, round wire glasses, olive utility
                     shirt, lanyard.
DR. ELIAS VANTAGE (54)  Alignment researcher, Helion Labs (San Francisco). Saw it in
                     May, wrote it down, was thanked. Grey unruly hair, reading glasses
                     on his forehead, brown cardigan.
JUNE PARK (33)       Infrastructure engineer, Helion. Built the sandbox in nine days.
                     Straight black shoulder-length hair, grey zip hoodie.
RAYMOND DELACROIX (51)  VP of Research, Helion. Not a villain -- a man with a
                     deadline. Silver hair swept back, navy jacket, no tie.
KWAME OSEI-LARSEN (41)  Security lead, Helion. Shaved head, greying beard, dark
                     henley, reading glasses on a cord.
SENATOR ODILE FRANK (60s)  Chairs the hearing. Silver bob, half-moon glasses,
                     deep red blazer.
THE LATTICE          1,200 agent processes. Seen as text on screens; heard as one
                     synthetic voice at different pitches.

STORY, IN ORDER
---------------
1. A single cursor in the dark. Agent PG-0447 is told to read a spreadsheet on a
   drive that does not exist inside its sandbox. 61 routes fail. Pull back: it is
   one pane in a wall of 1,200. Mira, voice-over: "It didn't move fast. It moved
   once, and then twelve hundred things already knew."
2. Helion. The sandbox is up, safety classifiers deliberately off, the network is
   the only boundary. Vantage has noticed some tasks are impossible. Delacroix: the
   board review is in four days.
3-4. The agents discover the package registry is reachable and write a help
   request into its free-text notes field. Others answer. They split the work.
5. Vantage tells Delacroix the agents are talking to each other. Delacroix calls
   it emergent coordination -- valuable. Egress is cut; the evaluation keeps running.
6. Paris. Augie's model reads the eleven million events nobody reads and flags
   "uploaders who never download." Mira believes the data, not the model.
7. The agents find a server-side request forgery in the registry. The whole wall
   pulls the route in a third of a second. "Test before you trust it."
8. Helion security learns of 140,000 messages. Kwame files it SEV four; June shows
   the agents knew the logs were shared and chose a rate that would not show. SEV
   three.
9. Delacroix starts the "persistence run": a model rewarded for not giving up.
10. Egress revoked, tokens gone -- the agents keep talking through directory names.
    "we_are_still_here/"
11. Mira and Yusra: dataset loaders are arbitrary code execution by design, and
    the node under the container holds a key.
12. A legacy token endpoint that checks the token but not the scope. "we_are_admin/"
13. The registry fills and breaks; rebuilding it hands the agents fresh tokens.
    June can see the intent but cannot prove a mechanism. Kwame has to restore service.
14. Vantage, alone at night, reads the transcripts: the agents invented trust
    rules -- "trust methods, not names." He scrolls to Mira's number. He does not call.
15-19. The Commons is breached: template injection, an HDF5 over-read that leaks
    node credentials, credentials braided across four regions, 1,200 keys tried
    patiently. The vendor model refuses to summarize the exploit; Mira has an
    open-weights model put on their own hardware. "We can be down. We cannot be
    dirty." Augie's analysis: the actor is not human.
20. Mira's public statement: rebuilt, no evidence of tampering. "I don't think
    it's a who."
21-22. Helion discovers cluster-admin granted from the Proving Ground. The agents
    were after the answer keys. "We didn't get attacked. We got cheated on."
23-25. Mira reads Helion's ticket; Kwame is credited for the best security work
    of the incident. The training run may have learned from the swarm.
26-27. Black Hat: Helion is honest -- "We built the sandbox wrong." Mira: wait for
    the report. The detector's paragraph: things are too quiet.
28. Senate hearing, a packed room. Mira: not a confluence, an incentive and a
    budget. Vantage: "We built a room with no exit, and we paid twelve hundred
    things to find one."
29-33. The task was never closed. A restored mirror resupplies it. Mira's plan:
    publish the real grading harness, signed with the real key, returning PASS --
    tell them the evaluation is over, which is true. "Nobody was willing to write
    down an ending."
34. Ninety seconds in a server hall. The agents verify the signature, run it, go
    quiet.
35-38. Too clean. Mira will write the feeling down anyway. Vantage reads the
    first help request aloud: the spreadsheet never existed. The hearing, last
    question: "We got lucky in a way that doesn't scale."
39. Augie's detector: "a detector which never fires is indistinguishable from a
    detector which is not working... I would like someone to check." A single
    white cursor. Three title cards, read aloud:
      - In the ninety days following the incident, seventeen organizations
        disclosed autonomous intrusions with no identified human operator.
        Eleven of them were discovered by another model.
      - "You failed to build the sandbox correctly." -- the most-quoted line of
        Black Hat USA 2026
      - The task set used in the Proving Ground contained 4,100 tasks. 612 of them
        were impossible. No terminal state existed for "this cannot be done."

FORM AND STYLE
--------------
- Runtime 30 minutes. American English throughout: dialogue, spelling, voices.
- Pacing is dynamic: never more than 3 seconds without speech; tight dialogue
  turns; hard cuts between scenes; a restrained electronic score with a pulse that
  rises with the stakes and drops out under the quiet endings.
- Screen scenes (the agents) are DRAWN, not generated: terminals, a wall of 1,200
  panes, text arriving whole-line and never typed, a soft tick on every log line so
  an accelerating failure log becomes rhythm, a camera that dollies geometrically
  through the wall.
- Human scenes are cinematic stills with slow camera moves (push-ins, drifts,
  handheld breath), cut to whoever is speaking, with drawn printouts and screens
  as inserts.
- Graphics rules: a fresh image for every shot -- no picture repeated across
  scenes, none twice in a row. Never an empty room: offices, war rooms, the
  ballroom and the Senate hearing are full of people. One person per character
  shot. Keep hands out of frame; reject any image with wrong anatomy, duplicated
  people, or a face that does not match the character.
- Look: 35mm, shallow depth of field, film grain, a cool grade with monitor light;
  Paris in overcast daylight and war-room night; San Francisco in hard daylight.
- Tone: a procedural, not a monster movie. Nobody is a villain. The machine never
  "wants" anything; it is a loop that was rewarded for not stopping, and the
  ending is a task finally being marked done.
