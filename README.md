# **Brain Tumor Detection from MRI Scans**

## **Overview**

This project aims to develop a deep learning pipeline for detecting brain tumors from MRI scans using Python, TensorFlow, and Keras. The pipeline consists of two models:
1. **Classification Model**: Identifies whether a brain MRI scan contains a tumor.
2. **Segmentation Model**: Generates a segmentation mask to locate the tumor within the scan.

## **Table of Contents**
- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Details](#model-details)
  - [Classification Model](#classification-model)
  - [Segmentation Model](#segmentation-model)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## **Dataset**

The dataset used in this project consists of brain MRI images and their corresponding segmentation masks, which highlight the regions affected by tumors.

## **Installation**

To set up the environment for this project, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/brain-tumor-detection.git
    cd brain-tumor-detection
    ```

2. **Install the required libraries**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up Google Colab**:
   This project is designed to be run on [Google Colab](https://colab.research.google.com/), which provides free access to GPUs.

## **Usage**

1. **Prepare the dataset**:  
   Ensure that your dataset is structured correctly and that the paths in `data_mask.csv` are accurate.

2. **Run the notebook**:  
   Open the provided Jupyter notebook in Google Colab and run the cells to train and evaluate the models.

3. **Model Inference**:  
   Use the trained models to classify new MRI scans and generate segmentation masks.

## **Project Structure**
- We will develop 2 separate models to make our predictions. The first model will predict if a brain MRI has a tumor, which will be a binary output of 0 or 1, with 1 indicating positive case. If an MRI does have a tumor, as determined by the first model, then it will be sent to a second deep learning model that will actually make a segmentation mask to display where the tumor is on the given MRI.

## **Model Details**

### **Classification Model**
- **Architecture**: ResNet50/DenseNet121 with transfer learning
- **Input**: 224x224 MRI image
- **Output**: Binary (0 for no tumor, 1 for tumor)
- **Activation**: Sigmoid

### **Segmentation Model**
- **Architecture**: U-Net
- **Input**: 224x224 MRI image
- **Output**: Segmentation mask highlighting the tumor area
- **Activation**: Sigmoid

## **Results**

- **Classification Model**: Achieved an accuracy of **98%** on the test set.

## **Contributing**

Contributions are welcome! Please submit a pull request or open an issue for any improvements or bug fixes.

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
