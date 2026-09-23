# 2048 in Java

My programming project — the 2048 sliding-tile game, built in my first-year Data Structures course.

The course provided the starter framework (the text/graphical drivers and the standard I/O & drawing libraries).
**My work is the game logic in [`src/game/Board.java`](src/game/Board.java):**

- `updateOpenSpaces()` – finds every empty cell on the board
- `addRandomTile()` – drops a new tile in a random empty cell (90% a 2, 10% a 4)
- `swipeLeft()` / `mergeLeft()` – slides tiles and merges equal neighbors
- `transpose()` / `flipRows()` – rotate the 2D array so every direction reuses the "left" logic
- `makeMove()` – combines the above to move Up, Down, Left, or Right
- `isGameLost()` – ends the game when the board is full and no merges are left

## How to run

Requires Java (JDK 11 or newer). From the project folder:

```bash
javac -d bin src/game/*.java

# Graphical version (window opens)
java -cp bin game.AnimatedDriver

# Terminal version
java -cp bin game.TextDriver
```

Choose **2. Play full game**, then use **W A S D** to move and **Q** to quit
(in the terminal version, press Enter after each key).
Choose **1. Test individual methods** to try each method on the sample boards in `input*.in`.
