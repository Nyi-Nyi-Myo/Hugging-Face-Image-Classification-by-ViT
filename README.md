# Hugging-Face Image Classification by ViT

This repository contains a complete pipeline for **multi-label image classification** of surgical instruments using **ViT-base** with custom dataset in **Hugging Face**.

## 🚀 Highlights

- Model: `"google/vit-base-patch16-224-in21k"` (from Hugging Face Models)
- Task: Multi-label classification (one image could have multiple instruments)
- Classes: `G`, `HA`, `IS`, `M`, `NH` (5 classes total)
- Dataset Format: COCO-style with `.json` annotations and image folders
- Threshold Optimization for per-class F1
- Visualization of predictions with ground truth comparison

## 📁 Datasets details

```
Training set size: 956
Positive samples per class:
  Class 0 (G): 280
  Class 1 (HA): 309
  Class 2 (IS): 119
  Class 3 (M): 92
  Class 4 (NH): 187
Validation set size: 331
Positive samples per class:
  Class 0 (G): 120
  Class 1 (HA): 64
  Class 2 (IS): 50
  Class 3 (M): 51
  Class 4 (NH): 96
```

## 📊 Performance

- **Validation F1 (Best Epoch)**: 0.8049
- **Per-Class F1**:
  - `G`:  0.8211
  - `HA`: 0.8103
  - `IS`: 0.8352
  - `M`:  0.9804
  - `NH`: 0.8710

## 🧠 Notes

- The best model is automatically saved during training among 30 epochs.
- Thresholds for each class are optimized using validation F1.
- **Transformer + Augmentation** could provide higher metrics. 
- Example results in `.ipynb`

## 📄 License

This project is released for research purposes only. Please cite appropriately if used in publications.
