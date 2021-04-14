# HW7 Geometry Modeling

CS 148 Fall 2020-2021
Due Date: Monday, 2 November 2020 by 7 pm PT

Follow the instructions carefully. If you encounter any problems in the setup, please do not hesitate to reach out to CAs on Piazza or attend office hours on Nooks.

Be aware of the **Checkpoints** below. Make sure you complete each one since we will grade based on them.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled.png)

"Growing" geometry. Source: [Nervous System.](https://n-e-r-v-o-u-s.com/blog/?p=6721)

The goal of this assignment is to help you get more comfortable with modeling geometry in Blender, and to start building your scene for your final project. You will become familiar with the process of taking a piece of geometry, whether it be one you found or one you created, and placing it into your scene.

It is highly recommended that you use this assignment as a milestone towards your final project, as you will be able to get some preliminary feedback from the teaching team. This assignment will focus on the geometry behind your scene, so there will be no texturing, lighting, or coding, but it’s still a good idea to start thinking about how you might want the final scene to look.

# I. Importing 3D Models

While we have primarily worked with primitive meshes (e.g. cubes, spheres, etc.) in previous homework assignments, there are infinite possibilities for models one might create! We saw examples of [past final projects](http://web.stanford.edu/class/cs148/showcase.html) in lecture, where students leveraged free online resources to incorporate some more complex 3D models in their scenes. In this section, you will be given some pointers on how to get started exploring the breadth of resources online, and you will choose and import a model for your own scene.

**Overview at a high-level:**

1. Find a model
2. Download the model
3. Import the object in Blender
4. Optional: modify the object to work with your scene

## I.1 Find a 3D model to use

It is **highly recommended** that you choose models that are available in the Blend (.blend) or OBJ (.obj) file format. You've had some experience working with Blend files in previous homework assignments; OBJ files are another simple format for representing 3D geometry. OBJ files store only an object's geometry data (note that it doesn't store data on textures, materials, etc.). If you open it with XCode (Mac) and 3D Builder (Windows), you can get a preview of what the object looks like before loading it in Blender.

OBJ is a human-readable file format, so to view the data itself, you can open it with any text editor of your choice. If you have never worked with the OBJ file format before and want to better understand what each line in the data represents (e.g. 'v', 'f', etc.), you might find [this website](http://paulbourke.net/dataformats/obj/) helpful.

There are many free resources for finding meshes online, but here are some cool places you might start:

- General: [Poliigon](https://www.poliigon.com/search?type=model&refine_by=assets-free), [TurboSquid](https://www.turbosquid.com/3d-model/free), [CGTrader](https://www.cgtrader.com/free-3d-models), [3DSky](https://3dsky.org/3dmodels?types=free&page=1), [Dimensiva](https://dimensiva.com/free-3d-models/), [3DModelHaven](https://3dmodelhaven.com/models/)
- Specifically Blender assets: [Blendswap Blends](https://www.blendswap.com/blends)
- Unique scanned artifacts: [Sketchfab CC0 Historical Artifacts](https://sketchfab.com/nebulousflynn/collections/cc0)
- Landscapes: [Quixel Megascans](https://quixel.com/megascans/free)
- 3D map models: [Map models importer](https://github.com/eliemichel/MapsModelsImporter) (tool for importing from e.g. Google maps)

The steps for downloading a model slightly depends on the website you’re using. The steps for importing an object into Blender using a different website are largely the same - the only difference is how you download the OBJ / Blend file from the website.

Here is a step-by-step walkthrough example of how to import an object from TurboSquidNote that to use TurboSquid, you will need to register for an account - however, it’s free and there is a wide variety of models to choose from.

- **Instructions for Downloading Models**

    1. Search for a model

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%201.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%201.png)

    Search for a 3D model

    2. Filter for **free** models in the **.obj** file format (or .blend)

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%202.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%202.png)

    Filter for free resources

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%203.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%203.png)

    Filter for .obj file format (or .blend)

    3. Choose which model you want to use and open its product page

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%204.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%204.png)

    Choose a model

    4. Download to your TurboSquid account. Note that this does not download it onto your computer yet - when you click “Download,” it will redirect you to your TurboSquid Downloads asset manager.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%205.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%205.png)

    Download the model to asset manager

    5. From your TurboSquid Downloads, save the downloaded .obj file by clicking on the file name (“icecream.obj”). Some models also come with texture / shading materials that you can download (“tex.zip”) - though we will not be working with texturing / shading in this assignment, you might want to download these files and explore what these materials look like.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%206.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%206.png)

    Download the model to your computer

## I.2 Import into Blender

Once you’ve got your downloaded model, you’re ready to add it to your scene in Blender. To import an OBJ file in Blender, go to File ‣ Import ‣ Wavefront (.obj), or another format that matches your file.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%207.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%207.png)

Import Wavefront OBJ file

Navigate to the folder where you saved the model, select the .obj file, and click Import OBJ. Leave the default import settings.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%208.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%208.png)

Find and select your downloaded object

You should now see your imported object in the 3D viewport, and the name of the object should appear in the outliner region.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%209.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%209.png)

