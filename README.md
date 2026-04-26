# Project README

## Overview
- This project is a C application that compiles and runs custom languages like `.alxml`. It supports building for multiple platforms (Linux, Windows, Wine, WebAssembly) using different compilers and build systems.

## Features
- Compilation and execution of `.alxml` scripts.
- Cross-platform compilation using GCC, Clang, and MinGW-w64.
- Support for debugging on Linux using GDB.

## Project Structure
```
<Project>/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── ComponentDefines.h  # Header file for custom token definitions
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects (example given WINAPI, X11, ALSA)

## Build & Run
### Linux
- **Build Process**:
  ```sh
  cd <Project>
  make -f Makefile.linux all
  ```
- **Clean Rebuild**:
  ```sh
  make -f Makefile.linux clean
  make -f Makefile.linux all
  ```
- **Execute**:
  ```sh
  make -f Makefile.linux exe
  ```

### Windows
- **Build Process**:
  ```sh
  cd <Project>
  make -f Makefile.windows all
  ```
- **Clean Rebuild**:
  ```sh
  make -f Makefile.windows clean
  make -f Makefile.windows all
  ```
- **Execute**:
  ```sh
  make -f Makefile.windows exe
  ```

### Wine (Linux Cross Compile for Windows)
- **Build Process**:
  ```sh
  cd <Project>
  make -f Makefile.wine all
  ```
- **Clean Rebuild**:
  ```sh
  make -f Makefile.wine clean
  make -f Makefile.wine all
  ```
- **Execute**:
  ```sh
  make -f Makefile.wine exe
  ```

### WebAssembly (Emscripten or wasmtime)
- **Build Process**:
  ```sh
  cd <Project>
  make -f Makefile.web all
  ```
- **Clean Rebuild**:
  ```sh
  make -f Makefile.web clean
  make -f Makefile.web all
  ```
- **Execute**:
  ```sh
  make -f Makefile.web exe
  ```

This README provides a comprehensive guide to building and running the project on different platforms.