# Monte Carlo Mazes

## Project Description

Using an open-source dataset of randomly generated squared mazes from a [Kaggle dataset](https://www.kaggle.com/datasets/emadehsan/rectangular-maze-kruskals-spanning-tree-algorithm/code), a reinforcement learning algorithm (paired with Monte Carlo methods) was trained to solve simple mazes. The maze dataset was selected for consistent start and end positions, relatively simple solutions, and small maze sizes. A weighted reward matrix is cast over the maze, and a simple geomoetry (with no "trick" features) supported the method. 

For each step through the maze, the agent can proceed forward or select a route after encountering an intersection. When choosing a route, random probes explore each possible path forward (stopping at dead ends) and reporting on the accrued rewards. The agent finds the route with the largest average return (a Monte Carlo method) and proceeds along that path. Rewards are calculated by the weighted reward matrix centered at the maze's exit that uses a radially decreasing reward scheme. Once the agent reaches a dead end or the maze's exit, the iterations end and the final status is returned.

Throughout the project, a number of factors impacted the results. Rather than selecting the route with the highest average return, attempts to select the route with the greatest probe reward created a higher maze solution rate. Additionally, the random probing of possible routes created inconsistent paths through a given maze. These challenges may be a feature of the simple maze dataset, and future work includes exploring different path selection methods and probing techniques. In addition to altering the reinforcement learning method, future work could include testing the algorithm on complex mazes and trick mazes. Changing the maze architecture would require a different weight ovrelay, and possible solutions could be explored in future work.

## Table of Contents

* How to Access, Install, and Run the Project
* How to Contribute
* Tests and Outcomes

## How to Access, Install, and Run the Project

To accesss the open-source maze dataset, visit the [Kaggle page](https://www.kaggle.com/datasets/emadehsan/rectangular-maze-kruskals-spanning-tree-algorithm/code) and create a local download of the image files. To run the Python code, download the [Anaconda app](https://anaconda.org/) and open the file in Jupyter Notebooks to run each cell. In line three of the second cell, the hard coded file path to the .png maze files will need to be customized to the user's computer. After tuning the filepath, the algorithm will run on the file's third cell.

## How to Contribute

To contribute to this work, please fork off the repository or email rla00009@mix.wvu.edu with questions, comments, or updates.

## Tests and Outcomes

After applying the algorithm to simple square mazes, the results were formalized in a research symposium poster and presented to a series of judges. The poster and results can be found in the Symposium_Poster.png file.

