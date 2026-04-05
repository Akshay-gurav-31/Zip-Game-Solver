# Zip Creator — Twin Box Precision

A fast, interactive web-based creator and solver for LinkedIn Zip puzzles. It allows users to design custom grids, add constraints, and instantly compute all valid Hamiltonian paths that visit every cell exactly once while following numbered waypoints.

---

## Overview

Zip Creator enables you to:

- Create custom puzzles from 3×3 to 9×9 grids  
- Place numbered waypoints (1, 2, 3, …) in sequence  
- Add horizontal and vertical walls as constraints  
- Solve puzzles and explore multiple valid solutions  
- Visualize paths with smooth animated rendering  

This project is useful for puzzle enthusiasts and developers exploring constraint-based problem solving.

---

## Quick Access

<p align="center">
  <strong>Scan to try Zip Creator instantly</strong><br/><br/>
  <img src="https://raw.githubusercontent.com/Akshay-gurav-31/Zip-Game-Solver/main/scan-me.png" width="260" />
</p>

---

## Features

- Interactive grid editor (numbers and walls)  
- Dual edit modes for precise control  
- High-performance DFS-based solver  
- Multiple solution viewer with navigation  
- Canvas-based animated path visualization  
- Dark and light theme support  
- Fully responsive (desktop and mobile)  
- Runs completely offline  

---

## Architecture

The entire application is implemented inside a single `index.html` file.

- No build tools  
- No backend  
- No installation required  

Everything — UI, logic, and solver — runs directly in the browser.

---

## Tech Stack

- HTML5  
- CSS3 (custom styling + theming)  
- JavaScript (ES6+)  
- React 18 (UMD via CDN)  
- Tailwind CSS (CDN)  
- Babel Standalone (for JSX transpilation)  
- Canvas API (for path rendering)  

---

## How It Works

1. Select a grid size (3–9)  
2. Place numbers sequentially on the grid  
3. Add walls to restrict movement  
4. Click Solve All  
5. Explore and animate solutions  

Each solution:

- Visits every cell exactly once  
- Follows numbered cells in order  
- Respects all wall constraints  

---

## Algorithm

The solver is based on Depth-First Search (DFS) with backtracking and optimizations:

- Grid modeled as a 4-directional graph  
- Visited-state pruning  
- Number-order enforcement  
- Isolation detection using BFS  
- Manhattan-distance heuristic for move ordering  
- Early stopping after 50 solutions  

These optimizations ensure fast execution even for complex grids.

---

## Purpose

This project was built to explore how rule-based systems and algorithms solve constrained problems.

The goal is not to bypass puzzles, but to:

- Understand algorithmic thinking  
- Analyze solution strategies  
- Experiment with optimization techniques  

---

## Installation & Usage

1. Clone or download the repository  
2. Open `index.html` in any modern browser  
3. Start creating and solving puzzles  

No setup required.

---

## Developer

Akshay Gurav  

- LinkedIn: https://www.linkedin.com/in/akshay---gurav/  
- GitHub: https://github.com/Akshay-gurav-31  

---

## License

MIT License — free to use, modify, and distribute.

---

Built for precision and problem-solving.