Import into Blender (resize as needed)

If it looks something like this, it is likely because your object is massive, so the first thing you’ll want to do is scale down the size (S, 0.1 or some other magnitude <1) until you can see the whole object, like below.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2010.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2010.png)

Imported object, resized

Once you’ve resized as needed, you might want to move (G, X to snap and move the object along the x-axis; G, Y to move it along the y-axis; G, Z to move it along the z-axis) or rotate the object (R; note that the same shortcuts apply for rotating the object around a specific axis) to position it in your scene. Feel free to also move the camera (same keyboard shortcuts, just with the camera selected) to frame the shot however you want.

When you're ready, render View ‣ Viewport Render Image **from the camera view** and save the image:

- [ ]  **Checkpoint 1: Render the image with your imported object.** Your imported object should be fully visible in the image.

# II. Creating Geometry

Choose **ONE** of the three following options for creating your own geometry in Blender. You can do this either from scratch (i.e. start with a basic mesh in Blender), **or** start with a 3D model from an online resource. If you choose to start with a 3D model you find online, **you must demonstrate that you have significantly changed the geometry** (using one of the following techniques) - be prepared to show the original model, and discuss the changes you made.

Also note that any model you find online or create/generate yourself must be more complex than a simple geometric primitive (e.g. sphere, cube, plane, conic, etc.) or a trivial combination of multiple geometric primitives (e.g. two spheres stacked on top of each other). **You will not receive credit for any piece of geometry that can be made without non-trivial modifications** in any 3D modeling package. Any non-rigid transformation (i.e. any deformation that is not just a scale, translation, or rotation of the mesh) will be considered a “non-trivial modification.” If these requirements are at all unclear, ask a CA or post on Piazza for guidance and clarification on whether your object meets the requirements.

- [ ]  **Checkpoint 2: Viewport render the image from the camera view with a piece of geometry you create yourself, using at least one of the three techniques below.**

## II.1 Polygon Modeling

Polygon modeling is the basis of every 3D modeling package, like Blender. With modeling, we manipulate polygonal meshes by moving around vertices, edges, and faces to create complex and interesting objects. Modeling is ideal for creating hard-surface objects (i.e. man-made things, objects with hard angles) due to the precision of selecting and moving individual vertices. On the flip side, modeling is not so great for organic objects - if you're hoping to create a more organic effect, sculpting techniques might be better for this (see Section II.2 Sculpting below).

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2011.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2011.png)

Dining Table in wireframe mode. [ArtStation.](https://www.artstation.com/artwork/aRY5V2)

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2012.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2012.png)

