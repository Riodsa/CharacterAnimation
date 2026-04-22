OpenGL Skeletal Animation - Playable Character
This project is a playable character system built using C++ and OpenGL. It extends the core skeletal animation concepts from LearnOpenGL to create a controllable player with state-based animations and 8-directional movement logic.

🎥 Demo Video


https://github.com/user-attachments/assets/2b90dccd-3f29-4d77-a009-74b646b57635



🎮 Controls
Player Movement
Arrow Keys: Move the character in 8 directions.

The character automatically rotates to face the direction of movement using atan2 logic.

Diagonal Movement Fix: Movement speed is normalized to prevent the character from moving faster when traveling diagonally.

Spacebar: Perform a special action (Dancing animation).

Idle State: The character automatically returns to an idle animation when no movement keys are pressed.

Camera & System
W / A / S / D: Move the camera position.

Mouse Movement: Look around (Yaw/Pitch).

Mouse Scroll: Zoom in and out (FOV adjustment).

ESC: Exit the application.

🚀 Technical Features
Animation State Machine: Manages transitions between IDLE, WALKING, and DANCING states.

8-Way Movement & Rotation: Uses vector normalization for consistent speed and trigonometric functions for smooth character orientation.

Bone Limit Extension: The system is configured to support up to 200 bones per model to accommodate complex Mixamo rigs, preventing "vector subscript out of range" errors.

Assimp Integration: Robust 3D model loading supporting the COLLADA (.dae) format.

📂 Sources & Credits
Core Engine & Logic: Based on the LearnOpenGL - Skeletal Animation tutorial series.

3D Assets: * Character Model: Character assets sourced from Adobe Mixamo.

Animations: Idle, Walking, and Dancing animations were retargeted and exported from Mixamo.

Libraries:

GLFW / GLAD: Window management and OpenGL profile loading.

GLM: OpenGL Mathematics for matrix and vector operations.

Assimp: Open Asset Import Library for skeletal data.

stb_image: Image loading for textures.

🛠️ Build Instructions
Ensure you have CMake and Visual Studio (or another C++ compiler) installed.

Install required dependencies: assimp, glfw, and glm.

Place your model files in resources/objects/.

Compile the project using the provided Visual Studio solution or CMake script.

Run the executable. Ensure shaders (anim_model.vs, anim_model.fs) are in the working directory or specified path.
