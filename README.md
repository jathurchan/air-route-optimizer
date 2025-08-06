# Air Route Optimizer

[![Python](https://img.shields.io/badge/Python-3.12%2B-blue)](https://www.python.org/)
[![Last Commit](https://img.shields.io/github/last-commit/jathurchan/air-route-optimizer)](https://github.com/jathurchan/air-route-optimizer/commits/main)
[![License](https://img.shields.io/github/license/jathurchan/air-route-optimizer)](LICENSE)

This project demonstrates a multi-objective optimization algorithm to design safer and more efficient air traffic networks. It transforms a complex academic problem—the **Crossing Waypoints Location Problem (CWLP)**—into an interactive Python-based demonstration, showcasing an **83% reduction in network risk** with a minimal 0.3% increase in airline operational costs.

## Key Features

* **High-Impact Optimization:** Achieves an **83% reduction in network risk** by intelligently balancing safety metrics against operational costs.
* **Interactive Visualization:** A [Jupyter Notebook](https://www.google.com/search?q=/air-route-optimizer.ipynb) brings the algorithm to life, demonstrating the step-by-step network improvements.
* **Modern & Documented Code:** A clean implementation using Python, NumPy, and Scikit-learn, built for clarity and extensibility.

## The Challenge

Global air traffic is projected to double by 2037, making airspace congestion a critical challenge. The **Crossing Waypoints Location Problem (CWLP)** is a core issue where intersecting flight paths create bottlenecks, increase controller workload, and elevate safety risks. This project provides a computational solution to redesign route networks, minimizing these conflict points while respecting operational constraints.

## Key Results

| Metric | Before | After | Improvement |
| :--- | :---: | :---: | :---: |
| **Network Dangerousness**\* | 322.3B | 54.7B | **-83%** |
| **Airline Cost Index**\* | 469.5M | 471.2M | **+0.3%** |
| **Control Intersections** | 215 | 96 | **-55%** |

<p align="left"><sub>* <em>Dangerousness and Cost are unitless indices calculated by the model for relative comparison.</em></sub></p>

<p align="left">
  <img src="results/optimization_comparison.png" alt="Performance Metrics" width="80%"/>
</p>

## **How It Works**

The optimizer solves a multi-objective problem: **minimize (Airline Cost, Network Dangerousness)** using a three-phase pipeline:

1. **Network Generation:** Builds an initial graph of direct routes from traffic demand and detects all crossing points.
2. **Complexity Reduction:** Applies **K-Means clustering** to merge nearby intersections into fewer, safer waypoints.
3. **Position Optimization:** Iteratively adjusts waypoint positions to minimize conflict risk while preserving route efficiency.

## Project History & Versions

This project evolved from academic research into an interactive prototype.

### v1.0 (2018–2019): Research & Algorithm Design

Co-authored with **Patrice Zhou** ([@Patrice-Zhou](https://github.com/Patrice-Zhou)), this version introduced the Crossing Waypoints Location Problem (CWLP) and developed a multi-objective optimization algorithm as a proof-of-concept.

* **Deliverables**: [Research Paper (French)](/paper_fr.pdf) & [Presentation Slides (French)](/slides_fr.pdf).

### v2.0 (2025): Refactored Prototype & Jupyter Demo

The prototype was refactored for modularity, readability, and hands-on exploration via an interactive notebook.

* **Deliverable**: [Jupyter Notebook](/air-route-optimizer.ipynb).

## Tech Stack

* **Core Logic:** Python 3.12+
* **Numerical Computing:** NumPy, SciPy
* **Machine Learning:** Scikit-learn (for K-Means clustering)
* **Development & Demo:** Jupyter Notebook, Git

## Quick Start

1. **Clone the repository:**

    ```bash
    git clone https://github.com/jathurchan/air-route-optimizer.git
    cd air-route-optimizer
    ```

2. **Set up the virtual environment:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Run the interactive demo:**

    ```bash
    jupyter notebook air-route-optimizer.ipynb
    ```

## License

This project is licensed under the MIT License. See the [LICENSE](/LICENSE) file for details.
