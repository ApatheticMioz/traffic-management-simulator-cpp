# DS-Project

# Smart Traffic Management System Simulator

## Introduction

The Smart Traffic Management System Simulator is designed to replicate and optimize real-world urban traffic flow using advanced data structures and algorithms. This system focuses on efficient traffic management, incorporating features such as dynamic vehicle routing, real-time traffic signal control, congestion management, and emergency vehicle handling. The goal is to simulate and improve traffic conditions in a city, ensuring smoother traffic flow and better management of road disruptions.

Key features of the system include:

-   A **City Traffic Network** represented as a weighted, directed graph, modeling intersections and roads.
-   A **Vehicle Routing System** powered by Dijkstra's Algorithm to find optimal routes dynamically.
-   **Traffic Signal Management** using priority queues for adjusting signal timings based on congestion.
-   **Congestion Monitoring** and rerouting using BFS/DFS to alleviate traffic jams.
-   **Emergency Vehicle Handling** with special routing to clear paths for urgent vehicles.
-   **Accident and Road Closure Simulation** to handle disruptions in the road network.
-   A **Simulation Dashboard** to visualize and control the system in real-time.

This simulator is built using C++ and leverages various data structures like graphs, priority queues, and heaps for efficient traffic management and optimization.

## Features

### 1. **City Traffic Network**

-   Represented as a weighted, directed graph where:
    -   **Nodes**: Intersections.
    -   **Edges**: Roads between intersections, with weights representing travel times or congestion levels.
-   Supports dynamic addition and removal of roads or intersections.
-   Can visualize the graph structure in a text-based or graphical form.

### 2. **Vehicle Routing System**

-   Calculates the shortest or fastest route for vehicles dynamically.
-   Uses **Dijkstra’s Algorithm** to find the optimal path.
-   Recalculates routes dynamically based on changes in traffic conditions.
-   Tracks vehicle movement across the network.

### 3. **Traffic Signal Management**

-   Controls traffic lights at intersections to minimize congestion.
-   Uses a **priority queue** to manage incoming roads based on vehicle density.
-   Dynamically adjusts green signal durations to reduce wait times.
-   Includes an emergency override system for critical situations.

### 4. **Congestion Monitoring**

-   Monitors vehicle counts on each road segment.
-   Identifies congested roads and reroutes traffic using **BFS** or **DFS**.
-   Displays congestion levels for analysis.

### 5. **Emergency Vehicle Handling**

-   Provides special routing for emergency vehicles to minimize delays.
-   Overrides normal traffic signal operations to clear paths.
-   Uses an **A\* Algorithm** (mentioned as a feature, ensure implementation exists) to find the fastest possible route.
-   Restores normal traffic flow once the emergency vehicle has passed.

### 6. **Accident and Road Closure Simulation**

-   Simulates disruptions such as road closures or accidents.
-   Blocks specific roads or intersections dynamically.
-   Recalculates affected vehicle routes and updates the traffic network.
-   Monitors system performance during disruptions.

### 7. **Simulation Dashboard**

-   Provides an interactive interface to visualize and control the simulation.
-   Displays traffic flow, congestion levels, and signal statuses.
-   Allows manual addition or removal of vehicles.
-   Generates logs for all system actions, including rerouting and signal changes.

## Data Structures and Algorithms

-   **Graph**: Represents the city's road network with adjacency lists (`Graph.h`).
-   **Priority Queue**: Manages road order for signal adjustments (`PriorityQueue.cpp`).
-   **Min-Heap**: Efficiently identifies roads with the highest congestion or used in Dijkstra's (`Minheap.cpp`).
-   **Hash Table**: Tracks real-time vehicle counts on roads (`HashTable.cpp`).
-   **Dijkstra’s Algorithm**: Finds shortest paths for vehicles (`Dijkstra.cpp`).
-   **A\* Algorithm**: Handles emergency vehicle routing (Mentioned in features).
-   **BFS/DFS**: Detects congestion or inaccessible paths (Used in Graph class `Graph.cpp`).
-   **Other Structures:** LinkedList (`List.cpp`), Queue (`Queue.cpp`), Stack (`Stack.cpp`), Vector (`Vector.cpp`).

### Code Component Details:

*(Details for Graph.cpp, Dijkstra.cpp, HashTable.cpp, List.cpp, Minheap.cpp, ParseFiles.cpp, PriorityQueue.cpp, Queue.cpp, Stack.cpp, Vector.cpp)*

## Requirements

-   **Programming Language**: C++ (likely C++11 or newer)

## Setup and Compilation

1.  **Clone:** `git clone https://github.com/ApatheticMioz/traffic-management-simulator-cpp.git`
2.  **Compile:** (Example using g++, adjust based on your file structure and dependencies)
    ```bash
    g++ main.cpp game.cpp Dijkstra.cpp HashTable.cpp ParseFiles.cpp *.cpp -o traffic_simulator -std=c++11
    ```

## How to Run
```bash
./traffic_simulator
```

Follow simulation prompts.