Stormtrooper Helmet in wireframe mode. [ArtStation](https://vince_niebla.artstation.com/projects/XQGvR).

- **Instructions**

    Until now, we have primarily been working in Object Mode in Blender. To access the modeling tools in Blender and make changes to objects at the vertex/edge/face-level, we will want to be in Edit Mode.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2013.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2013.png)

    Switch to edit mode in the dropdown

    Once in Edit Mode, you will notice that 1) new tools have appeared in the sidebar, and 2) you can now see the individual vertices and edges that make up your object meshes.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2014.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2014.png)

    Objects in edit mode, and mesh editing tools in left toolbar

    Now, you will be able to use these tools to manipulate meshes and create interesting objects for your scene. Note that in Edit mode, you will be making changes to objects by manipulating vertices, edges, or faces.

    **Selection**

    Simply click on a vertex to select it. If you want to select multiple vertices, hold Shift, and click on other vertices that you want to select. You can also toggle between “Vertex select,” “Edge select,” and “Face select” in order to make selections easier / quicker. In the screenshot below, “Vertex select” is enabled, and we have selected a single vertex of the cube. The corresponding shortcut is 1, 2, and 3.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2015.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2015.png)

    Selecting vertices, edges, and faces

    **Deletion**

    To delete a vertex / edge / face, simply press X while the vertex / edge / face is selected. This will bring up the “delete” menu, which you can use to specify exactly what you want to delete.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2016.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2016.png)

    Right click → Delete (shortcut X) 

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2017.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2017.png)

    Cube with the deleted vertex

    **Extruding regions**

    A basic but powerful mesh editing tool is the Extrude Region tool, which does exactly as its name suggests - it allows you to easily extrude the selected region based on the local surface normals.

    To extrude a face, first select the Extrude Region tool in your toolbar. Then, select the face you want to extrude (switch to “Face select” and click on the face).

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2018.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2018.png)

    Extrude region tool (1 face)

    Next, click and drag the yellow + symbol. That’s it!

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2019.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2019.png)

    Cube with extruded region (1 face)

    Keyboard shortcut is also available: first select the face, then hit E to extrude.

    We can also extrude an entire region composed of multiple faces. Simply select the faces you want to extrude (hold Shift and click to multi-select), and drag the yellow **+** symbol.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2020.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2020.png)

    Extruding 2 faces

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2021.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2021.png)

    Cube with extruded region (2 faces, using local normal)

- **Resources**
    - [This Youtube video series](https://www.youtube.com/watch?v=7bHleRTEmZ0&list=PLa1F2ddGya_-UvuAqHAksYnB0qL9yWDO6&index=8) is a great basic intro series to modeling on Blender's official channel. It was created as part of Blender's 2.8 fundamentals series, but works in Blender 2.9 as well.
    - Other common techniques for modeling are with booleans and bevels - see [this beginner’s Youtube video tutorial](https://www.youtube.com/watch?v=epkluf3WJyQ) for how to do so in Blender 2.9.
    - Blender has a free add-on for performing boolean operations. It already comes with Blender, but see [here](https://blender-addons.org/bool-tool-addon/) for how to enable the "Bool Tool," configure its preferences, and keyboard shortcuts.
    - For more in-depth information on how to use *any* of Blender's modeling tools, see the [full Blender documentation](https://docs.blender.org/manual/en/latest/modeling/meshes/editing/index.html) on editing meshes.
    - There are many, many more modeling tutorials on Youtube, so if there's a specific object you're interested in creating, try searching on Youtube for a video tutorial that can help get you started.

## II.2 Sculpting

Sculpting is best suited for organic shapes and uses brushes to deform the object.

The resulting mesh of sculpting will likely to have a high polygon count. You will need decent computing power to handle sculpting details. The topology of the mesh will also need to be cleaned up after the shapes are sculpted, in order to be textured.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2022.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2022.png)

Scuplting a realistic face. Be aware, human faces are really hard to get right! Uncanny valley still exists. [FlippedNormals.](https://flippednormals.com/downloads/sculpting-a-realistic-male-face-in-zbrush/) 

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2023.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2023.png)

Creature sculpting done in Blender. [ArtStation](https://www.artstation.com/artwork/6R5mw).

- **Instructions**

    To access the modeling tools in Blender and make changes to objects, we will want to be in Sculpt Mode. Access it by directly clicking the Sculpting tab on the top or through the Object mode menu.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/sclupt_img.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/sclupt_img.png)

    Access Sculpt Mode

    Once in Sculpt Mode, you will again notice that new tools have appeared in the sidebar. 

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_11.09.50_AM.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_11.09.50_AM.png)

    Sculpt Brush Tools

    If you have imported an object, you may want to sculpt without any material. To set the object to the default white, click to change the MatCap. For less pronounced details, unclick cavity if already selected. For a smoother look, turn on smooth shading or add subdivisions.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_11.14.28_AM.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_11.14.28_AM.png)

    Change viewport lighting before sculpting

    **Brush Settings**

    Now, we will go over some brush settings. On either the top or sidebar you can change the size of the brush using Normal Radius and the intensity using Hardness. On the top right, you can change symmetry between x,y,z. The brush, at default, is symmetrical around x, which will similarly affect both sides of the face below.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_11.37.53_AM.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_11.37.53_AM.png)

    Sculpt Brush Settings

    Note: Toggling ctrl/cmd while using the brush will change the direction the brush affects the geometry. Holding down ctrl/cmd subtracts from the object using the brush shape while not using ctrl/cmd will add to the object using the brush shape.

    **Accumulate and Dyntopo**

    Next, you can turn on/off accumulate above which causes strokes to accumulate on top of each other and front faces which causes the brush to only affect the vertices facing the viewer.

    Finally, use Dyntopo! This tool will help you add or remove geometry, allowing you to construct more complex shapes out of a simple mesh. If you need more detail in a model, you do not have to manually bump up the vertex count. Instead, enable Dyntopo for dynamic tessellation sculpting method.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-12_at_5.57.27_PM.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-12_at_5.57.27_PM.png)

    Above, Dyntopo was used with accumulate. The clay strips brush was applied to the top of the monkey's head to make it larger.

    With a combination of the above settings and brushes, you will be able to sculpt different objects and meshes for your scene.

