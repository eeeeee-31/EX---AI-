# 🧠 Explainable AI using SHAP and LIME on MNIST

## 📌 Project Overview

This project demonstrates how to interpret the predictions of a deep learning model using Explainable AI (XAI) techniques. A Convolutional Neural Network (CNN) is trained on the MNIST dataset to classify handwritten digits (0–9), and two popular explanation methods — SHAP and LIME — are used to understand the model’s decision-making process.

---

## 🎯 Objective

Deep learning models often act as “black boxes,” making it difficult to understand how predictions are made. The objective of this project is to provide transparency by identifying which parts of an input image influence the model’s predictions.

---

## ⚙️ Methodology

### 1. Model Training

* A CNN model is trained on the MNIST dataset.
* Input images are normalized and reshaped for training.
* The model outputs probabilities for each digit class (0–9).

---

### 2. SHAP Explanation (GradientExplainer)

* SHAP (SHapley Additive exPlanations) is used to compute feature importance.
* The *GradientExplainer* method is applied, which is suitable for deep learning models.
* SHAP provides *pixel-level explanations*, showing how each pixel contributes to the final prediction.

  * Positive contribution → increases prediction confidence
  * Negative contribution → decreases prediction confidence

---

### 3. LIME Explanation

* LIME (Local Interpretable Model-agnostic Explanations) is used as a complementary method.
* It segments the image into regions (superpixels) and identifies the most influential regions.
* LIME provides *region-level explanations*, making it easier to visually interpret model behavior.

---

## 📊 Results and Observations

* The CNN model successfully classifies handwritten digits with good accuracy.
* SHAP visualizations highlight important pixels that influence the prediction.
* LIME visualizations highlight important regions of the image.
* Both methods confirm that the model focuses on meaningful parts of the digit rather than irrelevant areas.

---

## ⚖️ SHAP vs LIME

| Feature           | SHAP           | LIME           |
| ----------------- | -------------- | -------------- |
| Type              | Model-specific | Model-agnostic |
| Explanation Level | Pixel-level    | Region-level   |
| Detail            | High           | Moderate       |
| Interpretability  | Precise        | Intuitive      |

---

## 🧠 Conclusion

This project shows that combining SHAP and LIME provides a more comprehensive understanding of model predictions. While SHAP offers detailed feature-level insights, LIME provides intuitive region-based explanations. Together, they help improve trust, transparency, and interpretability in deep learning models.

---

## 🚀 Future Improvements

* Train the model with more epochs for higher accuracy
* Evaluate explanations on multiple test samples
* Extend to more complex datasets and models
* Include quantitative evaluation of explanation quality

---

## 📚 References

* Lundberg, S. M., & Lee, S.-I. (2017). A Unified Approach to Interpreting Model Predictions (NeurIPS)
