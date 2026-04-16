# ml-decision-surfaces-lab-
# ML Decision Surfaces Lab 🎯

Interactive playground for linear, nonlinear, and regression models — with rich visual diagnostics (decision regions, 3D surfaces, ROC/AUC, confusion matrix, learning curves) and optional 3D rotation GIFs.

Built with Scikit-learn + Matplotlib + Gradio for an interactive, hands-on ML learning experience.

<img width="241" height="526" alt="image" src="https://github.com/user-attachments/assets/6e60eccf-8744-499f-98e2-409eba6c321d" />
<img width="1754" height="803" alt="image" src="https://github.com/user-attachments/assets/443a6c24-dd47-41c5-b979-665582cd8d1c" />

<img width="1039" height="904" alt="image" src="https://github.com/user-attachments/assets/67527292-1bb9-456e-9b98-42787d458176" />



## ✨ What you can do
<img width="360" height="312" alt="image" src="https://github.com/user-attachments/assets/21fa6923-5e76-4df5-b691-25e882c5bc8d" />
Choose a task type

- Linear classification (e.g., Logistic Regression, Linear SVM, Perceptron, LDA)
- Nonlinear classification (SVM RBF/Poly, KNN, Trees/Ensembles, MLP, etc.)
- Regression (Linear, Ridge/Lasso/ElasticNet, RF, KNN, MLP, SVR)

Generate data

- Synthetic datasets (moons, circles, blobs, XOR, spiral, checkerboard…)
- Upload your own CSV and pick numeric feature & target

Stress-test models

- Add label noise and outliers
- Control train/test split and random seed

Visualize like a pro

- Decision regions (2D)
- 3D decision surface / regression surface
- ROC curve + AUC (classification)
- Confusion matrix (classification)
- Learning curve (train vs validation)
- Model diagnostics (coefficients / feature importances / distributions)

Export results

- Download current plot as PNG
- Generate & download 3D rotation GIF

## 🧠 How it works (high level)

1. Pick mode (Linear / Nonlinear / Regression)
2. Pick dataset (or upload CSV)
3. Tune model + noise/outliers + visualization controls
4. Run experiment → get plots + metrics + downloads

## 🚀 Run (Notebook)

### Option 1 — Google Colab (Recommended)

Upload the notebook to Colab and run all cells:

```text
notebooks/MachineLearningPlaygroundLast.ipynb
```

### Option 2 — Run locally

```bash
pip install -r requirements.txt
jupyter notebook
```

Open:

```text
notebooks/MachineLearningPlayground.ipynb
```

## ✅ Using your own CSV

### Requirements

CSV file with numeric columns

Choose:

- Feature column (numeric)
- Target column (numeric)

### Notes

For classification:

- If target has >2 unique values → it’s converted to binary using the median split
- If target is binary but not {0, 1} → it is mapped to {0, 1}

The app internally uses two features for visualization:

- It takes your selected feature as one axis
- Generates a second synthetic feature to form a 2D input space

## 🎛️ Key controls explained

### Noise %

- Classification: flips labels for a % of samples
- Regression: adds extra noise to a % of targets

### Outliers %

- Classification: injects random points + random labels
- Regression: injects large target deviations

### Use PCA

- If data has >2 dimensions, PCA projects to 2D for plotting

### Animation

- Generates a GIF by rotating the 3D surface view (downloadable)

## 🧪 Tips for best results

- Start with Synthetic data to understand model behavior.
- Increase Noise to observe robustness.
- Add Outliers to see how trees/ensembles differ from linear models.
- Compare train vs validation in the learning curve to detect:
  - underfitting
  - overfitting

## 🙌 Acknowledgements

- Scikit-learn for classic ML models and dataset generators
- Matplotlib for 2D/3D plotting and animations
- Gradio for the interactive UI
