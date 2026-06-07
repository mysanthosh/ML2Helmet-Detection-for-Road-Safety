# Helmet Detection for Road Safety

## Overview

This project develops an intelligent helmet detection system using Deep Learning to classify whether a motorcycle or bicycle rider is wearing a helmet. The system compares three different Convolutional Neural Network (CNN) architectures: a Custom CNN, MobileNetV2, and ResNet50. In addition to classification performance, Explainable AI (XAI) techniques such as Grad-CAM and SHAP are used to provide visual explanations of model predictions.

## Dataset

Dataset: https://www.kaggle.com/datasets/andrewmvd/helmet-detection

Classes:
- With Helmet
- Without Helmet

## Project Workflow

1. Parse XML annotation files
2. Extract rider head regions using bounding boxes
3. Generate cropped images with padding
4. Create classification dataset
5. Split dataset into Training, Validation, and Testing sets
6. Train Custom CNN, MobileNetV2, and ResNet50 models
7. Evaluate model performance
8. Generate Grad-CAM and SHAP explanations
9. Compare model performance

## Models Implemented

- Custom CNN
- MobileNetV2
- ResNet50

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

## Results

| Model | Accuracy | Precision (Macro) | Recall (Macro) | F1-Score (Macro) | ROC-AUC |
|---------|---------:|------------------:|---------------:|-----------------:|--------:|
| MobileNetV2 | 0.6931 | 0.3466 | 0.5000 | 0.4094 | 0.5000 |
| ResNet50 | 0.6931 | 0.3466 | 0.5000 | 0.4094 | 0.5885 |
| Custom CNN | 0.3069 | 0.1534 | 0.5000 | 0.2348 | 0.6111 |

## Model Parameters

| Model | Parameters |
|---------|-----------:|
| Custom CNN | 110,785 |
| MobileNetV2 | 2,422,081 |
| ResNet50 | 23,850,113 |

## Explainability

The project uses:
- Grad-CAM heatmaps
- SHAP visualizations

These techniques help interpret model predictions and verify that models focus on relevant helmet regions.

## Repository Structure

```text
ML2Helmet-Detection-for-Road-Safety/
├── helmet-detection-for-road-safety.ipynb
├── README.md
├── Tables/
├── Figures/
└── Models/
```

## How to Run

```bash
git clone https://github.com/mysanthosh/ML2Helmet-Detection-for-Road-Safety.git
cd ML2Helmet-Detection-for-Road-Safety
```

Install dependencies:

```bash
pip install tensorflow pandas numpy matplotlib seaborn scikit-learn opencv-python shap
```

Run the notebook in Kaggle with GPU enabled and attach the Helmet Detection dataset.

## Author

**Karnati Mysanthosh**  
MSc Data Science  
University of Europe for Applied Sciences

## License

Academic and research purposes only.
