# Complex Networks Project 2 2018/2019

This repository contains the second Complex Networks project code and results in order to support the project report (group 87). The project was coded using Jupyter and therefore the code is inside Jupyter notebooks. Results from the algorithms have been kept in the notebooks for visualization purposes.

The project is divided in two main folders, "notebooks" and "logs", containing the Jupyter notebooks and results we obtained from running the algorithms, respectively.

# Notebooks
This folder contains code for the algorithms used to support the report. The main file is ``Get Nodes By Degree of Separation_SPL_random_SI`` where we generate a graph using one of the three algorithms (BA, HK and WS). In order to change the graph generator remove the # from the desired algorithm and add one on the rest:

```python
#G = nx.powerlaw_cluster_graph(NUM_NODES, 2, 1)
G = nx.barabasi_albert_graph(NUM_NODES, 6)
# G = nx.watts_strogatz_graph(NUM_NODES, 6, 1)
```

The paramethers for these algorithms can be checked on the NetworkX documentation.

The remaining notebooks are merely steps we took before reaching the final product. Notable mentions are:

  - `Get Nodes By Degree of Separation_old` contains the code we used before *all_pairs_shortest_path_length*, where we calculated nodes at some network distance by using ego-networks
  - `Get Report Data`, the file we used to generate the data needed to support the report
  - `2000_nodes_scale_free`, a file we created using Python's Pickle package in order to save a graph for multiple usages

# Logs

The folder logs contains the results we obtained from running the algorithms with multiple conditions. The ones used in the report are mainly:

  - `charts_results_files`, which contains the propensities for each algorithm with different settings, among other measures such as the average degree and clustering coefficient
  - `processed_data` contains the maximum and minimum values obtained from `charts_results_files` used in the report
  - `ba_5000_nodes_6_avgdg_results` is the results for one iteration of the algorithm using BA with 5000 with 6 average degree, in order to verify that the 2 degrees of separation seen in the same algorithm with only 1000 nodes might be due to node shortage

# Required packages

In order to be able to run our algorithms we recommend running Python 3 using Anaconda. The required packages needed for executing our code can be installed using the following commands through Anaconda Prompt:

```sh
pip install networkx
pip install ndlib
```
