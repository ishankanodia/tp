# Rubik's Cube Solver

## Overview
This project implements an advanced Rubik's Cube solver using multiple search algorithms, including:
- **BFS (Breadth-First Search)**
- **DFS (Depth-First Search)**
- **IDDFS (Iterative Deepening Depth-First Search)**
- **A*** (A-Star Algorithm)
- **Korf's IDA*** (Iterative Deepening A-Star)

The solver efficiently determines the shortest solution for scrambled Rubik's Cubes by leveraging heuristic optimizations, such as precomputed pattern databases.

---

## Features
- **Multiple Solving Algorithms:** Choose between BFS, DFS, IDDFS, A*, and Korf's IDA* based on the desired tradeoff between speed and memory usage.
- **Heuristic Optimization:** Utilizes pattern databases to improve search efficiency.
- **Scalable Design:** Modular architecture for easy extension and customization.
- **Visualization Support:** (Optional) Model rendering for the cube state.

---

## Prerequisites
- **C++ Compiler**: Ensure you have GCC, Clang, or an equivalent C++ compiler installed.
- **CMake**: Used for build configuration.
- **Standard Libraries**: STL support is required.
- (Optional) **3D Rendering Tools**: For visualizing the Rubik's Cube.

---

## Directory Structure
```
Rubik-Cube-Solver/
├── Databases/              # Precomputed pattern databases for heuristics
├── PatternDatabases/       # Additional patterns used in heuristic optimization
├── Solver/                 # Core solver algorithms
├── Model/                  # 3D visualization models (optional)
├── main.cpp                # Entry point for the project
├── CMakeLists.txt          # Build configuration file
├── README.md               # Documentation
├── .gitignore              # Git ignore rules
├── .git/                   # Git repository metadata
├── .idea/                  # IDE-specific configuration (optional)
```

---

## Installation
### Clone the Repository
```bash
git clone https://github.com/<your-username>/Rubik-Cube-Solver.git
cd Rubik-Cube-Solver
```

### Build the Project
1. Create a build directory:
   ```bash
   mkdir build && cd build
   ```
2. Generate the build files using CMake:
   ```bash
   cmake ..
   ```
3. Compile the project:
   ```bash
   make
   ```

### Run the Solver
After building, execute the solver:
```bash
./RubikCubeSolver
```

---

## Usage
1. Launch the solver and provide the scrambled cube configuration as input.
2. Select the desired solving algorithm from the menu.
3. View the solution steps output in the terminal or the 3D visualization (if enabled).

### Input Format
The cube configuration should be provided as a string, with each face's stickers represented in a fixed order.

---

## Algorithms Explained
### BFS
Breadth-First Search guarantees the shortest solution but requires significant memory for larger states.

### DFS
Depth-First Search explores deep states first, using less memory but is not optimal.

### IDDFS
Iterative Deepening combines the benefits of BFS and DFS, with better memory efficiency.

### A*
A-Star utilizes heuristics to focus the search towards optimal solutions.

### Korf's IDA*
Iterative Deepening A-Star is tailored for Rubik's Cube, combining A*'s heuristic strength with IDDFS's memory efficiency.

---

## Contributions
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch.
3. Commit your changes with clear messages.
4. Submit a pull request.

---

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for more details.

---

## Acknowledgments
- **Korf's Algorithm Research** for inspiring heuristic-based approaches.
- Open-source contributors for their support and collaboration.

---
