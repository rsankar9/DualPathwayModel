#### README.md

Ref: 
Sankar, R., Leblois, A. and Rougier, N.P., 2022.
Dual pathway architecture underlying vocal learning in songbirds.
Pre-print.

This folder contains a the models presented in the  abovementioned paper in Python using Jupyter notebooks.

Author: Remya Sankar

#### Contents

2 directories:-

- ```SyrinxModel```: Contains a re-implementation of a syrinx model by Amador, et. al (https://doi.org/10.1038/nature11967). The contour generated using this avian syrinx model, is used to test the dual pathway model.
- ```Model```: Contains the scripts for the dual pathway architecture and the corresponding benchmark model using a single pathway framework.

Figures of the paper:-

-   To generate Fig2, use `SyrinxModel/syrinx-amador.ipynb` and `Model/DualPathwayModel/DualPathwayModel.ipynb`.
-   To generate Fig3, use `Model/DualPathwayModel/DualPathwayModel.ipynb`.
-   To generate Fig4a, use `Model/DualPathwayModel/RepeatRunswArtificial.ipynb`.
-   To generate Fig4b, use `Model/Benchmarks/RepeatBenchmarkWSyrinx.ipynb`.

1 dataset file:-

- `SyrinxModel/Contour/Z-T03_P005_n10.npy`: The performance landscape generated using the syrinx model and used to test the dual pathway model.


##### Usage

-  To simulate the dual pathway model on any specific scenario, use the script `Model/DualPathwayModel/DualPathwayModel.ipynb`.
-  To generate several simulations of the dual pathway model as a batch on Gaussian-based performance landscapes, use `Model/DualPathwayModel/RepeatRunswArtificial.ipynb`.
-  To generate several simulations of the dual pathway model as a batch on Syrinx-based performance landscapes, use `Model/DualPathwayModel/RepeatRunswSyrinx.ipynb`.
-   `Model/DualPathwayModel/RepeatRunswArtificial.ipynb` and `Model/DualPathwayModel/RepeatRunswSyrinx.ipynb` can also be used to compute summary statistics, either by first running several simulations, or using the `Performance.npy` file provided in each folder.
-  The `Performance.npy` file provided in each folder contains the performance metric of batch simulations already run in the relevant scenarios.
- To simulate the alternate learniing rules on the benchmark framework, use `Model/Benchmarks/BenchmarkModel.ipynb`.
-  To run the benchmark tests, use `Model/Benchmarks/RepeatBenchmarkwArtificial.ipynb` or `Model/Benchmarks/RepeatBenchmarkWSyrinx.ipynb` by specifying the desired learning rule.