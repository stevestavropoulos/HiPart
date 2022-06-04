HiPart: Hierarchical divisive clustering toolbox
================================================
HiPart is a package created for the implementation of hierarchical divisive clustering algorithms. Even among this family of algorithms, its specialty is high-performance algorithms for high-dimensional big data. It is a package with similar execution principles as the scikit-learn package. It also provides two types of static visualizations for all the algorithms executed in the package, with the addition of linkage generation for the divisive hierarchical clustering structure. Finally, the package provides an interactive visualization for manipulating the PDDP-based algorithms' split-point for each of the splits those algorithms generated from the clustering process.

Installation
------------
For the installation of the package, the only necessary actions and requirements are a version of Python higher or equal to 3.6 and the execution of the following command.

```bash
pip install HiPart
```

Simple Example Execution
------------------------
The example bellow is the simplest form of the package's execution. Shortly, it shows the creation of synthetic clustering dataset containing 6 clusters. Afterwards it is clustered with the dePDDP algorithm and only the cluster labels are returned.

```python
from HiPart.clustering import dePDDP
from sklearn.datasets import make_blobs

X, y = make_blobs(n_samples=1500, centers=6, random_state=0)

clustered_class = dePDDP(max_clusters_number=6).fit_predict(X)
```

Users can find complete execution examples for all the algorithms of the HiPart package in the [clustering_example](https://github.com/panagiotisanagnostou/HiPart/blob/main/clustering_example.py) file of the repository. Also, the users can find a KernelPCA method usage example in the [clustering_with_kpca_example](https://github.com/panagiotisanagnostou/HiPart/blob/main/clustering_with_kpca_example.py) file of the repository. Finally, the file [interactive_visualization_example](https://github.com/panagiotisanagnostou/HiPart/blob/main/interactive_visualization_example.py) contains an example execution of the interactive visualization. The instructions for the interactive visualization GUI can be found with the execution of this visualization.
