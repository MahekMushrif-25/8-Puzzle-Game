# 8-Puzzle Game Solver

This project is an interactive web-based 8-puzzle game that allows users to solve a sliding puzzle using images. It includes an option to solve the puzzle automatically using the Breadth-First Search (BFS) algorithm.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Technologies Used](#technologies-used)
- [License](#license)

## Overview
The 8-puzzle game is a classic sliding puzzle where the goal is to arrange tiles in numerical order or to complete an image by sliding them into an empty space. This project allows you to select an image set and start the puzzle game in your browser. You can solve the puzzle manually or let the BFS algorithm find the solution path automatically.

## Features
- **Interactive gameplay**: Slide tiles to solve the puzzle manually.
- **Automatic solving**: Uses the BFS algorithm to solve the puzzle and display the solution path.
- **Image set selection**: Choose from different image sets to use as the puzzle background.
- **Responsive design**: Works on mobile and desktop browsers.

## Demo
To see a live demo, follow these steps:
1. Clone this repository.
2. Open `index.html` in your preferred web browser.

## Installation
Clone the repository using the following command:
```bash
git clone https://github.com/yourusername/8-puzzle-game-solver.git
cd 8-puzzle-game-solver


## Usage
1. Open `index.html` in a web browser.
2. Select an image set to start the puzzle.
3. Manually solve the puzzle by clicking on tiles adjacent to the empty space.
4. Use the “Solve” button to trigger the BFS algorithm and display the solution.

## How It Works

### Code Overview
The core game functionality is contained in `puzzle.html` and is powered by JavaScript. Here’s a breakdown of key functions:

- **Rendering the Puzzle (`renderBoard`)**: This function creates the visual grid for the puzzle. It dynamically sets each tile’s background image based on the selected image set. Empty spaces are styled separately.
- **Tile Movement (`moveTile`)**: Handles user input for sliding a tile by checking if the clicked tile is adjacent to the empty tile.
- **Automatic Solving with BFS (`bfs`)**:
  - **Initial Setup**: A queue is initialized with the starting board configuration.
  - **State Tracking**: A `visited` set stores unique board configurations to prevent revisiting the same layout.
  - **Exploring Moves**: Possible moves from the empty tile’s position are checked, and new configurations are added to the queue if unvisited.
  - **Checking for Solution**: Each new configuration is compared with the goal state. If a match is found, the solution path is returned.

### Logic Explanation
The BFS algorithm works by systematically exploring each possible tile configuration starting from the initial state, ensuring the shortest path to the solution. Each layout (or "state") of the board is saved as a JSON string in a `Set` called `visited` to avoid revisits and loops.

## Technologies Used
- **HTML/CSS**: For structuring and styling the web interface.
- **JavaScript**: Core functionality, including game logic and BFS for solving the puzzle.
- **JSON**: Used for converting the board configuration to a string format to enable unique comparisons in the BFS algorithm.

## License
This project is open-source and available under the MIT License.
```
