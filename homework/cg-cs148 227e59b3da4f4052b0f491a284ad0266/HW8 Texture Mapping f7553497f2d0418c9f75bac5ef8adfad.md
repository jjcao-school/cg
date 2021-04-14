# HW8 Texture Mapping

CS 148 Fall 2020-2021
Due Date: Monday, 9 November 2020 by 7 pm PT

Follow the instructions carefully. If you encounter any problems in the setup, please do not hesitate to reach out to CAs on Piazza or attend office hours on Nooks.

Be aware of the **Checkpoints** below. Make sure you complete each one since we will do the grading based on them.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled.png)

Image texture applied to objects. This particular scene uses AI to create albedo, normal and height map from a single image. Source: [Substance3D](https://magazine.substance3d.com/ai-power-2d-painting-a-massive-boost-for-substance-alchemist/), a commercial software.

The goal of this homework is to help you start picking textures for your final project. Specifically, you will become familiar with the process of texturing an object. Like HW7, it is highly recommended that you use this assignment as a milestone for your final project, as you will be able to get some preliminary feedback from the teaching team.

# I. UV unwrapping

In class, we have discussed what UV mapping is. UV mapping is the process of assigning UV coordinates to each vertex of the mesh. As mentioned in class, this is what is used to sample the texture. UV coordinates do not usually magically appear on meshes though — you will have to create your own UV coordinates. If you've never done UV unwrapping before, we suggest you watch [this official tutorial](https://www.youtube.com/watch?v=Y7M-B6xnaEM&list=PLa1F2ddGya_-UvuAqHAksYnB0qL9yWDO6&index=19) first before proceeding.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%201.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%201.png)

"Unwrapping" a christmas chocolate. Source: [twitter](https://twitter.com/xxivips/status/938366852039888896?lang=en).

In order to apply a texture to an object, we have to do what is called **UV unwrapping** to generate a UV map for it first. Here we will walk you through how to unwrap an object in Blender.

### I.1 First glance at the UV map

First let's visualize what a UV map looks like in blender.

Open a new Blender project and select the default cube. Then toggle the UV map editor view by clicking on UV editing. You should be able to enter Edit Mode and see the UV map of the default cube object on the left side of the screen.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%202.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%202.png)

UV Editing window.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%203.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%203.png)

The UV map of a blender default cube.

### I.2 Generate the UV map

Now let's proceed to generating a UV map for your object. You can close the default cube scene without saving.

Open your Blender project from homework 7. Here we use a simple stool model as an example. Toggle the UV map editor view. Select all vertices of an object and press U, then click on Smart UV project*.*

If your object does not have a clean topology (especially when you sculpt with dynamic topology), you may consider tidy up your mesh before unwrapping using retopology tools such as [quadriflow](https://docs.blender.org/manual/en/2.90/modeling/meshes/retopology.html#quad) from Properties ‣ Object Data ‣ Remesh.

For simulated mesh, you need to apply the simulation by going to the modifier and apply your simulation modifier before getting access to the mesh in each frame.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/28.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/28.png)

Smart UV project for automatic UV unwrapping.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%204.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%204.png)

Quadriflow remesh for sculpted objects.

You will only UV unwrap what you've selected. If you accidentally deselected an object in Edit Mode, press A in the 3D viewport window to select all vertices of it.

Then you should be able to see an auto generated UV map.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/8.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/8.png)

Smart UV Project auto generated UV map.

**Switching between multiple objects in the edit mode:** if you have multiple objects in your scene and you want to quickly switch between them when editing, you can click the mesh icon next to your target object in the outliner.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/10.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/10.png)

Switching between multiple objects in Edit Mode.

**Local View:** Turning on local view can hide non-selected objects and is very useful when other objects get in your way during editing. Select an object and press / (forward slash) or click View ‣ Local View ‣ Toggle Local View in the main window to toggle local view. 

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/9.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/9.png)

