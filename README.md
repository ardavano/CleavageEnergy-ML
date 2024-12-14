# Cleavage Energy Prediction with MLIPs

This repository benchmarks **Machine Learning Interatomic Potentials (MLIPs)** for predicting cleavage energy using a **high-fidelity DFT-calculated dataset**. The project explores advanced **equivariant neural networks**, specifically the **MACE model**, leveraging physics principles such as symmetry preservation, rotational equivariance, and translational invariance. These methods enable accurate and efficient predictions of cleavage energy, critical for high-throughput materials discovery.

---

## Project Overview

### Objectives
- Benchmark state-of-the-art MLIP models for cleavage energy prediction.
- Demonstrate the benefits of embedding physics principles like equivariance and symmetry preservation into ML models.
- Analyze performance metrics (MAE, MAPE, R²), outlier distributions, and computational efficiency.

### Key Topics
- **Physics-Informed ML:** Integration of point group symmetries, SO(3) symmetry, and translational invariance of MACE model.
- **Benchmarking MLIPs:** Compare advanced ML architectures, including MACE, GemNet, and EquiformerV2.
- **Physics-embedded Training**: Ensure physical principles guide ML predictions.
- **Scientific Insights**: Demonstrate how physics principles improve ML generalization and accuracy.
- **DFT Dataset**: Utilize a dataset of cleavage energies derived from Density Functional Theory.
- **Dataset Integration:** High-throughput DFT data for bulk and slab structures with detailed geometric and energetic properties.
- **Comprehensive Analysis:** Explore outlier fractions, parity plots, periodic table error visualization, and computational costs.


---

## Dataset
The dataset used is derived from high-throughput **Density Functional Theory (DFT)** calculations, ensuring high fidelity. Key details include:
- **Size:** 36,332 slab configurations derived from 3,716 bulk materials.
- **Features:**
  - **Energetic Properties:** Bulk and slab energies, cleavage energy.
  - **Geometric Properties:** Miller indices, slab thickness, and symmetry information.
  - **Atomic Properties:** Material Project IDs (MPIDs), atomic positions, and lattice vectors.
- **DFT Setup:** PBE functional, ultra-soft pseudopotentials, optimized k-point grids, and energy cutoffs ensuring precise calculations.

---

## **Methodology**

### **1. DFT Calculations**
- Developed using Schrödinger equation reformulation for energy minimization.
- Cleavage energy is computed using:
  \[
  E_{\text{cleavage}} = \frac{E_{\text{slab}} - n \cdot E_{\text{bulk}}}{2A}
  \]
  Where \(E_{\text{slab}}\) and \(E_{\text{bulk}}\) are the total energies of the slab and bulk, \(A\) is the surface area, and \(n\) is the bulk layer count.

### **2. MLIP Architectures**
- **MACE:** Equivariant neural network preserving physical symmetries.
  - SO(3) symmetry for rotational invariance.
  - Tensor-based representations capturing higher-order interactions.
- **GemNet and EquiformerV2:** Graph-based ML models with atomic embeddings and symmetry-preserving operations.
- **Symmetry Advantages:** Models achieve generalization across diverse structures.

### **3. Evaluation Metrics**
- **Mean Absolute Error (MAE):** Measures average prediction error.
- **Mean Absolute Percentage Error (MAPE):** Highlights relative accuracy.
- **R² Score:** Evaluates variance captured by the model.

### **4. Visualizations**
- **Parity Plots:** Compare DFT vs. predicted cleavage energies.
- **Error Heatmaps:** Periodic table distribution of MAPE across elements.
- **Outlier Fractions:** Percentage of extreme errors for each model.

---

## **Computational Code**

### **Scripts**
The project includes detailed Python scripts for preprocessing, training, and evaluating models, as well as visualizing results. Key files include:
- **Main Script (Prediction Cleavage Energy using MLPs):** A Python script to calculate and benchmark MLIP performance.
- **Visualization Notebook:** `Ardavan_project.ipynb` for generating parity plots, error maps, and other analyses.


---

## Results
- Improved cleavage energy predictions with embedded physics.
- Identification of outliers and their impact on model performance.
- Benchmark results for MLIP models.

---

## Future Work
- Investigate outliers and challenging surfaces.
- Combine bulk and surface datasets for improved generalization.
- Develop new physics-embedded MLIP architectures.

---

## Contributors
- **Ardavan Mehdizadeh**
- **Jawad Ahmed**

---

### **Repository Structure**
```plaintext
├── data/                     # Input datasets (DFT-calculated values)
├── scripts/                  # Preprocessing, training, and evaluation scripts
├── notebooks/                # Jupyter notebooks for visualization
├── models/                   # Pre-trained model weights (e.g., MACE, GemNet)
├── results/                  # Output files: metrics, charts, and logs
└── README.md                 # Repository overview
```

---

## References
1. Schindler, P., et al., "Discovery of Stable Surfaces with Extreme Work Functions," *Adv. Funct. Mater.*, 2024. DOI: [10.1002/adfm.202401764](https://doi.org/10.1002/adfm.202401764).
