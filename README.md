## Project PL-Guard: Adversarial Robustness of Polish NLP Models
### Project Overview
This project conducts a comprehensive security and robustness analysis of Polish BERT-based NLP models. Using the PL-Guard dataset, we explore how adversarial text attacks (typos, leetspeak, character substitutions) affect the semantic representation of text and degrade safety classifiers.

We move beyond standard accuracy metrics to analyze:

- Geometric Distortion: How attacks "shatter" semantic clusters in high-dimensional space.

- Embedding Drift: Quantifying the movement of data points due to malicious perturbations.

- Defensive Immunization: Evaluating Adversarial Training as a method to harden safety models.

### Key Features
- Embedding Analysis: Text vectorization using ```bash dkleczek/bert-base-polish-uncased-v1.```

- Visualization: Dimensionality reduction via t-SNE and UMAP to compare clean vs. adversarial data.

- Unsupervised Drift Detection: Using Isolation Forest to identify adversarial samples as outliers.

- Robust Classification: Comparative study of Logistic Regression, SVM, and Random Forest under attack.

### Results Summary
- Linear Stability: Linear SVMs proved more stable under character-level attacks than Logistic Regression.

- Adversarial Training: Retraining models on mixed (clean + adversarial) data improved detection accuracy by up to 10% for linear models.

- Distribution Shift: Adversarial modifications were over 2x more likely to be flagged as outliers compared to clean text.

### Dataset & Dependecies
##### Hugging Face Access:
This project uses the ```bash NASK-PIB/PL-Guard``` dataset. You may need a Hugging Face token to load the data.

##### Dependencies
- ```bash torch``` & ```bash transformers``` (BERT Model)

- ```bash scikit-learn``` (Clustering & Classifiers)

- ```bash plotly``` & ```bash matplotlib``` (Visualizations)

- ```bash umap-learn``` & ```bash pandas``` & ```bash numpy```

