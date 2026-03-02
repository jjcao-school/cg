# Computer Graphics - 2026 (DLUT)
## 0. Introduction
- 授课32学时（上机24学时）.
内容涵盖3D Transformation, Image Processing, 渲染(光栅化rasterization和光线追踪)，3D几何建模，计算机仿真动画，以及人工智能与图形学。
应用为主，理论为辅，大家需要多动手实验，积极解决实际问题。
Note that C++ is not required; the assignments can be completed using JavaScript and WebGL.

- 通过这门课程的学习，你将会了解计算机图形学的基本知识，掌握一定的CG操作和编程技能。具体如下：
  - Read, write, and manipulate digital images,
  - 通过坐标变换组织3D scenes and objects,
  - Render 3D objects using textures, lighting, shadows, and reflections,
  - Explain the fundamental concepts behind computer animation and physics-based simulations in graphics,
  - Develop WebGL applications that can display 3D models on web pages.
<!-- Develop interactive graphics software using the GPU rendering pipeline,
Describe sampling and signal processing operations used for image synthesis and representation,
Design software with typical representations of curves and surfaces used in computer graphics,
-->

- Course Instructor: [Junjie Cao](http://jjcao.github.io/); Email: jjcao at dlut.edu.cn; 
- Lectures: 周二 (15:35 - 17:10) & 周四 (13:30 - 15:05) at 第一教学馆 1-316. 上机时间待定！！！
- Textbooks: This course will not follow any textbook. You can find some from the course website I recommended.  



## 1. Schedule (subject to change)
### 1.1 Introduction & transformation
- [00_01_introduction](http://pan-yz.chaoxing.com/share/info/dc5968d8ed5cc29f) 
- [00_02_light](http://pan-yz.chaoxing.com/share/info/c74faa7e2618ecdc), reading: [人眼亮度感知的非线性与gamma矫正](https://www.zhihu.com/question/27467127)
- [00_03_camera](http://pan-yz.chaoxing.com/share/info/ebe6118e1449a61b)
- [01_01_2d_Transformations](http://pan-yz.chaoxing.com/share/info/5104d084e1a06ad3)
- [01_02_3d_Transformations](http://pan-yz.chaoxing.com/share/info/a08fa5722fe65ae0), assignment 2 out
- [01_03_viewing_3d_to_2d / viewing transformation](http://pan-yz.chaoxing.com/share/info/e116e246237394d0)
- Review
  
### 1.2 Ray tracing
- [02_01_rasterization-device-triangle](http://pan-yz.chaoxing.com/share/info/13e13623fe1ab681)
- ray tracing
- optics &nshading
- Monte Carlo Path Tracing
- Camera models
- Materials
- Ray tracing accelerating
- Adbanced Topics in Rendering
- Review

### 1.3 Pipeline & Texture
- Graphics pipeline & Shader
- Texture mapping

### 1.4 Geometry
- Representation
- Mesh
- implicit <=> explicit representation
- Digital geometry processing
- Spline
- Review

### 1.5 AI for CG (SIGGRAPH 2019)
- Introduction
- Neural Networks
- Suervised Learning
- Unsupervised Learning

### 1.6 Animation
- Simulation
  - Mass-spring & SPH


### 1.7 Rasterization
- Sampling & Antialiasing
- Quantization & Dithering
- Rasterize lines & circles
- Review

## 2. Assignments (not fully determined)
- 4--6 assigments without C++.
- 作业体验：你只需双击打开 index.html，就能在浏览器里看到极其精美的可视化 UI 界面。通过修改 JavaScript 代码，你可以实现图像处理、3D网格编辑、光线追踪和物理动画。保存代码后刷新浏览器，立马就能看到效果，调试起来极为直观，且你完成的作业可以直接作为一个网页链接发给朋友或写进简历里。

## 3. Courses
1. **https://cos426.cs.princeton.edu/ @ Fal 2025**
   - 6 assignments: JavaScript + WebGL 
2. **https://graphics.cs.utah.edu/courses/cs4600/fall2025/ @ utah**
   - best and most understandable introductory
   - 7 assignments: JavaScript + WebGL
   - video: https://www.youtube.com/watch?v=vLSphLtKQ0o&list=PLplnkTzzqsZTfYh4UbhLGpI5kGd5oW_Hh

## 4. Other Resources
- [什么是计算机图形学？](http://staff.ustc.edu.cn/~lgliu/Resources/CG/What_is_CG.htm)
- 进阶
    You may want to browse interesting research papers in the top avenues in graphics (Siggraph, Siggraph Asia, ACM TOG, Eurographics) and computer vision (CVPR, ICCV, ECCV), as well as some more specialized but equally excellent conferences (SGP, SCA, 3DV). 

<!-- - Prerequisites: linear algebra, C/C++ programming, and Data Structures -->