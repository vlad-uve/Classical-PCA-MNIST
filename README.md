# PCA on MNIST Digits

This project explores Principal Component Analysis (PCA) applied to the MNIST digit dataset, focusing on dimensionality reduction, reconstruction, and simple generative modeling.

## Project Overview

- Visualization of original MNIST digits
- Creation of an Orthonormal Basis (ONB) using both SVD and eigendecomposition
- Analysis of total variance and explained variance
- Reconstruction of digits with varying numbers of PCA components
- Analysis of reconstruction error vs number of components
- Simple random generation of new digits using PCA space

## Project Structure
<pre>
PCA-MNIST/
├── 📄 README.md            — Project overview
├── 📄 requirements.txt     — List of Python libraries
├── 📄 .gitignore            — Files/folders ignored by Git
│
├── 📁 notebooks/            — Exploratory Jupyter Notebooks
│   └── 01-pca-mnist.ipynb
│
├── 📁 src/                  — Source code (optional utilities, future modules)
│   └── pca_utils.py
│
├── 📁 outputs/              — Saved figures and generated samples
│   ├── 📁 figures/
│   └── 📁 samples/
│
└── 📁 data/                 — Dataset (empty or managed automatically)
    └── README.md
</pre>


## Key Results

- **Explained Variance Curves**: Most variance captured within first 50–100 components.
- **Reconstruction Quality**: Acceptable reconstruction achieved with 50-100 components.
- **Simple Generation**: New "zero" digits sampled from PCA latent space.

## Future Work

- Develop a modular `MyPCA` class
- Explore deeper probabilistic models (e.g., Probabilistic PCA, VAE)

## Setup

To install all required Python libraries, run:

```bash
pip install -r requirements.txt
```

## How to Run

All experiments and visualizations are contained in the notebook:

```bash
notebooks/01-pca-mnist.ipynb
```
Then you can run and explore the notebook step-by-step.


---

## License

This project is open-source and available for educational and personal use.
