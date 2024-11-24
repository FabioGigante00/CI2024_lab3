## CI2024_lab3
 Lab 3 of Computational Intelligence Course in Politecnico di Torino

# Heuristics
| Heuristic                  | Admissible | Consistent |
|----------------------------|------------|------------|
| Hamming                    | Yes        | Yes        |
| Manhattan                  | Yes        | Yes        |
| Linear Conflict Manhattan  | Yes        | No         |

Resolving a conflict can increase temporarily heuristic estimates 
for intermediate nodes

# Puzzle 3x3

All the puzzles were generated using a randomized step of 100_000
I will show results for two fairly different configurations
(Different in computation time and n. of steps)

Configuration 1
```
            2 8 7
            3 6 5
            0 1 4
```


| Algo   | Heuristic                    | Steps   | Cost  |
|--------|------------------------------|---------|-------|
|A*      | Linear Conflict Manhattan    | 108     | 28    |
|A*      | Manhattan                    | 701     | 24    |
|A*      | Hamming                      | 22223   | 24    |
|Dijkstra| None                         | 233947  | 24    |

Configuration 2
```
            8 6 0
            1 7 2
            4 5 3
```

| Algo   | Heuristic                    | Steps   | Cost  |
|--------|------------------------------|---------|-------|
|A*      | Linear Conflict Manhattan    | 30     | 20    |
|A*      | Manhattan                    | 178     | 18    |
|A*      | Hamming                      | 1550    | 18    |
|Dijkstra| None                         | 25062   | 18    |

Cost is higher for Linear Conflict Manhattan cause its not
consistent

# Puzzle 4x4

All the puzzles were generated using a randomized step of 100_000
I will show results for two different configurations
(Different in computation time and n. of steps)

Configuration 1
```
            10 1  13 6
            8  15 4  12
            0  9  2  5
            3  14 11 7
```

I stopped after 1M steps with any algorithm

| Algo   | Heuristic                    | Steps   | Cost  |
|--------|------------------------------|---------|-------|
|A*      | Linear Conflict Manhattan    | 13298   | 64    |
|A*      | Manhattan                    | None    | None  |
|A*      | Hamming                      | None    | None  |
|Dijkstra| None                         | None    | None  |

Configuration 2
```
            11 6  14 13
            4  3  15 2
            9  10 0  5
            8  1  7  12
```


| Algo   | Heuristic                    | Steps   | Cost  |
|--------|------------------------------|---------|-------|
|A*      | Linear Conflict Manhattan    | 809256  | 72    |

### Solution Steps

```
(2, 2) -> (1, 2) -> (0, 2) -> (0, 1) -> (1, 1) -> (1, 0) -> (0, 0) -> (0, 1) -> (1, 1) -> (1, 0) -> (2, 0) -> (2, 1) -> (3, 1) -> (3, 2) -> (2, 2) -> (1, 2) -> (1, 1) -> (2, 1) -> (3, 1) -> (3, 0) -> (2, 0) -> (1, 0) -> (1, 1) -> (2, 1) -> (2, 2) -> (2, 3) -> (3, 3) -> (3, 2) -> (3, 1) -> (2, 1) -> (2, 2) -> (3, 2) -> (3, 3) -> (2, 3) -> (2, 2) -> (1, 2) -> (1, 3) -> (0, 3) -> (0, 2) -> (0, 1) -> (0, 0) -> (1, 0) -> (2, 0) -> (2, 1) -> (1, 1) -> (1, 2) -> (1, 3) -> (0, 3) -> (0, 2) -> (0, 1) -> (1, 1) -> (1, 2) -> (1, 3) -> (2, 3) -> (2, 2) -> (2, 1) -> (1, 1) -> (1, 0) -> (2, 0) -> (2, 1) -> (1, 1) -> (1, 2) -> (2, 2) -> (2, 3) -> (3, 3) -> (3, 2) -> (3, 1) -> (3, 0) -> (2, 0) -> (2, 1) -> (3, 1) -> (3, 2) -> (3, 3)
```

Configuration created with 400 steps
```
  8  2  0  14
  10 13 11 1
  9  12 15 7
  6  5  4  3
 ```

| Algo   | Heuristic                    | Steps   | Cost  |
|--------|------------------------------|---------|-------|
|A*      | Linear Conflict Manhattan    | 102205  | 72    |

Steps really depend on configuration, even with same 
randomized steps great variation
