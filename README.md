# PCA on MNIST Digits

This project demonstrates how **Principal Component Analysis (PCA)** can be applied to the MNIST handwritten digit dataset to to see in detail how PCA works and why it's useful for understanding the structure of image data.

We explore PCA for:
- **Dimensionality reduction**
- **Image reconstruction**
- **Synthetic digit generation**

All computations are implemented from scratch using **NumPy**, enabling a transparent, step-by-step understanding of PCA’s mathematical foundations.

---

## Project Overview

- Loading and standardizing the full MNIST dataset
- Visualization of original MNIST digits
- **Computation of PCA** using **Singular Value Decomposition (SVD)** to obtain an **orthonormal basis (ONB)** of principal components and the **variance explained** by each component
- **Analysis of individual variance** captured by each individual principal component
- **Analysis of cumulative variance** captured by subspaces spanned by the first M principal components
- **Projection of digits** onto subspaces spanned by principal components
- **Reconstuction of digits** from latent spaces with varying numbers of PCA components
- **Evaluation of reconstruction error** vs number of components using  Mean Squared Error (MSE) 
- **Generation of new digits** using both global PCA (across all digits) and class-specific PCA
- Compare generation quality for different numbesr of PCA components forming the latent space

## Project Structure
<pre>
PCA-MNIST/
├── 📄 README.md            — Project overview
├── 📄 requirements.txt     — List of Python libraries
├── 📄 .gitignore            — Files/folders ignored by Git
│
├── 📁 notebooks/            — Exploratory Jupyter Notebooks
│   └── PCA_on_MNIST_Digits.ipynb
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
