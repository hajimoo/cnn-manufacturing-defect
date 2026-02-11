# CNN-based Manufacturing Defect Detection

## Overview
This project builds a CNN-based image classification model to detect defective products in manufacturing images.

The goal is not only high accuracy but minimizing false negatives, which is critical in real production environments.

---

## Motivation
In manufacturing systems, missing defective products (false negatives) can lead to serious financial and safety risks.  
Therefore, **Recall** was treated as the primary evaluation metric.

---

## Dataset

The dataset is highly imbalanced.

| Split | Normal | Defective |
|------:|-------:|----------:|
| Train | 1102   | 59        |
| Test  | 276    | 15        |

---

## Preprocessing
- Resize images to 256x256
- Normalize pixel values to [0, 1]
- Convert to RGB format
- Label encoding (0: normal, 1: defect)

---

## Model
- AutoKeras ImageClassifier
- Loss: Binary Cross Entropy
- Validation split: 0.2
- Epochs: 3

---

## Evaluation Metrics
- Accuracy
- Precision
- **Recall (Primary Metric)**
- F1-score
- Confusion Matrix
- ROC Curve

---

## Results
The model achieved high performance on the test dataset.

However, due to the small dataset size and possible data similarity,
further validation is required to rule out potential overfitting or data leakage.

---

## How to Run

1. Open `notebook.ipynb` in Google Colab.
2. Mount Google Drive and set `dir_path` to your dataset directory.
3. Run all cells from top to bottom.

---

## Limitations
- Small dataset size
- Severe class imbalance
- Limited hyperparameter tuning
- No external validation set

---

## Future Improvements
- Data augmentation
- Class weighting
- Cross-validation
- Larger dataset collection
- Deployment pipeline integration
