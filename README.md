# Multiomics data integration with quantile matrix factorization
Quantile matrix factorization (QMF) is a technique to approximate a matrix by a low-rank matrix followed by row-wise monotonic transform. Here we test its ability to identify factors associated with survival in bulk multi-omics TCGA data, and compare it to plain nonnegative matrix factorization (NMF), following the [MOMIX benchmark](https://github.com/ComputationalSystemsBiology/momix-notebook) proposed by [Cantini et al. (2020)](https://doi.org/10.1101/2020.01.14.905760).

## Data provided
We provide the pre-computed matrix factorization by NMF and QMF in the [data/factorizations/](data/factorizations/) directory. Note that we provide two factorizations for each method and each cancer, obtained by running the optimization twice with two different random initializations. We also provide the survival information for each cancer, as provided by the [MOMIX benchmark](https://github.com/ComputationalSystemsBiology/momix-notebook), in the [data/cancer/](data/cancer/) directory.

## Run the benchmark
To run the benchmark on the NMF and QMF factorizations, just run the Jupyter notebook (adapted from [the MOMIX one](https://github.com/ComputationalSystemsBiology/momix-notebook/blob/master/scripts/Comparison%20in%20cancer%20.ipynb)):

`jupyter-notebook script/runbenchmark.ipynb`

It should produce a series of plots, as in the QMF paper cited below.
## Citation
Cuturi, M., Teboul, O., Niles-Weed, J., and Vert, J.-P. (2020), “Supervised Quantile Normalization for Low-rank Matrix Approximation,” in Thirty-seventh International Conference on Machine Learning (ICML 2020). To appear. [PDF](https://arxiv.org/pdf/2002.03229.pdf)