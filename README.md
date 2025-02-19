# Pathfinding Visualizer in Python

<img src="https://github.com/user-attachments/assets/e58dcee1-5fab-4ca2-839c-7f0ca5962045" alt="ezgif com-video-to-gif-converter" width="300" />


A simple pathfinding visualizer built using Python and Pygame. This project demonstrates the A* algorithm in action by visually showing how the shortest path is found on a grid. Users can interactively set the start point, end point, and obstacles (barriers) while watching the algorithm work in real time. 

Youtube Video:
https://www.youtube.com/watch?v=O0MvdhQdj6I&t=6s

## Features

- **Interactive Grid:**  
  - Set start and end nodes.
  - Place barriers by clicking.
  - Reset nodes with a right-click.
- **A\* Algorithm Visualization:**  
  - Visual feedback for nodes being considered (open/closed).
  - Path reconstruction once the goal is reached.
- **Modular Codebase:**  
  - Organized into separate files for better readability and maintenance.

## Project Structure

```
Pathfinding_Visualiser/
├── main.py         # Main file to run the visualizer and handle UI events
├── spot.py         # Contains the Spot class representing each cell in the grid
└── algorithm.py    # Implements the A* pathfinding algorithm
```

## Prerequisites

- Python 3.x
- [Pygame](https://www.pygame.org/)  
  Install Pygame using pip:

  ```bash
  pip install pygame
  ```

## Getting Started

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/EgemenErin/Pathfinding_Visualizer.git
   cd Pathfinding-Visualizer
   ```

2. **Run the Visualizer:**

   ```bash
   python main.py
   ```

## How to Use

- **Left-click** to set the start node (orange), end node (turquoise), and barriers (black).
- **Right-click** to reset a cell.
- Press **Spacebar** to run the A* algorithm.
- Press **C** to clear the grid and start over.

## Code Overview

### `spot.py`

Defines the `Spot` class which represents each cell in the grid. It handles:
- **State Management:** Methods to mark a spot as start, end, barrier, open, closed, or part of the final path.
- **Drawing:** Rendering the spot on the Pygame window.
- **Neighbor Updates:** Determining adjacent spots that are not barriers for the algorithm.

### `algorithm.py`

Implements the A* pathfinding algorithm:
- **Heuristic Function (`h`):** Calculates the Manhattan distance between two points.
- **Path Reconstruction (`reconstruct_path`):** Traces back from the end node to the start node to visualize the shortest path.
- **A\* Algorithm (`a_star_algorithm`):** Uses a PriorityQueue to explore nodes, updating scores and paths until the goal is reached.

### `main.py`

Serves as the entry point and ties the modules together:
- **Setup:** Initializes the Pygame window and grid.
- **Event Handling:** Processes mouse and keyboard inputs to set nodes and run the algorithm.
- **Rendering:** Continuously draws the grid, updates the display, and handles user interactions.

## Contributing

Contributions are welcome! If you have ideas for improvements or bug fixes, please submit a pull request or open an issue.

## License

This project is open source and available under the [MIT License](LICENSE).

---
