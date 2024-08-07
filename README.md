# Procedural Dungeon Generation

This project implements a procedural dungeon generation system using Python and Pygame. The system generates a dungeon layout composed of rooms connected by hallways, ensuring a coherent and playable structure.

![image](https://github.com/user-attachments/assets/bcbf28b5-fe5a-4c8f-959c-ca5821b8f88d)

## Features

- **Random Room Generation:** Generates rooms of random sizes and positions within a predefined grid.
- **Room Collision Handling:** Ensures rooms do not overlap and adjust positions accordingly.
- **Main Room Identification:** Selects main rooms that will be focal points in the dungeon.
- **Void Filling:** Identifies and fills void spaces in the dungeon layout.
- **Neighbor Identification:** Finds and connects neighboring rooms with hallways.

## Files

### `Dungeon.py`
Contains the core classes and functions for dungeon and room management.

- **Classes:**
  - `Dungeon`: Manages the overall dungeon structure and generation process.
  - `Room`: Represents individual rooms within the dungeon.
- **Functions:**
  - `roundm(n, m)`: Rounds a number to the nearest multiple of `m`.
  - `slope(p0, p1)`: Calculates the slope between two points.
  - `collide_rooms(left, right)`: Checks for collisions between rooms.
  - `collide_and_scatter_rooms(left, right)`: Handles room collisions and applies repulsion.
  - `gridToScreen(count, spacing)`: Converts grid coordinates to screen coordinates.
  - `screenToGrid(coord, spacing)`: Converts screen coordinates to grid coordinates.
  - `collide_with_voids(left, right)`: Checks for collisions with void spaces.
  - `snap_rect_to_grid(rect, gridSpacing)`: Snaps a rectangle to the grid.

### `Generate.py`
Implements the game states and controls the dungeon generation process.

- **Classes:**
  - `GameMode`: Base class for game states.
  - `InitializationMode`, `AddRoomsMode`, `CollideRoomsMode`, `IdentifyMainRoomsMode`, `FillVoidsMode`, `MainRoomNeighborsMode`, `LocateHallwaysMode`: Specific game modes for different stages of dungeon generation.
  - `Game`: Manages the overall game state and runs the game loop.
- **Controls:**
  - `QUIT`: Exit the game.
  - `K_ESCAPE`: Exit the game.
  - `K_SPACE`: Progress through the game states.
  - `K_r`: Reset the dungeon generation process.

### `StateMachine.py`
Provides the state machine framework used to manage game states.

- **Classes:**
  - `State`: Base class for individual states.
  - `StateMachine`: Manages transitions between different states.

## Dependencies

- `pygame`: The Pygame library is used for rendering and handling input events.


