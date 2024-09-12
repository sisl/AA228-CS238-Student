# AA228-CS238-Student
[![AA228/CS238 Gradescope](https://img.shields.io/badge/aa228%2Fcs238-gradescope-green?color=42a0a2)](https://www.gradescope.com/courses/814395)


[AA228/CS238: Decision Making under Uncertainty](https://aa228.stanford.edu), Autumn 2024, Stanford University.

This repository provides starter code and data for Projects 1 and 2.

## Project 0: 

[![Project 0 Details](https://img.shields.io/badge/project0-details-blue)](https://aa228.stanford.edu/project-0/)

## Project 1: Bayesian Structure Learning

[![Project 1 Details](https://img.shields.io/badge/project1-details-blue)](https://aa228.stanford.edu/project-1/) [![Project 1 Template](https://img.shields.io/badge/project1-LaTeX%20template-white)](https://www.overleaf.com/read/hxwgtnksxtts)

[LaTeX Overleaf template](https://www.overleaf.com/read/hxwgtnksxtts): click the link, go to "Menu", and "Copy Project" (make sure you're signed into Overleaf). Note this is an optional template, you're free to use your own (or not even LaTeX).

    project1/
    ├── data                    # CSV data files to apply structured learning
    │   ├── small.csv               # Titanic dataset¹
    │   ├── medium.csv              # Wine dataset²
    │   └── large.csv               # Secret dataset
    ├── example                 # Helpful examples
    │   ├── example.gph             # Example graph (3 parents, 2 children with 1 parent each and 1 child with 3 parents)
    │   ├── example.csv             # Example data generated from "example.gph"
    │   ├── example.score           # Bayesian score of the "examples.gph" given the data "examples.csv"
    │   ├── examples.pdf            # Visualized "examples.gph" as a TikZ graph
    │   └── titanicexample.pdf      # Simple example network using "small.csv"
    ├── project1.jl             # Starter code in Julia (optional, meant to help)
    └── project1.py             # Starter code in Python (optional, meant to help)

<sup>1</sup>https://cran.r-project.org/web/packages/titanic/titanic.pdf
<br>
<sup>2</sup>https://archive.ics.uci.edu/ml/datasets/Wine+Quality

### Notes
- The starter code is there to help, but you're free to use any language.
- Use `example.gph` to validate your Bayesian scoring algorithm, not your structure learning algorithm.

### Graph Plotting
Here are some resources for plotting graphs in Julia, Python, and MATLAB.
- Julia:
    - [`Graphs.jl`](https://github.com/JuliaGraphs/Graphs.jl/)
    - [`TikzGraphs.jl`](https://nbviewer.jupyter.org/github/JuliaTeX/TikzGraphs.jl/blob/master/doc/TikzGraphs.ipynb)
    - [`GraphPlot.jl`](https://github.com/JuliaGraphs/GraphPlot.jl)
    - [`GraphRecipes.jl`](https://github.com/JuliaPlots/GraphRecipes.jl)
- Python:
    - [`NetworkX`](https://networkx.github.io/documentation/stable/tutorial.html)
- MATLAB:
    - [`GraphPlot`](https://www.mathworks.com/help/matlab/ref/matlab.graphics.chart.primitive.graphplot.html)

#### Julia Examples
##### TikzGraphs.jl
```julia
using Graphs  # for DiGraph and add_edge!
using TikzGraphs   # for TikZ plot output

# An example [Chvatal Graph](https://en.wikipedia.org/wiki/Chv%C3%A1tal_graph)
g = smallgraph(:chvatal) 

# Create notional names for the nodes
node_names = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L"]

# Create TikZ plot with node labels
p = plot(g, node_names)

# Save as PDF (using TikzPictures)
using TikzPictures # to save TikZ as PDF
save(PDF("chvatal_tikz.pdf"), p)
```

##### GraphPlot.jl
```julia
using Graphs
using GraphPlot

g = smallgraph(:chvatal)
node_names = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L"]

p = gplot(g; nodelabel=node_names)

# Save using Compose
using Compose, Cairo, Fontconfig
draw(PDF("chvatal_graphplot.pdf", 16cm, 16cm), p)
```

#### GraphRecipes.jl
```julia
using Graphs
using Plots
using GraphRecipes


g = smallgraph(:chvatal)
node_names = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L"]

p = graphplot(g; names=node_names, node_size=0.2)

savefig(p, "chvatal_graphrecipes.pdf")
```

## Project 2: Reinforcement Learning

[![Project 2 Details](https://img.shields.io/badge/project2-details-blue)](https://aa228.stanford.edu/project-2/) [![Project 2 Template](https://img.shields.io/badge/project2-LaTeX%20template-white)](https://www.overleaf.com/read/gsptsmcrzpdv)

[LaTeX Overleaf template](https://www.overleaf.com/read/gsptsmcrzpdv): click the link, go to "Menu", and "Copy Project" (make sure you're signed into Overleaf). Note this is an optional template, you're free to use your own (or not even LaTeX).

    project2/
    └── data                      # CSV data files of (s,a,r,sp)
        ├── small.csv                 # 10x10 grid world
        ├── medium.csv                # MountainCarContinuous-v0
        └── large.csv                 # Secret RL problem

*Note: no starter code provided for Project 2.*

## Contact
Please post on [Ed](https://edstem.org/) with any questions regarding this code, the data, and the projects in general. We'd be happy to help!
