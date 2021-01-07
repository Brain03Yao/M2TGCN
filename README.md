# MMTGCN (Mutual Multi-scale Triplet GCN)
MMTGCN (Mutual Multi-scale Triplet GCN) can analyze functional and structural connectivity matrix derived from MRI data for brain disorder diagnosis.

Multi-scale templates are used for coarse-to-fine parcellation of brain regions and construction of functional/structural connectivity networks. Multiple triplet GCN (TGCN) are  designed to learn network representations, with each TGCN corresponding to a template. Each TGCN inputs a triplet of three networks/subjects (e.g., <img src="http://latex.codecogs.com/gif.latex?mathbf{X}_{a}^{T}}" /><img src="http://chart.googleapis.com/chart?cht=tx&chl=\mathbf{X}_{a}^{T}" style="border:none;">, <img src="http://chart.googleapis.com/chart?cht=tx&chl=\mathbf{X}_{p}^{T}" style="border:none;">, and <img src="http://chart.googleapis.com/chart?cht=tx&chl=\mathbf{X}_{n}^{T}" style="border:none;">) with the same graph architecture but different signals, and outputs the similarity among the triplet. Note that each subject (e.g.,<img src="http://chart.googleapis.com/chart?cht=tx&chl=\mathbf{X}_{a}^{T}" style="border:none;">) is represented by a brain graph which contains a set of featuresFand an adjacency matrix <img src="http://chart.googleapis.com/chart?cht=tx&chl=\mathbf{A}" style="border:none;">. Each row ofFis a feature vector assigned to each node (i.e., brain region). A template mutual learning scheme is designed to fuse results of multi-scale TGCNs for the final classification.



