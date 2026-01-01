# Transfer Learning: VGG16 vs. ResNet50

![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat&logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Applications-red?style=flat&logo=keras)
![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)

## Project Overview
This project utilizes **Transfer Learning** to leverage state-of-the-art Deep Learning models pre-trained on the massive **ImageNet** dataset (1.2 million images).

The goal is to implement and compare two iconic Convolutional Neural Network (CNN) architectures—**VGG16** and **ResNet50**—for the task of image classification. Instead of training from scratch, we load the pre-trained weights to perform accurate inference on new images immediately.

## Architectures Used

### 1. VGG16 (Visual Geometry Group)
* **Structure:** A deep stack of 13 convolutional layers and 3 dense layers.
* **Key Characteristic:** Simplicity and uniformity (uses 3x3 small filters throughout).
* **Use Case:** Excellent feature extractor for general-purpose vision tasks.



### 2. ResNet50 (Residual Network)
* **Structure:** A 50-layer deep network using "Skip Connections".
* **Key Characteristic:** Solves the "vanishing gradient" problem, allowing for much deeper networks to be trained effectively.
* **Use Case:** High-accuracy classification where capturing complex features is required.



## Tech Stack
* **Deep Learning:** TensorFlow, Keras Applications API
* **Image Processing:** Keras Preprocessing, NumPy
* **Dataset:** ImageNet (via pre-trained weights)

## Capabilities
The pipeline includes:
1.  **Preprocessing:** Resizing input images to `224x224` and applying model-specific normalization (e.g., mean subtraction).
2.  **Inference:** Running the image through both networks to generate probability distributions.
3.  **Decoding:** Translating the raw probabilities into human-readable class labels (e.g., "Golden Retriever", "Sports Car") using `decode_predictions`.

## How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PyPro2024/Transfer-Learning-VGG16-ResNet50.git]
    ```
2.  **Install dependencies:**
    ```bash
    pip install tensorflow numpy pillow
    ```
3.  **Run the Notebook:**
    Open `Transfer_Learning_VGG16_ResNet.ipynb` in Jupyter Notebook or Google Colab.
    * *Note: Update the `img_path` variable with a path to your own local image to test the predictions.*

##  Results
The notebook outputs the **Top-5 Predictions** for each model, allowing for a side-by-side comparison of confidence scores.
* *Example Output:*
    * **VGG16:** `98.5% Persian Cat`
    * **ResNet50:** `99.1% Persian Cat`

---
*If you find this project helpful, feel free to ⭐ the repo!*
