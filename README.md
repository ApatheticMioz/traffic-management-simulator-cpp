# Traffic Management Simulator

A C++ simulation system for urban traffic flow optimization using advanced data structures and algorithms.

**Status:** Archived / Refactored

## Description

The Traffic Management Simulator replicates and optimizes real-world urban traffic flow. It models a city's road network as a weighted, directed graph and provides dynamic vehicle routing, real-time traffic signal control, congestion management, and emergency vehicle handling.

## Features

- **City Traffic Network** — Weighted directed graph modeling intersections and roads
- **Vehicle Routing** — Dijkstra's Algorithm for optimal path calculation
- **Traffic Signal Management** — Priority queue-based signal timing optimization
- **Congestion Monitoring** — BFS/DFS-based traffic analysis and rerouting
- **Emergency Vehicle Handling** — Priority routing with signal override
- **Road Closure Simulation** — Dynamic disruption handling and rerouting

## Project Structure

```
traffic-management-simulator-cpp/
├── main.cpp           # Entry point and simulation driver
├── Graph.cpp          # Graph representation with adjacency lists, BFS, DFS
├── Dijkstra.cpp       # Shortest path algorithm implementation
├── HashTable.cpp      # Hash table for congestion tracking
├── MinHeap.cpp        # Min-heap data structure
├── PriorityQueue.cpp  # Priority queue implementation
├── ParseFiles.cpp     # CSV file parsing for simulation data
├── Vector.cpp         # Custom dynamic array implementation
├── List.cpp           # Linked list implementation
├── Queue.cpp          # Queue data structure
├── Stack.cpp          # Stack data structure
├── examples/          # Sample CSV data files
├── LICENSE            # MIT License
├── CONTRIBUTING.md    # Contribution guidelines
├── CHANGELOG.md       # Version history
└── README.md          # This file
```

## Requirements

- C++ compiler with C++11 support (g++, clang++, MSVC)
- Standard C++ library

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ApatheticMioz/traffic-management-simulator-cpp.git
   cd traffic-management-simulator-cpp
   ```

2. **Compile:**
   ```bash
   g++ -std=c++11 -Wall -o traffic_simulator main.cpp
   ```
   > Note: main.cpp includes all other source files via `#include` directives, so only main.cpp needs to be compiled.

## Usage

1. **Prepare CSV data files** in the project directory (see `examples/` for sample files):
   - `road_network.csv` — Road connections (Intersection1, Intersection2, TravelTime)
   - `vehicles.csv` — Vehicle data (VehicleID, StartIntersection, EndIntersection)
   - `traffic_signals.csv` — Signal timings (Intersection, GreenTime)
   - `road_closures.csv` — Blocked roads (Intersection1, Intersection2, Status)
   - `emergency_vehicles.csv` — Emergency vehicles (VehicleID, Start, End, Priority)

   To use the example files:
   ```bash
   cp examples/*.csv .
   ```

2. **Run the simulator:**
   ```bash
   ./traffic_simulator
   ```

## Data Structures & Algorithms

| Component | Implementation | Purpose |
|-----------|---------------|---------|
| Graph | Adjacency Lists | Road network representation |
| Dijkstra's Algorithm | Min-Heap optimized | Shortest path routing |
| Hash Table | Random probing | Vehicle count tracking |
| BFS/DFS | Stack/Queue-based | Congestion detection |
| Priority Queue | Heap-based | Signal timing management |

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.
