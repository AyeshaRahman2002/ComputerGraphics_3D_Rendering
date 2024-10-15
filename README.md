ComputerGraphics_3D_Rendering
=====================

## Overview
This repository contains the implementation of a 3D rendering application using modern shader-based OpenGL. The application includes functionalities for matrix and vector operations, texturing, lighting, and animation. It features multiple tasks, each contributing to different components such as rendering, texturing, and performance measurement.

## Project Structure
- assets/: Contains runtime assets like textures, models, and shaders. All runtime data is stored here.
- main/: The main project source code, where most of the development work occurs.
- support/: Pre-provided support functions from exercises. Modifications to this code are not allowed.
- vmlib/: Math library with essential but incomplete functions. Missing functions were implemented, and additional operators were added where necessary.
- third_party/: Third-party code used in the project. Documentation and permission are required for any new additions.

## Team Members

Ayesha Rahman

Sandra Guran

Geeyoon Lim

## Tasks Breakdown

1. Matrix/Vector Functions
- Implemented essential matrix and vector operations for 3D computations, including matrix multiplication, rotations, and translations.
- Testing was conducted using Catch2, ensuring the results matched expected values with high precision.
  
2. 3D Renderer Basics
- Developed a 3D renderer using OpenGL to load and display a terrain OBJ file representing the Paarlahti region in Finland.
- Implemented first-person camera controls using keyboard and mouse inputs, including adjustable movement speed.
    ![Alt text](https://github.com/sc21samg/GraphicAlgorithms_3D_Rendering/blob/main/1.2%20git.png)
  
3. Texturing
  ![Alt text](https://github.com/sc21samg/GraphicAlgorithms_3D_Rendering/blob/main/1.3%20git.png)
- Applied orthophoto textures to the terrain using shaders for texture mapping and sampling.
- Debugged texture sampling issues and validated texture coordinates using checkerboard patterns before applying actual orthophotos.
  
4. Simple Instancing
- Added two launch pads at different coordinates and applied textures, ensuring correct rendering through OpenGL.
  
5. Custom Model
  ![Alt text](https://github.com/sc21samg/GraphicAlgorithms_3D_Rendering/blob/main/1.5%20git.png)
- Constructed a 3D rocket model composed of basic shapes (cubes, cylinders, and cones) and positioned it accurately on the launch pad.
  
6. Local Light Sources
  ![Alt text](https://github.com/sc21samg/GraphicAlgorithms_3D_Rendering/blob/main/1.6%20git.png)
- Implemented the Blinn-Phong shading model to simulate ambient, diffuse, and specular reflections. Added distance attenuation for point lights.
- Debugging revealed issues with lights following the camera, which remain unresolved.
  
7. Animation
- Created a dynamic flight animation for the rocket with lift-off and horizontal flight phases using a state machine approach for managing different stages.
- The animation incorporates timing managed by GLFW to maintain frame-rate independence.
  
8. Measuring Performance
- Measured rendering performance using OpenGL query objects and CPU timing via std::chrono::high_resolution_clock.
- Detailed GPU and CPU time analysis was performed for each major section, highlighting bottlenecks and suggesting optimizations.

## Results
- Rendering Performance: The application was tested across multiple systems with different GPU capabilities (e.g., Intel Iris Xe, Intel UHD Graphics) to evaluate performance.
- Lighting and Texturing: Visual improvements were achieved through the integration of Blinn-Phong shading and texture mapping, although some issues remain with light source positioning.
- Animation: The rocket’s smooth flight animation demonstrated the application’s ability to simulate complex motion realistically.

## Conclusion
The project successfully implemented a functional 3D rendering application using modern OpenGL techniques, showcasing skills in matrix computations, shader development, and real-time rendering. The application provides a solid foundation for future work, such as more advanced lighting models and interactive simulations.
