# 3D Desk Scene Project

## CS-330: Computational Graphics and Visualization

This repository contains my 3D desk scene project, which recreates my actual workspace using OpenGL. The scene includes a monitor, keyboard, mouse, desk lamp, coffee mug, and stacked books, all rendered with realistic lighting and materials.

---

## Project Reflection

### How do I approach designing software?

Working on this 3D graphics project has taught me valuable design skills that go beyond just writing code. I learned to think visually and spatially, planning how objects would fit together in 3D space before implementing them. The process of breaking down complex real-world objects like a desk lamp or coffee mug into simple geometric primitives (cylinders, boxes, spheres) taught me how to decompose problems into manageable pieces. This is a skill I can apply to any software project, not just graphics work.

My design process followed an iterative approach. I started by sketching out my desk setup and identifying which objects would be most interesting to model. Then I tackled one object at a time, beginning with simpler shapes like the monitor and gradually working up to more complex assemblies like the lamp with its multiple articulated parts. I constantly refined the positioning and scaling of objects by running the program, observing the results, and adjusting the parameters. This cycle of design, implement, test, and refine became my standard workflow.

These design tactics are directly applicable to future work. The habit of starting with a clear plan, breaking problems into smaller components, and iterating based on feedback works for any development project, whether I am building a web application, mobile app, or another graphics program. The visual thinking skills will especially help in UI/UX design and any work involving data visualization.

### How do I approach developing programs?

The 3D scene project introduced me to several new development strategies. I learned to work with transformation matrices and understand how translation, rotation, and scale operations combine to position objects in 3D space. The lighting system taught me about shader programming and how mathematical models simulate real-world light interactions. I also developed a better understanding of the graphics pipeline and how data flows from vertex definitions through transformations to final pixel colors on screen.

Iteration was fundamental to my development process. I did not try to build the entire scene at once. Instead, I added one object, got it working correctly, then moved to the next. When adding the stacked books, for example, I first created the bottom book, tested its position and color, then added the top book and adjusted its height to sit properly on the first one. Each iteration taught me something new about object positioning or material properties that informed the next addition. This incremental approach prevented me from getting overwhelmed and made debugging much easier because I always knew which recent change caused any new problem.

My coding approach evolved significantly throughout the project milestones. Early on, I wrote repetitive code for each object with hard-coded transformation values scattered everywhere. As the scene grew more complex, I realized this was unsustainable. I refactored my code to use helper functions like SetTransformations() and SetShaderMaterial(), which made the codebase much cleaner and more maintainable. By the final milestone, I was thinking in terms of reusable components and modular design rather than just getting individual objects to appear on screen. This evolution from novice procedural code to more organized, function-based architecture mirrors the learning curve of becoming a better programmer.

### How can computer science help me in reaching my goals?

Computational graphics and visualizations have given me knowledge and skills that extend far beyond this specific project. Understanding 3D mathematics, coordinate systems, and spatial transformations provides a foundation for many areas of computer science. In my future educational pathway, these concepts will be relevant to courses in virtual reality, augmented reality, game development, simulation, and scientific visualization. The mathematical thinking required for graphics work, particularly with vectors and matrices, strengthens my overall problem-solving abilities and will help in advanced computer science courses involving algorithms and linear algebra.

Professionally, computational graphics skills open doors to numerous career paths. The game industry obviously values 3D graphics expertise, but so do fields like architectural visualization, medical imaging, data visualization, and user interface design. Even if I do not work directly in graphics programming, the ability to create visual representations of data and concepts is increasingly valuable across all technology sectors. Companies need professionals who can turn abstract data into understandable visualizations, whether that is for business analytics dashboards, scientific simulations, or interactive product demonstrations.

Beyond the technical skills, this project taught me patience, attention to detail, and systematic debugging. Graphics programming is unforgiving because errors are immediately visible. A misplaced transformation or incorrect lighting calculation produces obvious visual artifacts. Learning to methodically track down these issues and fix them has made me a more careful and thoughtful developer. These soft skills, combined with the hard technical knowledge of rendering pipelines and 3D mathematics, give me a versatile toolkit for tackling complex problems in my future career.

---

## Technical Implementation

### Scene Objects
- **Monitor**: Box meshes with texture mapping for screen
- **Keyboard**: Multiple box meshes arranged in grid pattern
- **Mouse**: Sphere mesh with additional boxes for buttons and cylinder for scroll wheel
- **Desk Lamp**: Hierarchical assembly of cylinders and cone
- **Coffee Mug**: Cylinder body with curved handle made from rotated cylinders
- **Stacked Books**: Box meshes with rotation and color materials (green bottom, red top)

### Key Features
- Realistic lighting with ambient, diffuse, and specular components
- Multiple material types (plastic, metal, rubber)
- Texture mapping for monitor and mouse
- Camera navigation with keyboard (WASD, QE) and mouse controls
- Modular code organization with reusable transformation functions

### Custom Functions
- `SetTransformations()`: Handles object positioning with scale, rotation, and translation
- `SetShaderMaterial()`: Applies material properties for realistic lighting
- `SetShaderColor()`: Applies solid colors to objects
- `SetShaderTexture()`: Binds textures for surface detail
- Various `DrawMesh()` functions: Render different geometric primitives

---

## Project Files
- `SceneManager.cpp`: Main scene rendering and object definitions
- `README.md`: This file with project reflection
- `Design_Decisions_3D_Scene.docx`: Detailed design decisions document

---

## Running the Project

The project requires OpenGL, GLEW, GLFW, and GLM libraries. Camera controls:
- **WASD**: Move forward, left, backward, right
- **QE**: Move up and down
- **Mouse**: Look around (first person view)
- **Scroll Wheel**: Adjust movement speed

---

## Acknowledgments

Course materials and tutorials from CS-330: Computational Graphics and Visualization at SNHU provided the foundation for this project. The OpenGL community resources and documentation were invaluable for understanding graphics programming concepts.
