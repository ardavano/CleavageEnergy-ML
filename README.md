# Cleavage Energy Prediction with MLIPs

This repository focuses on **benchmarking Machine Learning Interatomic Potentials (MLIPs)** for predicting cleavage energy using a **DFT-calculated dataset**. The project explores **fine-tuning** and **transfer learning** techniques to adapt pre-trained ML models for this specific task.

By embedding **physics principles** directly into the model's training process, such as ensuring symmetry invariance, energy extensivity, and surface area scaling, this work demonstrates how **scientific principles can enhance ML accuracy and interpretability**.

---

## Project Overview

### Objectives
- Benchmark MLIPs for cleavage energy prediction.
- Fine-tune and transfer pre-trained models for accurate results.
- Embed physics principles like rotational invariance and extensivity into ML training.
- Analyze model performance, outlier detection, and generalization.

### Key Topics
- **Benchmarking MLIPs**: Compare predictive performance of MLIP models.
- **DFT Dataset**: Utilize a dataset of cleavage energies derived from Density Functional Theory.
- **Fine-tuning and Transfer Learning**: Adapt ML models for the specific cleavage energy prediction task.
- **Physics-embedded Training**: Ensure physical principles guide ML predictions.
- **Scientific Insights**: Demonstrate how physics principles improve ML generalization and accuracy.

---

## Dataset
The dataset contains:
- Structural information (bulk and slab configurations).
- DFT-calculated cleavage energies.
- Additional features like surface area and Miller indices.

---

## Methodology
1. **Model Selection**: Start with pre-trained MLIPs (e.g., GemNet-OC, MACE).
2. **Fine-tuning**: Adjust weights using the cleavage energy dataset.
3. **Physics Embedding**:
   - Ensure rotational and translational invariance.
   - Include surface area and energy extensivity.
4. **Evaluation**:
   - Benchmark models using MAE, MAPE, and parity plots.
   - Analyze outliers and model generalization.

---

## Results
- Improved cleavage energy predictions with embedded physics.
- Identification of outliers and their impact on model performance.
- Benchmark results for MLIP models.

---

## How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run Fine-tuning
```bash
python main.py --config config.yml --mode train
```

### 4. Evaluate Results
```bash
python main.py --config config.yml --mode evaluate
```

---

## Future Work
- Investigate outliers and challenging surfaces.
- Combine bulk and surface datasets for improved generalization.
- Develop new physics-embedded MLIP architectures.

---

## Contributors
- **Your Name**

---

## References
1. Schindler, P., et al., "Discovery of Stable Surfaces with Extreme Work Functions," *Adv. Funct. Mater.*, 2024. DOI: [10.1002/adfm.202401764](https://doi.org/10.1002/adfm.202401764).
2. Open Catalyst Project Datasets (OC20, OC22).
