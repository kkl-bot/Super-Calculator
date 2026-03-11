# Super Math Suite

<p align="center">A polished desktop math workbench built with PyQt6, NumPy, Matplotlib, and SymPy.</p>

<p align="center">
  <img alt="Python 3.9+" src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="PyQt6" src="https://img.shields.io/badge/UI-PyQt6-41CD52?style=flat-square&logo=qt&logoColor=white">
  <img alt="NumPy" src="https://img.shields.io/badge/Math-NumPy-013243?style=flat-square&logo=numpy&logoColor=white">
  <img alt="Matplotlib" src="https://img.shields.io/badge/Plots-Matplotlib-11557C?style=flat-square">
  <img alt="License MIT" src="https://img.shields.io/badge/License-MIT-black?style=flat-square">
</p>

Super Math Suite is a modular desktop application that brings together four practical math tools in one interface: a calculator, a linear algebra workspace, an interactive graph algorithms lab, and a multi-function plotting panel.

## Overview

This project is designed as a tab-based PyQt6 application with a clean custom UI and a simple code layout. It is a good fit for coursework, demos, experimentation, and small desktop math utilities.

## Modules At A Glance

| Module | What it does | Details |
| --- | --- | --- |
| Calculator | Quick numeric evaluation | Supports button-based input for arithmetic, parentheses, decimals, and exponentiation using `^` |
| Linear Algebra | Matrix operations in a grid UI | Determinant, inverse, rank, RREF, and transpose |
| Graph Algorithms | Visual graph construction and analysis | Weighted edges, directed or undirected mode, adjacency matrix export, Dijkstra shortest path, connectivity, connected components, bipartite check, and Prim MST |
| Calculus | Function plotting and comparison | Plot multiple expressions at once, set custom x-range, and use the embedded Matplotlib toolbar |

## Interface Highlights

- Tabbed desktop layout built with PyQt6
- Split-panel workflows for input and results
- Draggable graph nodes with live edge updates
- Embedded Matplotlib canvas with toolbar controls
- Lightweight custom styling through a centralized Qt stylesheet

## Tech Stack

| Layer | Tools |
| --- | --- |
| Desktop UI | PyQt6 |
| Numerical operations | NumPy |
| Plotting | Matplotlib |
| RREF support | SymPy |
| Core logic | Custom `Matrix` and `GraphAlgo` backends |

## Project Structure

```text
Super-Calculator/
|-- main.py
|-- backend.py
|-- components.py
|-- styles.py
`-- tabs/
    |-- tab_numeric.py
    |-- tab_linear.py
    |-- tab_graph.py
    `-- tab_calculus.py
```

## Quick Start

1. Install Python 3.9 or newer.
2. Install the required packages:

```bash
python -m pip install -r requirements.txt
```

3. Launch the app:

```bash
python main.py
```

SymPy is included in the dependency file because the RREF feature depends on it for correct results.

## How To Use

### Calculator

- Enter expressions using the on-screen buttons.
- Use `^` for powers, such as `(2+3)^4`.
- Press `=` to evaluate and `C` to clear the display.

### Linear Algebra

- Set the number of rows and columns.
- Click `Reset Grid` to rebuild the matrix input table.
- Fill in the matrix values and run any operation.
- Results appear in the output panel on the right.

### Graph Algorithms

- Choose `Add Node`, then click the canvas to create labeled nodes.
- Choose `Add Edge`, click a source node and a destination node, then enter a weight.
- Toggle `Directed Graph` to switch between directed and undirected behavior.
- Use `Show Adj Matrix` to print the graph as a Python nested list.
- Use the `Start` and `End` fields for Dijkstra; the values should match the node IDs displayed on the canvas.
- `Show MST (Prim)` is available for undirected graphs only.

### Calculus

- Add one or more functions such as `x**2`, `np.sin(x)`, `np.exp(x)`, or `abs(x)`.
- Set the x-axis range before plotting.
- Click `Plot All` to compare multiple functions on the same axes.
- Use the Matplotlib toolbar to pan, zoom, and save figures.

## Expression Notes

- Calculator and plotting expressions are evaluated as Python expressions.
- In the plotting tab, `x`, `np`, and `abs` are available by default.
- Enter only trusted expressions on your own machine.

## Why This Project Is Useful

- It combines several common math workflows into one small desktop app.
- The codebase is compact and approachable for learning PyQt6 application structure.
- The graph tab offers both visual interaction and algorithmic feedback, which makes it useful for demonstrations.

## License

This project is released under the MIT License. See the `LICENSE` file for details.
