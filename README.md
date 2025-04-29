# Custom Object Detection with YOLO

## Introduction
This project focuses on creating a **custom object detection model** using the YOLOv5 architecture. We selected strawberries as our object of interest, built and labeled a dataset, trained the model, and evaluated its performance. The goal was to gain hands-on experience in **data collection**, **model training**, and **performance evaluation**.

## Object Selection
During the initial phase, we selected **strawberries** as the detection target due to their visually complex features, which present a challenging and meaningful task for computer vision models.

## Data Collection and Preparation
**Data Collection**:
- 55 images were captured using an iPhone (.heic format).
- Images were taken under varied lighting and environmental conditions to promote model generalizability.

**Labeling**:
- Annotation was done using **makesense.ai**.
- Bounding boxes were labeled in **YOLO format**:
  - `class_id, x_center, y_center, width, height`
- Dataset was split strategically:
  - **Training Set**: 38 images (70%)
  - **Validation Set**: 11 images (20%)
  - **Testing Set**: 6 images (10%)

## Model Configuration and Training
- **Model**: YOLOv5s
- **Input Image Size**: 416x416 pixels
- **Training Epochs**: 50
- **Batch Size**: 16
- **Confidence Threshold**: 0.5

## Performance Evaluation

### Training Set Results
| Metric            | Value |
|-------------------|-------|
| Precision         | 0.903 |
| Recall            | 0.955 |
| mAP@0.5           | 0.972 |
| mAP@0.5:0.95      | 0.681 |

### Validation Set Results
| Metric            | Value |
|-------------------|-------|
| Precision         | 1.000 |
| Recall            | 0.955 |
| mAP@0.5           | 0.977 |
| mAP@0.5:0.95      | 0.715 |

### Key Observations
- **Perfect precision (1.000)** on the validation set.
- **Consistently high recall (0.955)** across both training and validation.
- Strong generalization despite a relatively small dataset.

### Computational Efficiency
| Metric                       | Time per Image |
|-------------------------------|----------------|
| Preprocessing Time            | 0.1 ms         |
| Inference Time                | 3.5 ms         |
| Non-Maximum Suppression (NMS) | 3.4 ms         |

## Conclusion
We successfully developed a high-performing custom object detection model using YOLOv5s. The project covered all key phases:
- Careful **object selection**
- Strategic **data collection**
- Precise **annotation**
- **Model training** with strong hyperparameter tuning
- Thorough **performance evaluation**

The model demonstrated **high accuracy** and **efficiency**, highlighting the potential of deep learning for custom object detection tasks.

---

### Team
- [Your Team Member Names]

### Tools Used
- Python
- YOLOv5
- makesense.ai
- GeoPandas, OpenCV
- PyTorch

### Repo Structure
```
|- dataset/
|    |- images/
|    |- labels/
|- yolov5s_model/
|- README.md
|- train.py
|- detect.py
|- results/
```

### How to Run
1. Clone the repository.
2. Install dependencies listed in `requirements.txt`.
3. Place the dataset in the appropriate folder.
4. Train the model:
   ```bash
   python train.py --img 416 --batch 16 --epochs 50 --data dataset.yaml --cfg yolov5s.yaml
   ```
5. Run detection on new images:
   ```bash
   python detect.py --weights best.pt --img 416 --source your_image_folder/
   ```

---

Feel free to fork this repo, experiment with different objects, or scale it up for real-world detection tasks!
