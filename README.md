# Interpretable AI: Explaining CNN Predictions with SHAP and LIME on MNIST

This project demonstrates how to interpret the predictions of a Convolutional Neural Network (CNN) trained on the MNIST dataset using two popular explainable AI (XAI) techniques: SHapley Additive exPlanations (SHAP) and Local Interpretable Model-agnostic Explanations (LIME).


## Project Overview
In the realm of deep learning, while models achieve high accuracy, their decision-making processes often remain opaque. This project aims to shed light on a CNN's predictions for handwritten digit classification using the MNIST dataset. We utilize SHAP (specifically `GradientExplainer`) and LIME to generate local explanations, showing which parts of an input image contribute most to a specific class prediction.

The notebook walks through:
1.  **Data Loading and Preprocessing**: Loading the MNIST dataset and preparing it for CNN training.
2.  **CNN Model Building and Training**: Constructing a simple CNN and training it on the preprocessed data.
3.  **SHAP Implementation**: Applying SHAP's `GradientExplainer` to understand feature importance for individual predictions.
4.  **LIME Implementation**: Applying LIME's `LimeImageExplainer` to generate local, interpretable explanations.
5.  **Comparative Visualization**: Displaying the original image alongside its SHAP and LIME explanations for a direct comparison.

## Key Features
-   **MNIST Dataset**: Standard dataset for handwritten digit recognition.
-   **Convolutional Neural Network (CNN)**: A basic CNN architecture for image classification.
-   **SHAP (GradientExplainer)**: Provides feature importance by attributing the prediction to input features, especially suitable for deep learning models.
-   **LIME (LimeImageExplainer)**: Creates an interpretable model around a single prediction, highlighting superpixels that influence the prediction.
-   **Visualization**: Side-by-side plots comparing the original image with its SHAP and LIME explanations.

## Installation
To run this notebook, you'll need a Python environment with the following libraries. You can install them using `pip`:

```bash
pip install shap lime tensorflow scikit-image matplotlib numpy
```

Ensure you have a compatible TensorFlow version (tested with TensorFlow 2.x).

## Usage
1.  **Clone the repository (or download the notebook)**:
    ```bash
    git clone <repository-url>
    cd <repository-name>
    ```
2.  **Open the notebook**: You can open the `.ipynb` file in Google Colab, Jupyter Notebook, or JupyterLab.
3.  **Run all cells**: Execute the cells sequentially. The notebook will:
    -   Install dependencies.
    -   Load and prepare the MNIST data.
    -   Build and train the CNN model (for 2 epochs for speed).
    -   Calculate SHAP values for a selected test image.
    -   Calculate LIME explanations for the same test image.
    -   Generate and display the comparative visualization.

No modifications are needed to run the notebook, but feel free to experiment with different `image_index` values or model parameters.

## Output
The primary output is a matplotlib figure displaying three subplots:
1.  **Original Image**: The handwritten digit from the MNIST test set.
2.  **SHAP Explanation**: An overlay on the original image, where red pixels indicate positive contribution to the predicted class and blue pixels indicate negative contribution.
3.  **LIME Explanation**: An overlay showing the superpixels that are most important for the predicted class, with other areas hidden or de-emphasized.

Example Output (for `image_index = 0`, which is typically a '7'):

![SHAP and LIME Explanations](https://raw.githubusercontent.com/YourGitHubUsername/YourRepoName/main/explanation_plot.png) <!-- Replace with an actual image link if you upload one -->

This visualization helps to understand *why* the CNN classified the digit as it did, by highlighting the most influential pixels.

## Dependencies
-   `tensorflow`
-   `keras` (part of TensorFlow)
-   `numpy`
-   `shap`
-   `lime`
-   `scikit-image` (for `mark_boundaries` in LIME visualization)
-   `matplotlib`

## License
This project is open-sourced under the MIT License. See the [LICENSE](LICENSE) file for more details.
