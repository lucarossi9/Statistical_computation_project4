# Cell cycle prediction, an unsupervised approach

* Project in collaboration with the [laboratory of computational biology](https://www.epfl.ch/labs/naef-lab/).

* A poster is available in the repo for a general understanding.

* The results and discussions are available at the following [Website](https://lucarossi9.github.io/statistical_computation_4_website/).

* Datasets:  [McDavid](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003696#s4); [CHLA9](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE146221).

## Abstract

Advances in omics technologies make it possible to study cellular dynamics, providing accurate information on which genes encoded in our DNA are turned on or off in the continuously changing transcriptome. In particular, RNA-seq provides a powerful means to analyze molecular mechanisms underlying cell-state transitions, leading to an unprecedented opportunity to reveal latent biological processes. As a result, the reconstruction of cell development processes from RNA sequences has attracted much attention in recent years. Still, it remains a challenge due to the heterogeneous nature of the processes. The underlying idea in most methods proposed is that there is a biological process responsible for the main variations in the data. Then the goal is to infer the trajectory of that process in the gene expression space so that its effects can be removed. It allows the delineation of other cell subpopulations, which can be crucial to studying tumor evolution. This project explores computational techniques for pseudo-time inference of the cell cycle process from RNA sequences. This study presents different unsupervised approaches to this problem: an **autoencoder** based approach, an **autoencoder with residual neural networks** based approach and a **Bayesian Gaussian process latent variable model** based approach.

# Results

Table summary to compare our result with previous approaches. The accuracies are reported below. 
Our models are GPLVM, residual autoencoders, the others are the main models employed in previous academic research.

|                      | pc3 dataset | mb dataset | H9 dataset |
|----------------------|-------------|------------|------------|
| GPLVM                |  **0.802**       | 0.763      | 0.629      |
| Cyclum model         | 0.793       | **0.779**      | 0.593      |
| PCA                  | 0.448       | 0.482      | 0.489      |
| oscope               | 0.504       | 0.401      | 0.458      |
| reCAT                | 0.695       | 0.591      | 0.617      |
| Cyclops              | 0.446       | 0.395      | 0.515      |
| Residual autoencoder | 0.759       | 0.742      | **0.648**      |
