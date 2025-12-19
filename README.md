# c-opengl-speedrun-templates
Templates for coding OpenGL speedruns in C

## Repository Setup
### Clone the Repository
```bash
git clone https://github.com/Nzrsc/c-opengl-speedrun-templates.git
cd c-opengl-speedrun-templates
```

### Third-Party Dependencies
The repository includes all necessary third-party libraries:
- third_party/glad/ (OpenGL loader)
- third_party/glfw/ (window/context/input library)
No system-wide installation is required.

# Build Instructions
## Build a Category
```bash
cd <category_folder>
make
./build/bin
```

Replace <category_folder> with the folder name (e.g., 01_triangle).
Each category has its own Makefile but shares third_party/ at the root.

# OpenGL C Speedruns – General Rules

These rules apply to **all categories** in the OpenGL C speedrun repository, providing consistency and guidelines for participants.

---

## Allowed

- **Libraries:**
  - GLFW (window/context/input)
  - GLAD (OpenGL loader)
  - Standard C library
- **Prepared Files:**
  - Empty placeholder files are allowed (e.g., shaders, text files)
  - Prepared Makefiles are allowed and may be used as-is
- **Shaders:**
  - Can be embedded in code or stored in `shaders/` folder
  - Must follow category-specific shader requirements

---

## Window and OpenGL Context
- Resolution may vary, but rendered objects must be clearly visible
- Categories must open a window and render continuously until closed

## Program Behavior

- Programs must terminate gracefully, releasing all resources
- Each category must be self-contained; building one category should not require code from another

---

## Build and Folder Guidelines

- Each category has its own folder with:
  - `src/` – source code
  - `shaders/` – vertex/fragment shaders
  - `build/` – binary output
  - `Makefile` – build instructions
- `third_party/` at the repository root provides GLAD and GLFW
- Use relative paths to include headers and load shaders
- Running `make` in the category folder must produce a working binary in `build/`

---


## Notes

- All categories build on the general rules; additional category-specific rules may override or extend these guidelines
- Using Makefiles is allowed to facilitate rapid setup, but the functional requirements of each category must still be met

# Triangle%

## Category Goal
Render a single triangle on the screen using OpenGL. Completion is achieved when the triangle is visible and the program runs without errors.

## Rules

### Allowed Libraries
- GLFW (window/context/input)
- GLAD (OpenGL loader)
- Standard C library

### Disallowed
- Precompiled shaders
- Prebuilt geometry beyond a single triangle

### Window and Context
- Any resolution is allowed
- Triangle must be fully visible

### Shaders
- Minimum vertex and fragment shaders are required
- Shaders can be embedded in the code or loaded from `shaders/` folder

### Program Behavior
- Opens a GLFW window
- Renders the triangle continuously until window close
- Terminates gracefully, releasing OpenGL resources

## Completion
- Completion occurs once the triangle is rendered correctly
