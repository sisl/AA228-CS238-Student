



# AA228-CS238-Student

[AA228/CS238: Decision Making under Uncertainty](https://aa228.stanford.edu), Autumn 2020, Stanford University.

This repository provides starter code and data for Projects 1 and 2.


## Project 1: Bayesian Structure Learning

See full details here: https://web.stanford.edu/class/aa228/cgi-bin/wp/project-1/

    project1/
    ├── data                    # CSV data files to apply structured learning
    │   ├── small.csv               # Titanic dataset¹
    │   ├── medium.csv              # Wine dataset²
    │   └── large.csv               # Secret dataset
    ├── example                 # Helpful examples
    │   ├── example.gph             # Example graph (3 parents, 1 child each)
    │   ├── example.csv             # Example data generated from "example.gph"
    │   ├── example.score           # Bayesian score of the "examples.gph" given the data "examples.csv"
    │   ├── examples.pdf            # Visualized "examples.gph" as a TikZ graph
    │   └── titanicexample.pdf      # Simple example network using "small.csv"
    ├── project1.jl             # Starter code in Julia (optional, meant to help)
    └── project1.py             # Starter code in Python (optional, meant to help)

Notes:
- the starter code is there to help, but you're free to use any language.
- use `example.gph` to validate your Bayesian scoring algorithm, not your structured learning algorithm.

<sup>1</sup>https://cran.r-project.org/web/packages/titanic/titanic.pdf
<br>
<sup>2</sup>https://archive.ics.uci.edu/ml/datasets/Wine+Quality


## Project 2: Reinforcement Learning
https://web.stanford.edu/class/aa228/cgi-bin/wp/project-2/

    project2/
    └── data                      # CSV data files of (s,a,r,sp)
        ├── small.csv                 # 10x10 grid world
        ├── medium.csv                # MountainCarContinuous-v0
        └── large.csv                 # Secret RL problem

Note: no starter code provided for Project 2 (you're free to use any language).

## Contact
Please post on [Piazza](https://piazza.com/) with any questions regarding this code, the data, and the projects in general. We'd be happy to help!