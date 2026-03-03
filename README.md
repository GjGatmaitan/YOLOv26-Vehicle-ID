# YOLOv26-Vehicle-ID
Vehicle Identification using YOLOv26 with multiple optimizer comparison

## Project Overview
This project implements YOLOv26 object detection on a custom traffic dataset derived from intersection surveillance footage.

The objective was to compare three training configurations using different optimizers and hyperparameters.

---

## Dataset
- Classes: ebike, hatchback, motorcycle, pick-up, sedan, suv, van
- Image size: 640x640
- Format: YOLO
- Train/Val/Test split: 70/20/10

Dataset Link:
https://drive.google.com/drive/folders/1TzaYb7xPNdJNjpnsuuwMPZh3vF42TY0J?usp=drive_link

---

## Model Configurations

| Model | Optimizer | Epochs | mAP50 | Precision | Recall | F1 |
|-------|----------|--------|--------|-----------|--------|-----|
| Model 1 | Adam | 25 | 0.726 | 0.931 | 0.561 | 0.700 |
| Model 2 | Adam | 30 | 0.507 | 0.774 | 0.508 | 0.613 |
| Model 3 | SGD | 40 | 0.834 | 0.773 | 0.805 | 0.789 |

---

## Results
Model 3 achieved the best overall balance between precision and recall, making it the most suitable for real-world traffic deployment.

Confusion matrices and training outputs are shown in the notebook.

---

## How to Run
1. Open notebook in Google Colab
2. Mount Google Drive
3. Install ultralytics
4. Run training cells sequentially

---

## Author
[Gatmaitan, Gilbert Jan A.]
