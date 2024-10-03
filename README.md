# BattleShip

## Contents

[Objective](#objective)  
[Game Development](#game-development)  
[Example of Board](#example-of-board)  
[Scoring](#scoring)  
[Notes](#notes)

### Objective

Write a Python program that allows playing **BATTLESHIP**.

### Game Development

- **Only one player** plays with a randomly generated `board`.
- This initial board (`board`) will have a size of 10x10 (as a list of lists) where each cell can be:
  - **Empty**, represented by an empty string.
  - **Ship**, represented by a combination of letter + digit.
- The following ships will be present:
  - 1 ship of length 5 (`5A`)
  - 1 ship of length 4 (`4A`)
  - 2 ships of length 3 (`3A` and `3B`)
  - 1 ship of length 2 (`2A`)
- In each "turn," the player must specify the shooting position: `A4`, `B7`, `C1`, ... where the letters represent rows and the numbers represent columns.
- Shooting at a cell that is already occupied or outside the board is not allowed.
- In each "turn," the board with the attempted shots must be displayed:
  - **Unexplored cell** represented by ⬛
  - **Missed shot (water)** represented by 🟦
  - **Hit ship** represented by 🟧
  - **Sunk ship** represented by 🟥
- Each turn must show:
  - Number of turns.
  - Number of ships left to sink.
  - Score so far.
- The game ends when all ships have been sunk.

### Example of Board

The initial board shows the location of each ship and their identifiers. Here's an example:

```
██ ██ ██ ██ ██ ██ ██ ██ ██ ██
██ ██ ██ ██ ██ ██ ██ ██ ██ ██
██ ██ ██ ██ ██ ██ ██ ██ ██ 5A
██ ██ ██ ██ 3B 3B 3B ██ ██ 5A
██ ██ ██ ██ 4A ██ ██ ██ ██ 5A
██ ██ 3A ██ 4A ██ ██ ██ ██ 5A
██ ██ 3A ██ 4A ██ ██ ██ ██ 5A
██ ██ 3A ██ 4A ██ ██ ██ ██ ██
██ ██ ██ 2A ██ ██ ██ ██ ██ ██
██ ██ ██ 2A ██ ██ ██ ██ ██ ██
```

### Scoring

| Move             | Score                  |
| ---------------- | ---------------------- |
| MISS (WATER)     | -1                     |
| HIT              | 2 \* Ship's Length      |
| HIT AND SUNK     | 4 \* Ship's Length      |

> 💡 The "global" score cannot be less than zero.

### Notes

- Only use Python tools that have been covered in class so far.