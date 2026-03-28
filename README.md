# Flight Route Optimization: Shortest Path Analysis

## 📌 Project Overview
This project implements and compares two fundamental graph algorithms—**Dijkstra** and **Bellman-Ford**—to solve the shortest path problem. Using a dataset of 2,000 flight records, the system identifies the most efficient routes between 268 US airports.

## 🛠️ Implementation Details
- **Language:** Python
- **Environment:** Kaggle / Jupyter Notebook
- **Dataset:** [2015 Flight Delays and Cancellations](https://www.kaggle.com/usdot/flight-delays)

## 📊 Algorithm Comparison

| Feature | Dijkstra's Algorithm | Bellman-Ford Algorithm |
| :--- | :--- | :--- |
| **Design Family** | Greedy | Dynamic Programming |
| **Complexity (Avg)** | O((V + E) log V) | O(V * E) |
| **Use Case** | Positive weights, high speed |
| **Observed Time** | **31.45 ms** | **2.1** |

## 📈 Analysis (Best, Average, Worst Case)
### Dijkstra
- **Best Case:** Ω(V + E) - Occurs when the graph is sparse or the destination is found early.
- **Average Case:** Θ((V + E) log V) - The typical performance seen in our flight mapping.
- **Worst Case:** O((V + E) log V) - This occurs when the algorithm processes all vertices and edges, especially in dense graphs where every airport is connected to many others. In this case, the priority queue operations increase significantly, leading to higher execution time.

### Bellman-Ford
- **Best Case:** Ω(E) - Occurs if the graph is already relaxed.
- **Average/Worst Case:** O(V * E) - This occurs when the algorithm must perform all (V − 1) iterations without early termination. In this case, every edge is relaxed repeatedly in each iteration, resulting in the maximum number of computations. This happens when the shortest paths require continuous updates and no early convergence is achieved.

However, in this project, the algorithm converged early, which significantly reduced the actual runtime compared to the theoretical worst case.  _________________________________________________________________________________________________________________________________________________________________________
## Milestone 1: Proposal
- * **Status:** Completed ✅
## Milestone 2: Algorithm Comparison
* **Status:** Completed ✅
* **Algorithms Implemented:** Dijkstra (Greedy) and Bellman-Ford (Dynamic Programming).
* **Dataset:** 2015 Flight Delays (Kaggle).
* **Key Finding:** Both algorithms confirmed identical shortest paths for 268 airports. Bellman-Ford converged in 2.14 ms (2 iterations), comparing efficiently against Dijkstra's 31.45 ms in this specific network topology.