Local view of the stool top.

### I.3 Edit the UV map

Sometimes the auto-generated UV map of a complex object will be far from perfect. Each connected part of the unwrapped mesh is called a "UV Island". A good UV map should maximize its area covered by the islands with small distortion (e.g. stretched along some direction) and a reasonable amount of empty spaces between islands. There are things we can do to improve the UV map; we'll explore two techniques below. For a full list of UV editing tools, visit [Blender doc](https://docs.blender.org/manual/en/2.90/modeling/meshes/uv/editing.html).

**I.3.1 Add UV seams**

Just like in sewing, a seam is where the ends of the image/cloth are sewn together. In unwrapping, the mesh is unwrapped at the seams. Think of this method as peeling an orange or skinning an animal. You make a series of cuts in the skin, then peel it off. You could then flatten it out, applying some amount of stretching. These cuts are the same as seams.  Smart UV project creates seams automatically, but we can specify the seams to have finer control over the unwrapping process. Read more in this [Blender doc](https://docs.blender.org/manual/en/2.90/modeling/meshes/uv/unwrapping/seams.html).

Generally, artists will place seams at sharp edges, or places where non-overlapping textures are less noticeable (e.g. the back or the bottom of an object). Faces with edges not marked as seams will strictly adhere to each other. Sometimes we might want to add seams to separate a flat surface so the mesh could be better unwrapped.

In the 3D viewport, select edge selection mode.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%205.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%205.png)

Edge selection mode.

Then hold shift while clicking to select all the edges you want to mark as seams. Press ctrl/cmd+E for the Edge menu and click Mark Seam. 

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/29.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/29.png)

Mark Seam.

Seams will be marked in red in the 3D viewport.

The wireframe shading model can also be helpful to inspect an object. 

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/13.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/13.png)

Wireframe shading model.

After adding seams to an object, press *U* and select *Unwrap.* You should be able to see a new UV map with the seams you specified.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/14.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/14.png)

Manually add seams and unwrap the stool top.

**I.3.2 Directly editing the UV map**

In addition, we can directly edit the UV map. There are four different selection modes on the top left of the UV editor: 

- Vertex mode
- Edge mode
- Face mode
- Island mode

You can try whatever is suitable in your case and move, rotate, scale, or transform the selected target. A better UV map of the stool top after editing is as follows. The larger area of the square is covered by the unwrapped meshes, so that more pixels on the texture will be mapped onto the object which guarantees better details.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/15.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/15.png)

Manually adjust the UV map of the stool top.

Finally, save the UV map through UV ‣ Export UV Layout so we can create textures with this UV layout as the guide.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/16.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/16.png)

Export the UV layout.

- [ ]  **Checkpoint 1: UV unwrap one of the objects you made for HW7. Save the UV map.**

# II. Texturing

Texturing is a widely adopted method to add fine-grained detail to an object. There are different kinds of textures for different purposes: base color, normal, roughness, ambient occlusion, displacement textures, etc. Here we will show you how to apply base color, normal and displacement textures to an object. 

Texturing an object requires that the object has an associated UV map. After creating a UV map, we can apply textures to the object. Here we will apply a rock ground texture to a sphere as a demonstration. 

Before we start, download example textures (2k resolution Diffuse Map, Normal Map, and Displacement Map) from [here](https://texturehaven.com/tex/?t=rocks_ground_06). 

**If you feel comfortable with Blender, you can prepare your own texture and do the following steps on your own models as well.**

## II.1 Base Color

Open a new Blender project and delete the default cube. Let's start with a sphere. Add a UV sphere (Add ‣ Mesh ‣ UV sphere) and change it to smooth shading (right-click ‣ Shade Smooth).

The sphere is one of the Blender build-in meshes. Blender build-in meshes already have UV maps, so we can directly apply textures to them.

Then change the Render Engine to Cycles.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/17.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/17.png)

Change the render engine.

