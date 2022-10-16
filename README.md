# OpenGL C++ Template

## Libraries used

- [glad](https://glad.dav1d.de/)
- [glfw](https://github.com/glfw/glfw)
- [glm](https://github.com/g-truc/glm)

## Building

### Prequisites

- Compiler (MSVC, MinGW, gcc/g++, etc)
- CMake
- git

First, make sure you recursively clone the repository using git. This is so that you will also clone the glfw and glm submodules.

```bash
git clone --recursive https://https://github.com/piigle/opengl-template.git
```

Then create a directory called build:

```bash
cd opengl-template
mkdir build
cd build
```

Specify the generator for CMake. Do "cmake -G" for a list of possible generators.

```bash
cmake -G "Visual Studio 17 2022" .. 
```

Build

```bash
cmake --build .
```

When running the executable, make sure to run it from the root of the project so that the exeuctable will have access to the shaders directory.
