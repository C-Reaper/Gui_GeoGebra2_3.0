## Overview
The project appears to be a basic C application for a GUI-based tool called "GeoGebra 2.3". The application is designed to interpret and execute custom language commands, allowing users to perform various mathematical and geometric operations.

## Features
- Custom language interpretation and execution
- Graphical user interface (GUI) for command input/output
- Supports basic mathematical and geometric operations

## Project Structure
- `src/`: Contains the source code, including `Main.c` as the entry point.
- `Makefile.linux`, `Makefile.windows`, `Makefile.wine`, `Makefile.web`: Makefiles for building the project on Linux, Windows, Wine (Linux cross-compilation for Windows), and Emscripten (WebAssembly) environments.

### Prerequisites
- C/C++ Compiler and Debugger (GCC or Clang)
- Make utility
- Standard development tools
- Libraries needed:
  - `X11` for GUI rendering on Linux
  - `png`, `jpeg` libraries for image handling

## Build & Run
The project uses Makefiles to manage the build process. Here are the basic steps:

### Building
To build the project for a specific operating system, use the following command:
```sh
make -f Makefile.(os) all
```
Replace `(os)` with `linux`, `windows`, `wine`, or `web` depending on your target platform.

#### Clean and Rebuild
For a clean rebuild (removing previous build artifacts):
```sh
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

### Executing
To execute the built application:
```sh
make -f Makefile.(os) exe
```
This will compile and run the application.

### Clean Build
To clean up build artifacts:
```sh
make -f Makefile.(os) clean
```

## Note
The project structure includes specific Makefiles for different environments, ensuring that the correct settings are applied for each platform.