Open the Shading Editor.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/30.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/30.png)

Select shading editor.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/31.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/31.png)

The shading editor view.

The Shader Editor is used to edit materials. Materials used by Cycles and Eevee are defined using a node tree. In HW4 we played with materials in the Properties Editor as a list of parameters, but under the hood it is a tree structure. In the Shader Editor, you can create and edit the node tree more easily. Read more in this [Blender doc.](https://docs.blender.org/manual/en/latest/editors/shader_editor.html)

Add a new material for our sphere. A new material node will appear in the Node Editor.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/32.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/32.png)

Add new material.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/33.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/33.png)

Material node view window.

Go to the menu bar of the Shader Editor or press Shift + A **to open the Add menu. Search for image texture node or go to Texture ‣ Image Texture to add it to the graph.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/34.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/34.png)

Search for the image texture node.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/35.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/35.png)

The image texture node.

Click Open ****and select the downloaded base color texture *rocks_ground_06_diff_2k.jpg.* Then connect the image texture's Color channel to the material's Base Color.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/36.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/36.png)

Add the diffuse map.

You can also directly drag an image from your file explorer/finder into the node editor to create an image texture node.

Now change the Viewport Shading mode to Rendered. This allows you to view the changes you made to the material in real-time.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%206.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%206.png)

Viewport Shading mode to Rendered.

You should see a textured sphere as follows. Move around (with the middle mouse button, or click and drag on the navigation gizmo) to see what the sphere looks like. You may notice a seam on the sphere, which is from the UV map. If you're interested, you can also modify the UV map and see how the texture changes accordingly.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%207.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%207.png)

Sphere with diffuse map.

Render the image from the camera view.

- [ ]  **Checkpoint 2.1: Render the image with base color texture.**

## II.2 Normal Map

In 3D computer graphics, normal mapping is a texture mapping technique used for faking the lighting of bumps and dents. See [Wikipedia](https://en.wikipedia.org/wiki/Normal_mapping) for more. Keep in mind that normal mapping will only change the shading normal but not the actual geometry normals.

We start by adding a new image texture node and a ****normal map node (Shift + A to search, or Vector ‣ Normal Map) to the node tree. Select *rocks_ground_06_nor_2k.jpg* for the normal map node. Since the pixel value of a normal map does not represent actual colors (it's only storing the XYZ value of normal vectors in the RGB channel of an image), we should set the Color Space of the normal map to Non-Color.

Connect the Color channel from the image texture to the normal map, and the Normal channel from the normal map to the Principled BSDF.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/38.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/38.png)

Add a normal map node and apply the normal texture.

You should see a textured sphere as follows.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%208.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%208.png)

Sphere with diffuse map + normal map.

Render the image from the camera view

- [ ]  **Checkpoint 2.2: Render the image with base color texture and normal map. Discuss the effect of adding a normal map.**

## II.3 Displacement Map

Displacement mapping is an alternative computer graphics technique that uses a texture map to cause an effect where the actual geometric position of points over the textured surface are displaced, often along the local surface normal. See [Wikipedia](https://en.wikipedia.org/wiki/Displacement_mapping) for more.

Now we will create another image texture node and a **displacement node** (Shift + A to search, or Vector ‣ Displacement) and select *rocks_ground_06_disp_2k.jpg* as the displacement texture of the sphere. Make sure the Color Space of the normal map is set to Non-Color. Connect the Color channel of the displacement texture to the Height ****channel of the displacement node, then the output of displacement node to the Displacement channel of Material Output (not Principled BSDF!).

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%209.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%209.png)

Add displacement node and apply the displacement texture.

Then in Material Properties, set Displacement to Displacement and Bump.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%2010.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%2010.png)

Change displacement settings.

Since displacement mapping perturbs the actual mesh vertices and the default UV sphere has a low resolution, we need to add a subdivision modifier. As a reminder, go to Properties Editor → Modifier Properties and add a Subdivision Surface Modifier, or use shortcut ctrl/cmd+3. Set the Levels Viewport to 3.

