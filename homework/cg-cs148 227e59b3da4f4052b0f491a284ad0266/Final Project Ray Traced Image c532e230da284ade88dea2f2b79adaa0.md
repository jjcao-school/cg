# Final Project: Ray Traced Image

CS 148 Fall 2020-2021

Final images from previous CS148 offerings:

![Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2014_10-1.jpg](Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2014_10-1.jpg)

Marianna Neubauer and Yixin Wang, 2014

![Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2017_10-1.jpg](Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2017_10-1.jpg)

Christopher Sauer and Kevin Rakestraw, 2017

![Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2015_10-1.jpg](Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2015_10-1.jpg)

Peter Do Ha and Brennan Preston Shacklett, 2015

![Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2018_10-1.jpg](Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2018_10-1.jpg)

Fang-Yu Lin, 2018

![Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2016_10-1.jpg](Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2016_10-1.jpg)

Shyamal Buch and Wilbur Yang, 2016

![Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2019_10-1.jpg](Final%20Project%20Ray%20Traced%20Image%20c532e230da284ade88dea2f2b79adaa0/2019_10-1.jpg)

Kevin Chen, 2019

Larger versions of these images (and others) can be found under [the `Showcase' link](http://web.stanford.edu/class/cs148/showcase.html) on the course webpage.

These were images created within the ray tracer framework provided in previous years. We are adopting a new framework (Blender) and using a different set of requirements this fall, so expect this year's image to have a different look.

# Introduction

The final project is an image that you create using **your SimpleRT renderer** OR **Blender's Cycles**. You must put together a coherent scene using geometry, material, and texture that you made and/or found online. 

Since you will be graded primarily on artistic merit, we recommend you spend a lot of time asking for feedback from the CAs, Ron, friends, family, etc. You can come to office hours often to get feedback on your project as you develop it. We will give candid feedback to help improve your project grade. We want everyone to succeed and are here to help!

# (Optional) Project Proposal

Find a motivational image (or a couple), and write a short paragraph explaining the goals for your project as motivated by the image(s). Work with your partner, the CAs, etc. on this proposal, and make sure that you and your partner agree.

This proposal can be handed in at any point **in the first 7 weeks** (due 11/2 11:59 pm PT) of the course and can be iterated on or modified as the course proceeds. No late days are allowed.

The proposal will be graded on a 0-5 scale, similar to the HW assignments, and
those points will count as **extra credit** towards your HW assignment grade (which is
clamped at 5 times the total HWs, i.e. 40 points max).

# Requirements

### Common requirement

- **One Geometry from scratch:** At least 1 piece modeled/simulated/sculpted from scratch.
- **Cite your Source**: You are welcome to use any assets or blender addons you find online, provided you cite the link in your writeup.

### SimpleRT-specific requirement

- **Submit a Project proposal:** Since this option is harder from a technical perspective, you are required to submit a project proposal clearly stating that you will be using SimpleRT for your final image. CAs will evaluate the feasibility and provide suggestions.

### Blender Cycles-specific requirements

- **Main Geometry from scratch:** at least half of the main objects in your scene needs to be modeled/simulated/sculpted from scratch.
- **UV mapping and Texturing from scratch:** for at least one of the objects made from scratch in your scene, you must 1. UV unwrap the object yourself and 2. create a texture from scratch either via hand-painting or procedural generation.
- **Create a custom/procedural material:** make at least one material with OSL script nodes, or non-shader nodes (i.e. texture, color, vector, converter nodes. See the list of nodes [here](https://docs.blender.org/manual/en/latest/render/shader_nodes/index.html)).
- **Blender/Cycles feature:** Use at least one advanced feature in Cycles or Blender (e.g. depth of field, motion blur, denoising, post-processing).

You will be moved to a lower grading bucket for each of the requirement you fail to meet.

# Submission

All online submissions will be done via Google forms/Google drive which you should have access to with your Stanford account. If for some reason this is not an option for you, please make a private Piazza post ASAP.

**We will provide a link on Piazza for submission** of the electronic copy of your write-up and image nearing Thanksgiving break. You are welcome to submit multiple times; however, your latest submission before the final electronic submission deadline will be the one used for grading.

### Deliverables

To grade your final ray-traced image, we will require:

The filename should be the SUNet ID(s) of everyone in your group concatenated by underscores (e.g. `rfedkiw_kevli016.xxx`).

1. Final writeup detailing what you did (electronic copy): `student1_student2.pdf`. You must clearly state:
    - What each person in your group did
    - What assets you got online, what assets you made yourself
    - How you met the project requirements
    - Document/video you referenced
    - Technical contributions

    Please use a plain-text file format, a Microsoft Word document (`.doc` or `.docx`), or a PDF file (`.pdf`). 

2. An electronic copy of your image: `student1_student2.png`. The resolution should be at least 1000 pixels along the short edge.
3. Variant A of your image: `student1_student2_a.png`. Render your image from a different camera view.
4. Variant B of your image: `student1_student2_b.png`. Render your image from the original camera view and the same exact lighting conditions but with no textures (use a gray, pure diffuse BRDF, gray in RGB being: (0.5, 0.5, 0.5)). 
5. Source Blender File: `student1_student2.blend`. Pack all the data into the blender file (File ‣ External Data ‣ Pack All Into .blend) and upload that file. If you have some assets that are too big for upload (e.g. high-res geometry or texture), you can leave them out. Be sure to keep all the code/assets that you manually created, since they will be checked against the list of requirements.

Variant A and Variant B of your image can be rendered without any effects (e.g. global illumination) and with only one sample per pixel (and per light if relevant).
Additionally, Variant A and Variant B can be rendered at a lower resolution. At a minimum, Variant A and Variant B should have a short edge of 480 pixels. However, be sure to maintain the aspect ratio of your final image.

### Important Dates

By the academic calendar, there is no finals week this year, and grades are due on 12/8. In order for us to have adequate time to grade your projects, we need electronic submissions by these dates:

- 11/10, 11/12: CA led classes where we will discuss past images and their strengths and weaknesses as viewed by the CA.
- 12/2 (11:59 pm PT): Initial electronic submission due.
- 12/3 (11:59 pm PT): Last opportunity to submit a higher quality image. Final electronic submission due.

In other words, you will submit a version of your final image on 12/2, but from that point, you can also spend one more day re-rendering the same scene with higher sampling rates and image resolution to get a higher quality final image.

Your image must not change aside from sample count and resolution between the image submitted on 12/2 and the one on 12/3.

You are free to work beyond these deadlines and take an incomplete if you need more time.

# Grading

Your image will be graded primarily on artistic merit.

Since SimpleRT and Cycles are two tracks with different focuses, we will grade them **separately**.

For each track, the images will be separated into 10 ``buckets'' where each bucket represents images of around the same quality. Images in bucket 1 are of the poorest quality while images in bucket 10 are of the highest quality. Within each bucket, each image will be ranked. For example, an image that is bucket 10 rank 5 was deemed to be of lower quality than an image that is bucket 10 rank 2. However, both would be of higher quality than any image in bucket 9.

Any outstanding technical contributions will be taken into consideration when assigning buckets/ranks. **Technical contributions alone will not get you a good grade.**

A letter grade will then be assigned to each bucket. For example, here are examples of grades given to each bucket (along with the bucket descriptions) from previous offerings of the course:

Note that these are not the guidelines for this year. Bucket descriptions change based on the pool of images in the current class — only use these as an approximate reference.

- B. Image lacked complexity and/or exhibits serious artifacts (e.g. a simple box with shapes; black holes all over the image).
- B. Image has significant problems with texturing, lighting, and/or geometry (e.g. no textures; flat shading).
- B+. Incorporates more sophisticated models and/or custom-made models. The scene is still very simple or suffers from lighting or texturing problems. i.e. simply making a complicated model in Blender/Maya is not enough if the overall scene is sub-par!
- A-. Images in this bucket and higher exhibit an aesthetic appeal through having a focus/narrative. They are distinguished by some artistic merit or technical work, but may still lack complexity or have some problems with lighting or texturing.
- A. Image looks good through effective use of lighting, custom geometry, or good composition.
- A. Images are more complex than those of previous buckets. They contain great attention to detail, effective use of lighting, and/or technical effort. Strong artistic/aesthetic appeal.
- A. Images have good lighting and geometry. Images are cohesive and are more aesthetically appealing than those of previous buckets.
- A+. Excellent scene composition and artistic merit. Few to no visible artifacts. Might have superior technical merit through the effective use of custom geometry and custom shaders.