- **Resources**

    For an introduction to sculpting and an explanation of the various brushes - see the official [Blender Sculpting Fundamentals](https://www.youtube.com/watch?v=TAGWu08oWAM&list=PLa1F2ddGya_-UvuAqHAksYnB0qL9yWDO6&index=42) and [Sculpting in Blender with Complex Models](https://www.youtube.com/watch?v=A-Wq8K8icpQ) for how to do so in Blender 2.8 (the tutorial also works with 2.9). There's also this [post](https://www.artstation.com/pablodp606/blog/1vEn/new-blender-sculpt-mode-introduction) for first-time sculptors if you're into character modeling. The youtube channel [YanSculpt](https://www.youtube.com/channel/UCfjswDVU0XHyBN7UFG0Mi5Q) and [CGBoost](https://www.youtube.com/c/CGBoost/videos) are good places to find advanced sculpting videos.

    For more in-depth information on how to use these tools, see the full [Blender documentation on Sculpting](https://www.blender.org/features/sculpting/). For new additions, check out the [cloth brush](https://docs.blender.org/manual/en/latest/sculpt_paint/sculpting/tools/cloth.html)!

## II.3 Simulation

You can do a wide variety of complex simulations such as collision, rain, fire, smoke, fluid, cloth, and destructing objects in Blender. Today we will simulate a cloth falling down on Suzanne (the monkey) to get you used to the physics simulations.

Simulations may look cool, but they require a lot more resources to compute. Be prepared for long computation time, high memory usage and large cache files on your disk, especially for fluid simulation. There're also a bunch of parameters to tune for each simulation, so it could take a long time to get your desired result if you don't fully understand them.

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2024.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2024.png)

Rigid body simulation. [BlenderGuru](https://www.blenderguru.com/tutorials/quick-tutorial-make-a-wrecking-ball-with-rigid-body-physics).

![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2025.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2025.png)

Explosion. [Iridesium](https://www.youtube.com/watch?v=a9yXTXIRA4k).

- **Instructions**

    Add both a plane and monkey mesh. We will drape the plane (our cloth) onto the monkey. Move the plane above the monkey by clicking G and then Z, moving the plane upward. Then, click S to scale the plane, making it bigger than the monkey.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_1.55.33_PM.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-11_at_1.55.33_PM.png)

    Adding object meshes

    **Creating Subdivisions**

    To make the monkey and cloth smoother, we add the Subdivision Surface Modifier to both the cloth and monkey using the following settings. This will add more resolution to the meshes, creating a higher fidelity simulation result. For additional smoothing in the monkey, use Shade Smooth.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2026.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2026.png)

    Adding modifiers

    Change to Edit Mode and click on the plane. Right-click on cloth and click subdivide and then change the number of cuts below to 15. This combined with the subdivision modifier will be the mesh resolution for the simulation, in our case `mesh_resolution*2^(subdiv_level_viewport)`=$16\times2^2$.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2027.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2027.png)

    Subdivide in edit mode

    **Adding Physics**

    To add physics, go to Physics Properties. For the plane, add Cloth by clicking on the corresponding enable physics button. For the monkey, add just Collision.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2028.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2028.png)

    Physics Settings

    **Note: More Subdivisions in Cloth!**

    You can add a further subdivision to the plane after you enabled cloth in physics settings. The order of adding subdivisions and adding physics settings matters! 

    Increasing the subdivisions before the physics settings will create greater resolution, thus more folds and wrinkles when the plane simulates into a cloth. Doing the subdivision after adding the physics setting, like we are doing now, will not change the simulation result but acts as a "post-processing" to make the simulation result look smoother.

    Physics will also act as a modifier. Check the modifier stack for the order of modifiers.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2029.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2029.png)

    Subdivision added before and after Physics.

    Go to the first frame. Click Play on the bottom (or spacebar), and you will be left with this simulation.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2030.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Untitled%2030.png)

    **Common Mistakes**

    If your monkey or cloth needs more details (looks stiff or even bounced off the monkey) and looks like the image down below, go back and make sure you added enough subdivision for both the cloth and monkey before the simulation.

    ![HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-15_at_10.11.22_AM.png](HW7%20Geometry%20Modeling%20a179df33159f45b991ac527a8d3d476d/Screen_Shot_2020-10-15_at_10.11.22_AM.png)

    Unsmooth cloth and monkey

    With a combination of the above physics settings, you will be able to provide simulations for different objects and meshes for your scene. For credit and walkthrough of cloth simulation - see [cloth simulation tutorial](https://www.youtube.com/watch?v=-vVoQ-1U0SY).

- **Resources**

    For an overview of resources for different physics simulations - see this short [Blender Simulations](https://www.youtube.com/watch?v=ojmtUqivYZQ) video. For more advanced simulation techniques - see [Blender Physics - Simple Flow](https://www.youtube.com/watch?v=WMQdiC-6aVE) and [Blender Physics - Liquid Simulation](https://www.youtube.com/watch?v=fuuKOFLmg3U) for how to do so in Blender. 

    To find more in-depth information on how to use these tools, see the full [Blender documentation physics simulation](https://docs.blender.org/manual/en/latest/physics/introduction.html).

# III. Building a Scene

Your final ray-traced image ([the final project](http://web.stanford.edu/class/cs148/assignments/Final_Project_Ray_Traced_Image.pdf)) will, at the least, require one model you created/generated yourself. If you use the Blender Cycles render engine for your final ray-traced image, you will be expected to have created (i.e. modeled/sculpted/simulated) **at least half of the main objects** in your scene yourself.

Note that for this assignment, we do not expect a masterpiece for your scene - the baseline requirements focus on building upon the previous checkpoints and just putting your objects together in a scene.

**Requirements:**

- You must have at least 2 non-primitive objects in your scene. Though we only require 2 objects in your scene for this assignment, we strongly recommend ****adding more objects to build out a foundation for your final project image.
- At least one object must be imported from an online resource (though you can change the geometry as you wish)
- At least one object must be created by yourself, i.e. must have some non-trivial modification
- Note that while we will not be requiring any manipulation of lighting or shaders for this assignment, you may need to tweak your camera parameters in order to make the models in your scene visible in the rendered image.

- [ ]  **Checkpoint 3: Viewport render the image of your scene.**

# V. Grading (5 pts total)

This assignment will be graded on the following requirements

### Complete all the checkpoints (4 pts)

1. (1 pt) **Render the image with your imported object.**
2. (2 pt) **Render the image from the camera view with a piece of geometry you create yourself, using at least one of the three techniques.**
3. (1 pt) **Render the image of your scene.**

### Quiz Question (1 pt)

The TAs will choose one of the following questions during the grading session. Please be prepared to give a one-minute answer with your partner.

1. What is Laplacian smoothing? Why does Laplacian smoothing eventually shrink a closed curve/surface to a single point?
2. What could be a problem of loop subdivision on a mesh with sharp edges?
3. Describe how procedural geometry works, and give (at least) two examples of what it can be used to create.
4. How can we subdivide spline curves?
5. How can B-Splines be extended from curves to surfaces, and what about them makes it intuitive for artists to do quick mesh editing?
6. What is the marching cubes algorithm used for, and how does it work?
7. What is the loop subdivision, and how does it work?
8. What are implicit surfaces, and what are (at least) 2 advantages of implicit surfaces compared to triangle meshes?