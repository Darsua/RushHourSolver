# Java Rush Hour Puzzle Solver

![](test/example.gif)

A Java-based solver for Rush Hour puzzle configurations utilizing graph search algorithms and admissible heuristics. Built for IF2211 (Algorithm Strategy) at STEI ITB.

---

## Features

- Search algorithms: Greedy Best-First Search (GBFS), Uniform Cost Search (UCS), and A* Search
- Heuristic functions: `BLOCKING_PIECES`, `EXIT_DISTANCE`, and `BLOCKING_DISTANCE`
- Configurable puzzle board parsing from structured text files
- Step-by-step ASCII solution replay in the console

---

## Getting Started

### Option 1: Run with Pre-Built JAR
```bash
java -jar bin/Rush.jar <file> <algorithm> [heuristic]
```

### Option 2: Compile and Run from Source
```bash
javac -d out src/**/*.java
java -cp out Main <file> <algorithm> [heuristic]
```

- `<file>`: Path to puzzle input file (e.g. `puzzles/level1.txt`)
- `<algorithm>`: `GBFS`, `UCS`, or `A_STAR`
- `[heuristic]`: (Optional for A*) `BLOCKING_PIECES`, `EXIT_DISTANCE`, or `BLOCKING_DISTANCE`

**Example:**
```bash
java -jar bin/Rush.jar puzzles/level1.txt A_STAR BLOCKING_DISTANCE
```

---

## Input File Format

```text
6 6
12
AAB..F
..BCDF
GPPCDFK
GH.III
GHJ...
LLJMM.
```
- Line 1: Dimensions `<rows> <cols>`
- Line 2: Number of blocking pieces
- Remaining lines: Board layout with single-letter piece identifiers (`K` indicates exit target)

---

## Author

Darrel Adinarya Sunanda `13523061` — [@Darsua](https://github.com/Darsua)

---

## License

MIT
