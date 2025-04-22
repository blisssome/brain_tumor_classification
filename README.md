
# 🧠 Brain Tumor Classification with Vision Transformers

This repository contains an implementation of a Vision Transformer (ViT) model for classifying brain MRI scans into two categories: **tumor** and **no tumor**. The model achieves an **F1-score of 0.94**, with interpretability powered by **Attention Rollout**, allowing visual insights into the decision-making process.

## 🚀 Highlights

- 📊 **High Accuracy**: Achieved 0.94 F1-score on the test set.
- 🔍 **Explainability**: Integrated attention rollout visualizations for interpretability.
- 🧠 **Medical Imaging**: Applies state-of-the-art transformer architecture to brain MRI classification.
- 🔬 **Error Analysis**: Includes attention maps for misclassified samples.
- 📈 **Performance Visualization**: Includes a detailed confusion matrix.

---

## 📁 Project Structure

```bash
.
├── brain_tumor.ipynb              # Main notebook for training, evaluation, and visualization
├── attention_rollout.png          # Example of attention visualization for correct prediction
├── attention_rollout_lacking_semantics.png  # Misclassified cases with attention maps
├── best_confusion_matrix.png      # Confusion matrix showing final performance
└── README.md
```

---

## 🧠 Model Overview

We use a **Vision Transformer (ViT)** architecture trained on T2-weighted axial MRI scans. The model has been fine-tuned to handle small-scale medical data using transfer learning and regularization techniques.

### 📌 Task

- **Binary Classification**:
  - **Class 0**: No Tumor
  - **Class 1**: Tumor

---

## 📸 Visualization

### ✅ Correct Prediction with Attention
![Attention Rollout](./attention_rollout.png)

The attention map highlights regions critical to the model's prediction. Notice how the tumor region is sharply attended to.

---

### ❌ Misclassifications and Their Attention Maps
![Wrong Predictions](./attention_rollout_lacking_semantics.png)

Even in incorrect predictions, the attention maps show where the model focused—often highlighting semantically relevant but misleading regions.

---

### 📊 Confusion Matrix
![Confusion Matrix](./best_confusion_matrix.png)

- **True Positives (TP)**: 30
- **True Negatives (TN)**: 18
- **False Positives (FP)**: 2
- **False Negatives (FN)**: 1

---

## 🧪 Metrics

| Metric       | Score  |
|--------------|--------|
| Accuracy     | 0.96   |
| Precision    | 0.94   |
| Recall       | 0.97   |
| **F1-score** | **0.94** |

---

## 🛠️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/brain-tumor-vit.git
   cd brain-tumor-vit
   ```

2. Open the notebook:
   ```bash
   jupyter notebook brain_tumor.ipynb
   ```

3. Install required dependencies (if not already):
   ```bash
   pip install -r requirements.txt
   ```

---

## 📚 References

- Dosovitskiy et al., "An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale"
- Chefer et al., "Transformer Interpretability Beyond Attention Visualization"

---

## 💡 Future Work

- Multi-class classification (e.g., glioma, meningioma, pituitary)
- Integration with clinical metadata
- Model compression for edge deployment

---

## 🧑‍🔬 Author

**Emil Aliyev**  
Graduate student in AI & Data Science  
Special interests: cognitive science, interpretability, and neurosymbolic AI.
