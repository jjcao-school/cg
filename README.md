# Computer Graphics - 2021 (DLUT)
## 0. Introduction
授课32学时（上机24学时）.内容涵盖光栅化rasterization和光线追踪等渲染算法，3D几何建模的数学概念和算法，计算机动画算法，应用为主，理论为辅，大家需要多动手实验，积极解决实际问题。通过这门课程的学习，你将会学习到计算机视觉和计算机图形学的基本知识，学习和掌握一定的编程技能。

<!-- - 目标
    By the end of the course, the student must be able to:
  - Explain and apply the fundamental mathematical concepts of computer-based image and geometry synthesis (synthesis data for training deep learning; basis of VR and simulation)
  - Implement a basic rendering pipeline based on rasterization and raytracing
  - Design and implement basic computer animation algorithms
  - Integrate individual components into a complete graphics application
  - Coordinate a team during a software project? -->

<!-- - 进阶
    You may want to browse interesting research papers in the top avenues in graphics (Siggraph, Siggraph Asia, ACM TOG, Eurographics) and computer vision (CVPR, ICCV, ECCV), as well as some more specialized but equally excellent conferences (SGP, SCA, 3DV). -->

<!-- - Prerequisites: linear algebra, C/C++ programming, and Data Structures -->

- Course Instructor: [Junjie Cao](http://jjcao.github.io/); Email: jjcao at dlut.edu.cn; 
- Lectures: Tuesday (13:30 - 15:05) & Friday (08:00 - 09:35) at 综合教学2号楼 A301. 上机时间待定！！！
- Textbooks: 
  - [FCG4]: [Fundamentals of Computer Graphics, 4th Edition, 2016.](http://www.cs.cornell.edu/courses/cs4620/2014fa/index.shtml), has slides. 
  - [Introduction to Computer Graphics v1.2 2018](http://math.hws.edu/graphicsbook/) by David J. Eck, Free online, with live, interactive demos with webgl.
  <!-- - [Modern OpenGL Guide](https://open.gl/), excellent! elegent!! -->

## 1. Course Notes
### 1.1 Introduction & transformation
- [00_01_introduction](http://pan-yz.chaoxing.com/share/info/dc5968d8ed5cc29f), assignment 1 out
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

### 1.5 Animation
- Space deformation
- Surface deformation

### 1.6 Rasterization
- Sampling & Antialiasing
- Quantization & Dithering
- Rasterize lines & circles
- Review

## 2. Assignments
使用Blender 2.9.0 (不要使用其他版本，包括更新的版本)，建议使用个人电脑完成。
For finishing the assignments quickly, learn [Python/NumPy Review I](homework/NumpyTutorial_Blank.ipynb) first. 

[Assignments 1-8](http://web.stanford.edu/class/cs148/assignments.html)
<!-- - [Rules & Setup](assignments/)
- [Assignment 1: Hello World (Mesh display, Connected Components & Subdivision)](assignments/assignment_1), deadline: TBD
- [Assignment 3: ](), deadline: TBD -->

## 3. Reading 
- [什么是计算机图形学？](http://staff.ustc.edu.cn/~lgliu/Resources/CG/What_is_CG.htm)

## 4. Resources
### References:
- [Graduate Computer Graphics, CSCI-GA 2270-001 Fall 2020, Daniele Panozzo](https://github.com/danielepanozzo/cg)
- [CS 148 Introduction to Computer Graphics and Imaging @ Stanford by Ron Fedkiw](http://web.stanford.edu/class/cs148)
- ... 
- [CS180 / CS280: Introduction to Computer Graphics @ UCSBb by Linqi yan](https://sites.cs.ucsb.edu/~lingqi/teaching/cs180.html)
- [Introduction to Computer Graphics @ Cornell by Steve Marschner](http://www.cs.cornell.edu/courses/cs4620/2018fa/): good homework
- [COMPUTER GRAPHICS @ CMU by Keenan Crane, Nacy Pollard](http://15462.courses.cs.cmu.edu/fall2020/): **has youtube**
- [CS 1230 Introduction to Computer Graphics @ Brown]()
- [Computer Graphics - Fall 2020 @ jhu by Misha](https://www.cs.jhu.edu/~misha/Fall20/)

<!-- ### Others
- [tutorial, GL]: <a href="http://learnopengl.com">Learn OpenGL</a> (fundamental OpenGL tutorials and notes, practical techniques); <a href="https://learnopengl-cn.github.io">中文网站。</a>使用了GLFW，而不是GLUT
- [tutorial, GL]: <a href="http://ogldev.atspace.co.uk/index.html">Modern OpenGL Tutorials</a>, good explanation and code; <a href="https://blog.csdn.net/column/details/13062.html">中文网站。</a> 使用了FreeGLUT和GLEW，但是前面的code中，FreeGLUT的函数和glut的一样，可以照用。
- [tutorial, GL]: <a href="http://www.songho.ca/opengl/"> OpenGL notes from Song Ho</a>, advance, awesome explanation and code
- [povray](http://www.povray.org/): Open source project for ray tracing
- [G3D](http://g3d.cs.williams.edu/g3d/www/index.html): a modern 3d engine -->

