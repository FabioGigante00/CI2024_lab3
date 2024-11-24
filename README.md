## CI2024_lab3
 Lab 3 of Computational Intelligence Course in Politecnico di Torino

All the puzzles were generated using a randomized step of 100_000
I will show results for two fairly different configurations

# Heuristics
| Heuristic                  | Admissible | Consistent |
|----------------------------|------------|------------|
| Hamming                    | Yes        | Yes        |
| Manhattan                  | Yes        | Yes        |
| Linear Conflict Manhattan  | Yes        | No         |

Resolving a conflict can increase temporarily heuristic estimates 
for intermediate nodes

# Puzzle 3x3

Configuration 1
```
            2 8 7
            3 6 5
            0 1 4
```


| Algo   | Heuristic                    | Steps   | Cost  |
|--------|------------------------------|---------|-------|
|A*      | Linear Conflict Manhattan    | 93243   | 24    |
|A*      | Manhattan                    | 240353  | 24    |
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
|A*      | Linear Conflict Manhattan    | 16068   | 20    |
|A*      | Manhattan                    | 30093   | 18    |
|A*      | Hamming                      | 1550    | 18    |
|Dijkstra| None                         | 25062   | 18    |

Cost is higher for Linear Conflict Manhattan cause its not
consistent

