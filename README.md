# Quantum-Assisted Correlation Clustering

<!-- [![Paper DOI](https://img.shields.io/badge/Paper_DOI-10.1007/978.3.031.97629.2_2-orange)](https://doi.org/10.1007/978-3-031-97629-2_2)   -->
[![arXiv](https://img.shields.io/badge/arXiv-2509.03561-green)](https://doi.org/10.48550/arXiv.2509.03561)  
[![Conference](https://img.shields.io/badge/Conference-QAI'25-blue)](https://qai2025.unina.it/)  
[![License: LGPL v2.1](https://img.shields.io/badge/License-LGPL%20v2.1-orange.svg)](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html)  
[![LinkedIn: SupreethMV](https://img.shields.io/badge/LinkedIn-Supreeth%20Mysore%20Venkatesh-blue)](https://www.linkedin.com/in/supreethmv/)  
[![Website: SupreethMV](https://img.shields.io/badge/Website-www.supreethmv.com-brightgreen)](https://www.supreethmv.com)

---


This repository contains the code and resources for reproducing the experiments and results presented in the paper:

**"Quantum-Assisted Correlation Clustering"**

Accepted at the IEEE QAI 2025 Conference. The preprint is available on [arXiv](https://arxiv.org/abs/2509.03561).

---

## About the Paper

### Abstract
This work introduces a hybrid quantum-classical method for correlation clustering, a graph-based unsupervised learning task that partitions nodes in a graph based on pairwise agreement and disagreement. The proposed method adapts **GCS-Q**, a quantum-assisted solver originally designed for coalition structure generation, to maximize intra-cluster agreement in signed graphs through recursive divisive partitioning. Each bipartitioning step is encoded as a quadratic unconstrained binary optimization (QUBO) problem, solved via quantum annealing. This approach enables handling graphs with arbitrary correlation structures, including negative edges, without relying on metric assumptions or a predefined number of clusters.

Empirical evaluations on synthetic signed graphs and real-world hyperspectral imaging data demonstrate that GCS-Q outperforms classical algorithms in robustness and clustering quality, particularly in scenarios with cluster size imbalance. These results highlight the promise of hybrid quantum-classical optimization for advancing scalable and structurally-aware clustering techniques in graph-based unsupervised learning.

---

## Key Contributions

1. **Novel Adaptation of GCS-Q**: The paper adapts the GCS-Q algorithm, originally developed for coalition structure generation, to the task of correlation clustering on signed graphs.
2. **Hybrid Quantum-Classical Optimization**: Integrates quantum annealing within a hierarchical clustering framework to solve QUBO problems for graph partitioning.
3. **Empirical Validation**: Demonstrates the effectiveness of GCS-Q on both synthetic signed graphs and real-world hyperspectral imaging datasets, outperforming classical clustering methods in robustness and quality.

---

## Repository Structure

- `clustering-experiments.ipynb`: Jupyter notebook containing the implementation of clustering algorithms, synthetic data generation, and experimental evaluations.
- `clustering-experiments_EO.ipynb`: Jupyter notebook for running clustering experiments for the hyperspectral Earth Observation (EO) data.
- `finding-optimal-k_EO.ipynb`: Jupyter notebook for determining the optimal number of clusters (`k`) for the hyperspectral data.
- `visualize_results.ipynb`: Jupyter notebook for parsing the clustering results in `\results` directory and visualizing the performance metrics to save them at `\plots`.
- `visualize-methods.ipynb`: Jupyter notebook for comparing and visualizing different clustering algorithms and their outputs, (Fig. 1 in paper).
- `requirements.txt`: List of dependencies required to run the code.
- `hyspectral_data/`: Directory containing hyperspectral EO datasets.
- `results/`: Directory for containing saved experimental results and logs.

---

## How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/supreethmv/Quantum-Correlation-Clustering.git
cd Quantum-Correlation-Clustering
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run Experiments
Open the `clustering-experiments.ipynb` notebook and execute the cells to:
- Generate synthetic signed graphs.
- Run clustering algorithms (GCS-Q, K-Means, PAM, DIANA, etc.).
- Evaluate clustering performance using metrics like NMI and Modularity.

---

## Summary of the Paper

### Introduction
Correlation clustering (CC) is a graph-based paradigm that extends traditional clustering methods by directly modeling pairwise relationships. Unlike distance-based methods like K-Means, CC operates on weighted graphs where edges represent real-valued affinities, including negative weights for dissimilarities. This flexibility makes CC suitable for diverse applications, including social network analysis, recommendation systems, and hyperspectral imaging.

### Methodology
The proposed method follows a hierarchical divisive clustering approach, starting with a single cluster containing all nodes and recursively partitioning it into smaller clusters. The GCS-Q algorithm is adapted to maximize intra-cluster agreement by solving QUBO problems using quantum annealing. This approach avoids metric assumptions and predefined cluster counts, making it robust to complex graph structures.

### Experiments
- **Synthetic Data**: Evaluated on signed graphs with varying cluster size distributions, demonstrating superior performance in robustness and clustering quality.
- **Real-World Data**: Applied to hyperspectral imaging datasets, achieving higher modularity scores compared to classical methods.

### Results
GCS-Q consistently outperforms classical clustering methods, particularly in scenarios with cluster size imbalance and complex correlation structures. The method's ability to handle signed graphs and its independence from predefined cluster counts make it a versatile tool for graph-based unsupervised learning.

---

## Citation
If you use this code or find it helpful, please cite the paper:

```
@inproceedings{macaluso2025quantum,
  title={Quantum-Assisted Correlation Clustering},
  author={Antonio Macaluso and Supreeth Mysore Venkatesh and Diego Arenas and Matthias Klusch and Andreas Dengel},
  booktitle={IEEE QAI},
  year={2025},
  eprint={2509.03561},
  archivePrefix={arXiv},
  primaryClass={quant-ph},
  url={https://arxiv.org/abs/2509.03561}, 
}
```

---



## **Contact**

**Supreeth Mysore Venkatesh**  

For any inquiries, please reach out to:

- Email: contact@supreethmv.com  
- LinkedIn: [Supreeth Mysore Venkatesh](https://www.linkedin.com/in/supreethmv/)  
- Website: [www.supreethmv.com](https://www.supreethmv.com)


## Contributors

[![Supreeth Mysore Venkatesh](_repo_data/supreethmv.jpg)](https://www.supreethmv.com)