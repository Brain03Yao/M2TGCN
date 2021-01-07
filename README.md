# MMTGCN (Mutual Multi-scale Triplet GCN)
MMTGCN (Mutual Multi-scale Triplet GCN) can analyze functional and structural connectivity matrix derived from MRI data for brain disorder diagnosis.

Multi-scale templates are used for coarse-to-fine parcellation of brain regions and construction of functional/structural connectivity networks. Multiple triplet GCN (TGCN) are  designed to learn network representations, with each TGCN corresponding to a template. Each TGCN inputs a triplet of three networks/subjects (e.g., <img src="https://latex.codecogs.com/gif.latex?\mathbf{X}_{a}^{T}">, <img src="https://latex.codecogs.com/gif.latex?\mathbf{X}_{p}^{T}">, and <img src="https://latex.codecogs.com/gif.latex?\mathbf{X}_{n}^{T}">) with the same graph architecture but different signals, and outputs the similarity among the triplet. Note that each subject (e.g.,<img src="https://latex.codecogs.com/gif.latex?\mathbf{X}_{a}^{T}">) is represented by a brain graph which contains a set of featuresFand an adjacency matrix <img src="https://latex.codecogs.com/gif.latex?\mathbf{a}">. Each row ofFis a feature vector assigned to each node (i.e., brain region). A template mutual learning scheme is designed to fuse results of multi-scale TGCNs for the final classification.



