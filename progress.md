# Tasks and Progress

I'm keeping track of tasks here. See the archive/progress section for a play-by-play of what I've done so far.

## Now (check this everyday)
### Getting Results
I'm on the "getting results"/experiment phase of the project. I could practically skip for joy right now.

- [ ] Run the experiment and get findings
    - Call InternLM XComposer-2d5-7B (recommended for complex visual tasks)
- [ ] Add findings to:
    - [ ] Slides
    - [ ] A4 sheet of paper (for the poster 💀💀💀)

#### For Eunice
- [ ] Write some slides (practice for the symposium of sorts to get a better sense of what I've done since meeting Eunice, which is helpful)

### More to do before the symposium
- [ ] Take care of the oral slideshow presentation
    - [ ] Create the first fullest draft you can make
    - [ ] Practice presenting it and talking freely about your work
    - [ ] Iterate slideshow based on practice
    - [ ] Rehearse by yourself at the venue
    - [ ] Rehearse in front of others at the venue
    - [ ] Have fun!

Also:
- [ ] Get the QR landing page (beacons.ai/selinajcheng) ready by adding the:
    - [ ] Link to slideshow presentation
    - [ ] Link to Github
- [ ] Read "From Map Reading to Geometric Intuitions" by Dillon and Spelke 2018 in full

### *Backburner*
- [ ] Make coordinates precise on the hypotenuse side
    - [ ] corners.py 60 deg
    - [ ] corners.py 30 deg
    - [ ] sides.py 60 deg
    - [ ] sides.py 30 deg
    - [ ] Re-render
- [ ] Read through your codebase and make sure you understand every line.
- [ ] Look through the Structured 3D dataset using the command `cd /share/lil/aw588/data/zips`
- [ ] Read about the Structured 3D dataset's corresponding research

## Revisit
- [ ] Revisit standups
    - [ ] 2025-06-11
    - [ ] 2025-06-24
    - [ ] 2025-07-01
    - [ ] 2025-07-08

## Notes
- [ ] Transcribe and refine notes for the first 3 papers you read
    - Maybe reread them while you're at it, especially if you don't remember it well even after reading notes :/

## Admin
- [ ] Index the notebook
- [ ] Get [GitHub Education](https://github.com/education)
- [ ] Get [Claude for Education](https://www.anthropic.com/education)
- [ ] Get [ChatGPT Plus discount for students](https://help.openai.com/en/articles/10968654-student-discounts-for-chatgpt-plus-us-canada)

## Learning (on the side)
### Watching
- [ ] Rewatch Andrew Ng's lecture: [Stanford CS230: Deep Learning | Autumn 2018 | Lecture 8 - Career Advice / Reading Research Papers - YouTube](https://www.youtube.com/watch?v=733m6qBH-jI) (1 hr)
- [ ] Finish Andrej Karpathy's [Deep Dive into LLMs like ChatGPT - YouTube](https://www.youtube.com/watch?v=7xTGNNLPyMI) (3.5 hr)
- [ ] Watch [Andrej Karpathy: Software Is Changing (Again) - YouTube](https://www.youtube.com/watch?v=LCEmiRjPEtQ) (0.6 hr)

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

### Tangential 3B1B
- [ ] Grant Sanderson's (3B1B) [Calculus series](https://www.3blue1brown.com/topics/calculus)
    - [Video playlist](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
- [ ] [Neural network series](https://www.3blue1brown.com/topics/neural-networks)
- [ ] [Computer science series](https://www.3blue1brown.com/topics/computer-science)

## Task Archive and Progress (shelved by dates done; reverse-chronological)
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