You should see the sphere as follows. Rotate around to see what the sphere looks like now. You can adjust the Scale value of the displacement node to make the displacement larger or smaller.

![HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%2011.png](HW8%20Texture%20Mapping%20f7553497f2d0418c9f75bac5ef8adfad/Untitled%2011.png)

Subdivided sphere with diffuse map + normal map + displacement map.

Render the image and save it.

- [ ]  **Checkpoint 2.3: Render the image with base color texture, normal map, and displacement map. Discuss the effect of adding a displacement map.**

# III. Resources

As you've noticed, to get realistic materials, you will need multiple maps. Base color (Diffuse) can be some image you find online, but getting the other maps can be tricky. Here are some websites that provide free textures sets:

- [TextureHaven](https://texturehaven.com/textures/)
- [Poliigon](https://www.poliigon.com/search?type=texture&refine_by=assets-free). There's an easy to use [addon for Blender](https://help.poliigon.com/en/articles/2540839-poliigon-material-converter-addon-for-blender) that can automatically import Poliigon materials.
- [CC0 Textures](https://cc0textures.com/)
- [3D Textures](https://3dtextures.me/)
- [Textures](https://www.textures.com/)
- [3DXO](https://www.3dxo.com/textures)
- [texture.ninja](https://texture.ninja/)

If you don't find anything of your taste, you can also create other maps from the diffuse map. You can use image-editing software such as photoshop, gimp, or Krita to create the other maps, or with dedicated tools such as [CrazyBump](http://www.crazybump.com/), [ShaderMap](https://shadermap.com/home/), and [Materialize](http://www.boundingboxsoftware.com/materialize/index.php). There's even a nice [web app](http://cpetry.github.io/NormalMap-Online/) for doing so, or you can even do it [inside Blender](https://www.youtube.com/watch?v=qfrRtmJFaMM).

If you want to start from scratch, see [this tutorial](https://www.katsbits.com/tutorials/textures/making-normal-maps-from-photographs.php) on how to make all the maps from a photograph.

If you want to explore advanced texturing, you can try out the industry-standard texturing software: S[ubstance Painter](https://www.substance3d.com/education/), which has a free education license.

If you're into procedual materials/textures, this is the best time of the year because [Nodevember](https://nodevember.io/) just started. You can search on [youtube](https://www.youtube.com/results?search_query=nodevember)/[twitter](https://twitter.com/hashtag/nodevember2020)/[instagram](https://www.instagram.com/explore/tags/nodevember/) for posts from artists that do amazing things with nodes, some of them even provide [tutorials](https://www.youtube.com/watch?v=sO0ulv7wz-0).

# IV. Grading (5 pts total)

This assignment will be graded on the following requirements

### Complete all the checkpoints (4 pts)

1. (1 pt) **UV unwrap one of the objects you made for HW7. Save the UV map.** 
2. (1 pt) **Render the image with base color.**
3. (1 pt) **Render the image with base color texture and normal map. Discuss the effect of adding a normal map.**
4. (1 pt) **Render the image with base color texture, normal map, and displacement map. Discuss the effect of adding a displacement map.**

### Quiz Question (1 pt)

The TAs will choose one of the following questions during the grading session. Please be prepared to give a one-minute answer with your partner.

1. What are the pros and cons of using bump / normal maps vs. displacement maps?
2. What are the advantages and disadvantages of pixel-based and patch-based texture synthesis?
3. Suppose you are not sure whether your mesh is UV mapped correctly for your texture. How might you go about debugging? Justify your answer.
4. Why does interpolating in screen space result in texture distortion?
5. What’s the cause of aliasing?
6. Explain MIP Maps.
7. What’s the difference between MIP maps and RIP maps?
8. Describe an algorithm for pixel-based texture synthesis from a small sample.