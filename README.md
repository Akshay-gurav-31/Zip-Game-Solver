# Zip Creator — Twin Box Precision

A fast, interactive web-based creator and solver for **LinkedIn Zip** puzzles. Place numbers on a grid, optionally add walls, and instantly compute all valid Hamiltonian paths that connect the numbers in sequential order while filling every cell exactly once.

## Overview

Zip Creator allows you to:
- Create custom Zip puzzles of any size from 3×3 to 9×9.
- Place numbered waypoints (1, 2, 3, …) that must be visited in order.
- Add horizontal or vertical walls to increase difficulty.
- Solve the puzzle and explore all valid solutions (up to 50 shown).
- Visualize each solution with smooth animated path tracing and timing.

Perfect for puzzle enthusiasts, developers learning backtracking algorithms, or anyone who enjoys LinkedIn’s daily Zip challenge.

## Features

- Real-time grid editor (numbers + walls)
- Dual edit modes: Numbers and Walls
- High-performance DFS solver with isolation pruning and heuristic ordering
- Multiple solution browser with navigation
- Canvas-based path animation with dynamic coloring
- Dark / Light theme with glassmorphic UI
- Fully responsive (desktop + mobile)
- Single-file HTML – no build step required

## How It Works

1. Choose grid size (3–9).
2. Tap cells to place numbers sequentially (1, 2, 3, …).
3. Switch to Wall mode and click near edges to place barriers.
4. Click **Solve All** to find every valid path.
5. Browse solutions and watch the animated trace.

The solver guarantees that every returned path:
- Visits every cell exactly once.
- Passes through the numbers in ascending order.
- Never crosses a wall.

## Algorithm

The core solver implements a **depth-first search** for Hamiltonian paths on a grid graph with the following constraints and optimizations:

- **Graph representation**: 4-connected grid with dynamic edge removal for walls.
- **Backtracking** with visited-set pruning.
- **Number-order enforcement** during traversal.
- **Isolation detection** (BFS on remaining cells) – instantly rejects branches that disconnect the unvisited area.
- **Manhattan-distance heuristic** to prioritize moves toward the next numbered cell.
- Early termination after 50 solutions for UI performance.

Full implementation is contained in the `ZipSolver` class (see `script` section of `index.html`).

## Tech Stack

- HTML5 + Tailwind CSS (via CDN)
- React 18 (UMD build)
- Vanilla JavaScript + Canvas 2D
- Babel standalone for JSX
- Font Awesome icons

No external dependencies or build tools required.

## Installation & Usage

1. Download or clone the repository.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).
3. No installation or server required – works completely offline.

**Hosting (optional)**  
You can host it instantly on GitHub Pages, Vercel, or Netlify by uploading the single `index.html` file.

## Developer

**Akshay Gurav**  
Software Engineer & Puzzle Enthusiast

- LinkedIn: [linkedin.com/in/akshay---gurav](https://www.linkedin.com/in/akshay---gurav/)
- GitHub: [github.com/Akshay-gurav-31](https://github.com/Akshay-gurav-31)

## License

MIT License – feel free to use, modify, and distribute.

---

Made with precision for puzzle lovers.
