# Classical PCA on MNIST Digits
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your_username/PCA-MNIST/blob/main/PCA_on_MNIST_Digits.ipynb)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

This project demonstrates how classical **Principal Component Analysis (PCA)** can be applied to the MNIST handwritten digit dataset to to see in detail how PCA works and why it's useful for understanding the structure of image data.

We explore PCA for:
- **Dimensionality reduction**
- **Image reconstruction**
- **Synthetic digit generation**

All computations are implemented from scratch using **NumPy**, enabling a transparent, step-by-step understanding of PCA’s mathematical foundations.

---

# Example Outputs
## Example Digits
![Sample Digits](images/mnist_sample_digits.png)

## PCA Variance Explained
![PCA Variance](charts/pca_variance_curve.png)

## PCA 2D Projection
![2D Projection](images/pca_2d_projection.png)

## Example Reconstructions
![Reconstructed Digits](images/reconstruction_examples.png)

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

## Key Results
- **Variance Distribution**: The very first principal components are the most important for preserving the data variance, with the first ~120 components capturing approximatel 75% of the total variance.
- **Reconstruction Quality**: Recognizable digits emerge with as few as 38 components (~50% of total variance).
- **Reconstruction Error**: MSE decreases sharply with first principal components, and then gradually converges toward zero as dimensionality increases.
- **Global Generation**: Sampling from global PCA latent space trained on all digits produces blurry, indistinct results.
- **Class-Specific Generation**: PCA applied to a single digit class (e.g., digit 2) produces sharper and more realistic generations.
- **Noise Tradeoff**: Using too many components reintroduces noise and artifacts into generated samples.

## Future Work
- Extend to **probabilistic PCA**, **VAEs**, or **GANs** for better generative modeling
- Use PCA latent space for dimensionality reduction in **classification** models
- Apply PCA for **noise filtering** applications

---

## Setup
You can view the full list of dependencies in the [requirements.txt](./requirements.txt) file.

To install:

```
pip install -r requirements.txt
```

## How to Run
All experiments and visualizations are contained in the [📓 Classical_PCA_on_MNIST_Digits.ipynb](./PCA_on_MNIST_Digits.ipynb) notebook. Then you can run and explore the notebook step-by-step in any Jupyter environment.
> 💡 Tip: This notebook runs out-of-the-box on **Google Colab** — no installation required.

## Project Structure
<pre>
Classical PCA-MNIST/
├── 📄 README.md            — Project overview
├── 📄 requirements.txt     — Required Python packages
│
├── 📁 notebooks/           — Main analysis notebook
│   └── Classical_PCA_on_MNIST_Digits.ipynb
│
├── 📁 outputs/             — All created charts and images
│   ├── 📁 charts/
│   └── 📁 images/
</pre>

---

## License

This project is licensed under the terms of the [MIT License](./LICENSE).
