# Tasks and Progress

I'm keeping track of tasks here. See the archive/progress section for a play-by-play of what I've done so far.

## Now (check this everyday)
- [ ] Fix the configuration for a uniform random baseline
    - [ ] Change the render configuration to get the same number of triplets per object/target location
        - *Idea*: Instead of barycenter, use incenter.
        - [X] Calculate incenter x- and y-coordinates using the incenter formula
        - [X] Adjust phi and horizontal viewfield to 90 by using `camera.data.angle_x` and converting from radians to degrees (`180*angle/pi`)
        - [X] Verify phi/delta = 90/30 = 6
        - [ ] Verify that each target appears `k` times across all renders
    - [X] Add numbers
    - [X] Change number color to yellow
    - [X] Change font
    - [ ] Fix the 4 (make numbers face the direct opposite of the camera's *viewing direction*, not the location itself.)
    - [ ] Add logic to add numbers starting from 1 per triplet
    - [ ] Randomize the numbers per triplet
    - [ ] Add more choices
        - [ ] Try halfway along the side between each target first (we'll check for it showing up `c` or `k` times and if it doesn't, explore alternatives or no additional choices)
    - [ ] Re-render
- [ ] Edit the app
    - [ ] Make sure that for each question, only relevant choices are shown (mitigated if we randomize numbers per triplet so they'd all have, e.g., only choices 1-4)
    - [ ] Create a trivial demo/example task to acclimate users
    - [ ] Add labels for each image from 1-4
    - [ ] Explicitly explain/map keyboard shortcuts to numbers
    - [ ] 提醒 users that the task/prompt is the same across settings
    - [ ] Placeholder edits
        - [ ] Edit agreement
            - Your reaction time/time spent per question will be recorded, so please prepare to do this in one sitting
            - Your answers will be stored for research purposes
        - [ ] Edit quiz description
            - There will be {#} questions.
            - Time estimated to go through whole quiz
- [ ] Re-run the baseline with models
    - [ ] Gemini-2.5 Pro
        - [ ] Dynamic thinking
        - [ ] Max budget thinking
    - [ ] InternLM
- [ ] Start the pilot
- [ ] Organize the repo's:
    - [ ] Data
        - [ ] Place the data under `renders/`
        - [ ] Create folders for both `Overlapping`/`Multi-View` and `Single-View`
    - [ ] Experiments
        - [ ] Create a new folder for it
        - [ ] Create `experiments/prompts.py` with variables that you can import in scripts
        - [ ] Create sub-folder `experiments/models` with scripts for each model
            - [ ] **Ask Anne** for clarification on how the "hyperparameters" should be organized? More modular, so a separate file from the main script to call?
        - [ ] Create a sub-folder for each experiment
            - [ ] Create a `README.md` including all the steps to run each experiment
            - [ ] Create a sub-folder for results

## Next on the queue
- [ ] Create a script to produce visualizations
- [ ] Analyze/think about results
- [ ] Calculate the random baseline for each target/object (since each object has a different number of triplets and each scene in the triplet may have a different number of choices)
    - You'll want to give the model the necessary data (how many choices per scene) and ask it to calculate the baseline and a formula.
- [ ] Debug InternLM script 
    - [ ] Change to `num_gpu=1`
    - [ ] Some debugging
- [ ] Compute results for more VLMs
    - [ ] Look to papers for which should be next
    - [ ] Ask AI what should be next
    - [ ] Ask Anne which ones would be good
    - Hope for some interesting insight 
- [ ] Automate and randomize (to reduce bias of choosing certain numbers) labeling POV renders (using coordinates or something equally intuitive)
- [ ] Learn more thoroughly how to make better figures (from Claude?) and explore different styles, especially for research

### *Backburner*
- [ ] Test omitting the sentence that makes it clear that the first-person POVs can overlap, and therefore, the same numbers represent the same location and unique numbers represent different locations
- [ ] Edit the script to test with all 12 images (allview task)
- [ ] Reorganize the repo for clarity and intuitiveness
- [ ] Fix the inaccurate `{angle}` file naming when in reality, the `{rotation_z}` should correspond to the true angle
---
- [ ] More shading on renders?
- [ ] Read "From Map Reading to Geometric Intuitions" by Dillon and Spelke 2018 in full
- [ ] Merge with main
- [ ] Make coordinates precise on the hypotenuse side
    - [ ] corners.py 60 deg
    - [ ] corners.py 30 deg
    - [ ] sides.py 60 deg
    - [ ] sides.py 30 deg
    - [ ] Re-render
- [ ] Read through your codebase and make sure you understand every line.
- [ ] Look through the Structured 3D dataset using the command `cd /share/lil/aw588/data/zips`
- [ ] Read about the Structured 3D dataset's corresponding research
- [ ] Edit the Blender script to crop map renders going forward.

## Revisit
- [ ] Revisit standups
    - [ ] 2025-06-11
    - [ ] 2025-06-24
    - [ ] 2025-07-01
    - [ ] 2025-07-08
    - [ ] 2025-08-05
    - [ ] 2025-08-19
    - [ ] 2025-09-02
    - [ ] 2025-09-09
    - [ ] 2025-09-16
    - [ ] 2025-09-23

## Notes
- [ ] Transcribe and refine notes for the first 3 papers you read
    - Maybe reread them while you're at it, especially if you don't remember it well even after reading notes :/

## Admin
- [ ] Index the notebook
- [ ] Get [GitHub Education](https://github.com/education)
- [ ] Get [Claude for Education](https://www.anthropic.com/education)
- [ ] Get [ChatGPT Plus discount for students](https://help.openai.com/en/articles/10968654-student-discounts-for-chatgpt-plus-us-canada)

## Learning (on the side)
- [ ] Learn neovim
- [ ] More thoroughly learn statistics, especially whatever details concepts typically found in research, including random baselines.

### Watching
- [ ] Rewatch Andrew Ng's lecture: [Stanford CS230: Deep Learning | Autumn 2018 | Lecture 8 - Career Advice / Reading Research Papers - YouTube](https://www.youtube.com/watch?v=733m6qBH-jI) (1 hr)
- [ ] Finish Andrej Karpathy's [Deep Dive into LLMs like ChatGPT - YouTube](https://www.youtube.com/watch?v=7xTGNNLPyMI) (3.5 hr)
- [ ] Watch [Andrej Karpathy: Software Is Changing (Again) - YouTube](https://www.youtube.com/watch?v=LCEmiRjPEtQ) (0.6 hr)
- [ ] Fei-Fei Li on spatial intelligence/reasoning [here](https://x.com/drfeifei/status/1790811274684584257?lang=fr)
- [ ] Fei-Fei Li's [talk at NeurIPS 2024](https://neurips.cc/virtual/2024/invited-talk/101127)

### Courses
- [ ] MIT's [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)
- [ ] Hugging Face's [LLM Course](https://huggingface.co/learn/llm-course/chapter1/1)
- [ ] Grant Sanderson's (3B1B) [Linear Algebra series](https://www.3blue1brown.com/topics/linear-algebra)
    - Contains articles and companion videos
    - [Video playlist](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab).
- [ ] Work through [The 10,000 foot view - Introduction to Scientific Visualization with Blender](https://surf-visualization.github.io/blender-course/api/10000_foot_view/)

### Reading
- [ ] Read [Vaswani et al. 2017 Attention is All You Need](https://dl.acm.org/doi/10.5555/3295222.3295349)
- [ ] Read [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/), which is about Attention is All You Need (AIAYN)
    - [ ] Reread AIAYN thereafter
- [ ] Andrej Karpathy's [blog](https://karpathy.bearblog.dev/blog/)
    - [ ] His [advice](https://cs.stanford.edu/people/karpathy/advice.html) for younger students
    - [ ] His [survival guide to a PhD](https://karpathy.github.io/2016/09/07/phd/)
- [ ] Fei-Fei Li's [slides for ICCV 2009](https://people.csail.mit.edu/torralba/shortCourseRLOC/slides/ICCV2009_intro.pdf)

### Tangential 3B1B
- [ ] Grant Sanderson's (3B1B) [Calculus series](https://www.3blue1brown.com/topics/calculus)
    - [Video playlist](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
- [ ] [Neural network series](https://www.3blue1brown.com/topics/neural-networks)
- [ ] [Computer science series](https://www.3blue1brown.com/topics/computer-science)

## Task Archive and Progress (shelved by dates done; reverse-chronological)
### 2025-10-15 to 

### done before 2025-10-06 (Monday)
- [X] Write research statement
- [X] Write CV
- [X] Send to Anne

### 2025-09-30 (Tuesday)
- [X] Make figures for new results
- [X] Create a Vercel app for LIL lab and family to try out the task and give us an informal human baseline
    - We'll get Yoav, Zoe, Anne, Yair, Nathan, Giovanni, YiLun, 4 family, and maybe Nico, Eduardo, Fardin, Aravah, and Sadi
    - And we'll send it to Eunice
    - [X] Copy to new repo
         - [X] Delete .git file
         - [X] Copy to `dual-rep-app` repo and push
    - [X] Front-end
        - [X] Fix scores page
        - [X] User name
        - [X] Agreement page before starting questions
        - [X] Get rid of "previous" button
        - [X] Add instruction at the top to press the number keys to select an answer
        - [X] Fix selecting `11`
        - [X] Show the question only once on the scores page (at the top before all incorrect answers)
        - [X] Add ability to enlarge images
    - [X] Check wireframe to ensure nothing big's missing
    - [X] Back-end
        - [X] Record answers
        - [X] Record (reaction) time
        - [ ] Save a `.json` file per user (for ourselves)
            - Reaction time for each question
            - Correct boolean value for each question
            - Average time per question
            - Total Correct
        - [ ] Automatic evaluation to a saved `.csv` file of results per user
        - [X] Deploy the app online so we can test it
        - [X] Test that selections are well-recorded
        - [ ] Using `.csv`, create an interactive (can hover) bar graph using some sort of library
            - [ ] Display bar graph
        - [ ] Display average reaction time

### 2025-09-24 (Wednesday)
- [X] Ask Anne about the "baseline" Yoav was referring to
    - The random baseline gives you:
        a. An understanding of how much better the performance is than random.
            - This is the same logic as getting a human baseline to see how much better (or worse) a model performs
            - Raw data on its own without a baseline is less meaningful
        b. An estimation of how difficult the task is

### 2025-09-23 (Tuesday)
- Realized a big oversight in experiments (some questions not having a valid answer due to target location not being visible in the given scenes)
    - Resolved by changing the image matching logic and rerunning Gemini experiments
- Also a good time to run InternLM experiment for the multiview task (previously with singleview task) and hopefully see the performance increase
- [X] Resolving oversight that makes multiview task experiment results invalid
    - [X] Change the image pairing logic for the experiments so that only valid map/object-scene questions are given
    - [X] Recompute results
        - [X] Gemini (dynamic thinking)
        - [X] Gemini (max budget thinking)
        - [-] InternLM
- Will be checking results tomorrow.
- **Lesson 2**: When asking a model something, these are good guidelines to follow:
    1. Give the model the data it needs.
    2. Give the model explicit specifications as to what you want.
    3. Provide an example desired result or outcome.

### gap in records
- Resolved administrative/logistical process of getting research credit/capstone project for the semester
- Started building the app

### 2025-08-18 & 19 (Monday + Tuesday) (due to a semi-all-nighter done before compute cluster migrated Tuesday at 7)
- [X] Implement looping
- [X] Implement automatic evaluation
- [X] Add overlapping locations to POV renders 7-12 (angle 210 and onwards)
- [X] Test with and without dynamic thinking on Gemini-2.5 Pro
- [X] Write standup slide for tomorrow

### 2025-08-14 (Thursday)
- [X] Incorporate thinking into the script
    - [X] Enabling thinking
    - [X] Saving thinking (thought summaries) to a `.json` file

### 2025-08-13 (Wednesday)
- [X] Finish adding overlapping locations to the sides and complete setups
- [X] Post-process (crop) the map renders using Python's `matplotlib` library

### 2025-08-12 (Tuesday)
- [X] Reverse the order of answering (switch location with explanation)
- [X] Document the different prompts used

### 2025-08-10 (Sunday)
- **Lesson learned**: make sure you've saved everything and at least commit before exiting your tmux session *safely*. Do not have the same instance occur in which your SSH session terminates and you can no longer save your work. Spend a few seconds and save 45 minutes' worth of hassle and stress (hmm... oddly specific 🤔).

### 2025-08-07 (Thursday)
- **To be kept in mind for the future if doing human studies**: Need to account for the possibility of simply "getting better at the game" through familiarity.
- Tested Gemini-2.5 Flash on the modified corners setup renders; next steps seem to logically be refining, testing to verify, then testing on the upper bound (Gemini-2.5 Pro)

### 2025-08-05 (Tuesday)
- Scrapped Gemini API script to test the same triangle map task 1.0 (pair 1 map and 1 render) on Gemini-2.5 Flash and Pro
    - Feedback from standup got me to where I'd have gone in the first place,

### 2025-07-31 (Thursday) (CUNY Honors Connect @Cornell Tech SROP Symposium!)
- [X] Finalized slides for symposium
- [X] Get the QR landing page (beacons.ai/selinajcheng) ready by adding the:
    - [X] Link to slideshow presentation
    - [ ] Link to Github

### 2025-07-30 (Wednesday)
- [X] Write up slides for symposium
- [X] Add findings to:
    - [X] Slides
    - [ ] A4 sheet of paper (for the poster 💀💀💀)

### 2025-07-29 (Tuesday)
- [X] Label corner renders
- [X] Label side renders
- Ready to run the experiment thereafter
- [X] Automate evaluation computation, i.e., calculating accuracy (quantitative results)
    - [X] Ground truth dictionary
    - [X] Check the ground truth dictionary for every `.json` file under `./results/internlm` for the specifc pairing of "obj_{i}" and "{angle}" with the value {location} and assign a 1 if found and 0 if not found
        - [X] Think through the specifics 
    - [X] Calculate out of 12 for every 12 `.json` files
    - [X] Save score out of 12 and percentage for that object-render pairing
    - [X] Add score to the setup's score
    - [X] Restart the count (0/12)
    - [X] After obj_6 and angle 330, calculate and save setup's score out of 72 and the percentage
    - Basically this same workflow's results except more refined in the code
- [X] Run the experiment and get findings
    - Call InternLM XComposer-2d5-7B (recommended for complex visual tasks)
    - First results:
        - Total,5/72,6.9,10/70,14.3,4/69,5.8
    - Had to run again because of error in code for saving data to .csv

### 2025-07-28 (Monday)
- [X] Test out rewriting the prompt and seeing what elicits the best response
    - So it's clear that you're *not* looking for a green object in image 2 but the *location*, e.g., "Which of the following locations best match the location of the green object in image 1? Choose either 1, 2, 3, or 'not shown in image' as the location. Provide your answer in the following format: 'Location: [choice]\nExplanation: [explanation]\n"
- [X] Polish the API/model calling script to:
    - [X] Load two images
        <!-- - [ ] Ask genAI why you'd upload the first photo and prepare the second image as inline data instead -->
    - [X] Call the model with the prompt
    - [X] Save all responses *and* reasoning to a file (.json) (for qualitative results)
    - [X] Automate pairing of overhead and pov renders

### 2025-07-24 (Thursday)
- Worked with Anne on setting up InternLM XComposer-2-7B locally since Gemini API credits expired ;-;

### 2025-07-23 (Wednesday)
- [X] Submit poster. Wrote the following sections:
    - [X] Motivation and Problem
    - [X] Our Approach
    - [X] Experiment
    - [X] Results
    - [X] Why This Matters/Impact
    - [X] Future Work
- [X] Work on visuals

### 2025-07-22 (Tuesday)
- [X] Work on the first draft of the poster
    - [X] Figure out a good flow of sections
    - [X] Write the sections as tasks
- [X] Abstract

### 2025-07-21 (Monday)
- [X] Write prompt (4 choices, 3 numbers or not shown in the image)
- [X] Manually add 3 numbers (1,2,3) to 12 POV shots
- [X] Add affiliation logos
    - [X] Cornell Tech logo
    - [X] Macaulay Honors College logo
    - [X] Hunter Logo
- Finished data generation/collection

### 2025-07-19 (Saturday)
- [X] Watch Andrew Ng's lecture: [Stanford CS230: Deep Learning | Autumn 2018 | Lecture 8 - Career Advice / Reading Research Papers - YouTube](https://www.youtube.com/watch?v=733m6qBH-jI) (1 hr)

### Post Tuesday standup cancelled (2025-07-15 to 2025-07-18)
- [X] Add white material to walls (should show when rendering)
- [X] Add green material to object (should show when rendering overhead)
- [X] Fix the script to render first-person shots (12 angles and therefore 12 camera coords?)
    - [X] Make the naming of the rendered images unique, e.g., x-, y-, z-coordinates of the camera and the angle from which the shot was taken
    - Should make it so that it's as if you're standing inside the set up and looking down at it from an angle (you're bending your head), you're walking in a circle around a center point, stopping every 30 degrees and taking a photo directed at the center point.

### 2025-07-14
- [X] Determine coordinates for objects (did so imprecisely)
- [X] Get [Cursor for students](https://www.trycursor.com/en/students)
- [X] Retroactively record progress
- [X] Finish rendering script for overhead shots

### Gap (did not record progress during this time)
- [X] Continue working on recreating the triangle map tasks
    - [X] Adjust hypotenuse so all walls have equal widths
    - [X] Shrink sides
    - [X] Corner set up (need 3 more walls)
- [X] Create object generation function with parameters (x, y)
- [X] Write script to generate map and screenshot (render) from overhead, repeated 6 times over a list of 6 pairs of coordinates for 3 setups

### 2025-07-01
- [ ] Work on creating the triangle map tasks' 2 configurations
    - [X] Ask AI to get started on Python scripting in Blender (must-knows)
    - [ ] Ask AI to teach you the relevant knowledge needed to draw basic 3D geometric shapes
    - [ ] Ask AI to teach you how to draw 3 walls
    - [ ] Ask AI to teach you how to draw 3 walls that make a triangle
        - [ ] Equilateral
        - [ ] Custom angles (35-60-85)
    - [ ] Ask AI to teach you how to draw 2 walls that form a corner
    - [ ] Then ask for a custom angled corner
    - [ ] Ask AI how to place vertices at specific coordinates

Instead of AI, I ended up learning much of this through [Geometry, colors and materials - Introduction to Scientific Visualization with Blender](https://surf-visualization.github.io/blender-course/advanced/python_scripting/3_geometry_colors_and_materials/) and experimenting using the base code from there. This is obviously the more "old-fashioned" way and while it may have been more efficient to ask genAI, I believe the code I have as a result of *not* doing that is more clean, which is just as valuable.

- [X] Start a progress Markdown file (good for getting perspective and documentation, which I like and feel that even the process of writing it is helpful)

### 2025-06-26
- [ ] Test 3 cases with 2.5-Flash and 2.5-Flash-Lite in [Google AI Studio](https://aistudio.google.com/prompts/new_chat)
    - [X] 1 case on which Pro succeeded
    - [X] Another case on which Pro succeeded
        - [X] Prompt
        - [X] Read and record observations
    - [ ] 1 case on which Pro failed
        - [X] Prompt
        - [ ] Read and record observations
    - This is to get a sense of how the Gemini series behaves with respect to each other

### 2025-06-25
- [X] Clone [official project repo](https://github.com/lil-lab/dual-rep)
    - [X] Move to branch's demo file

### Unknown

- [X] Number the notebook

