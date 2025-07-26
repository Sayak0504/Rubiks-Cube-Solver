# C++ Rubik's Cube Solver

This project is a high-performance, command-line-based Rubik's Cube solver written in C++. It can generate a random scramble for a 3x3x3 cube and then find an optimal solution using the IDA* (Iterative Deepening A-Star) search algorithm, guided by pattern databases.

## Features

Multiple Cube Representations: Includes several internal models of the Rubik's Cube for efficiency and testing, including a highly optimized bitboard representation.

IDA* Search Algorithm: Employs the powerful IDA* algorithm to find solutions quickly.

Pattern Databases: Uses pre-calculated pattern databases (specifically, a corner pattern database) to provide an accurate heuristic, significantly speeding up the search for a solution.

Cross-Platform Build System: Uses CMake to manage the build process, allowing it to be compiled on various operating systems.

## Requirements
To build and run this project, you will need a C++ development environment.

C++ Compiler: A modern C++ compiler that supports C++14 (e.g., GCC/g++, Clang).

CMake: Version 3.5 or higher.

Build Tool: A build tool like Ninja or make.

(Windows Users) It is highly recommended to use MSYS2 with the UCRT64 environment to install the required toolchain (gcc, cmake, ninja).

## Build and Run Instructions

These instructions will guide you through compiling and running the project from the command line.

1. Compilation Steps
Open your terminal.

Windows Users: Open the MSYS2 UCRT64 terminal.

Linux/macOS Users: Open your standard terminal.

Clone the repository 
   ```bash
   git clone https://github.com/Sayak0504/Rubiks-Cube-Solver.git
   ```

```Bash

cd /path/to/your/project/rubiks-cube-solving
Create and enter a build directory. This keeps the compiled files separate from the source code.
```

```Bash

mkdir build
cd build
Run CMake to generate the build files. This command points to the CMakeLists.txt file in the parent directory.
```

```Bash

cmake ..
Compile the project. If you are using the recommended MSYS2 setup, ninja will be used. Otherwise, make may be the default.
```

```Bash

ninja
(If ninja is not found, try make)
```

2. Run the Solver
After a successful compilation, an executable file will be created in your build directory.

Run the program:

```Bash

./rubiks_cube_solving.exe
```
The program will output the state of a randomly scrambled cube, the list of moves used to scramble it, and will then begin the solving process. Once a solution is found, it will print the solved state and the moves required to solve it.

Note: Solving complex scrambles can be computationally intensive and may take some time. For quicker testing, you can reduce the number of scramble moves in main.cpp.
