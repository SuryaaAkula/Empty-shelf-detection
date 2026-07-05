# Empty-shelf-detection
# YOLOv8 Empty Shelf Detection System

![YOLOv8 Logo](https://docs.ultralytics.com/assets/img/yolov8-banner.png)

This project implements an **Empty Shelf Detection System** using the **YOLOv8** object detection model. It detects empty regions on retail shelves from images and videos, helping with inventory management, stock monitoring, and retail automation.

---

<details>
<summary><strong>📌 Features</strong></summary>

- Custom YOLOv8n model trained on a custom empty shelf dataset.
- Model evaluation using Precision, Recall, mAP50 and mAP50-95.
- Training visualization (loss curves, confusion matrix, PR curve).
- Image and video inference.
- Bounding box visualization.
- Easy GitHub deployment with `requirements.txt`.

</details>

---

<details>
<summary><strong>🚀 Getting Started</strong></summary>

### Prerequisites

- Google Colab (Recommended)
- Google Drive
- Python 3.9+

### Dataset Setup

1. Prepare dataset in YOLO format.
2. Organize as:

```
train/
    images/
    labels/

val/
    images/
    labels/

test/
    images/
    labels/
```

3. Upload dataset to:

```
MyDrive/YOLO_Videos/dataset/dataset/
```

4. Place inference videos inside:

```
MyDrive/YOLO_Videos/
```

### Installation

```bash
pip install -r requirements.txt
```

### Running the Notebook

1. Open the notebook in Google Colab.
2. Mount Google Drive.
3. Run all notebook cells.

</details>

---

<details>
<summary><strong>📂 Project Structure</strong></summary>

```text
yolo-empty-shelf-detection/
│
├── README.md
├── empty_shelf_detection.ipynb
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── images/
│   └── labels/
│
├── videos/
│
├── runs/
│   ├── detect/
│   ├── train/
│   └── predict/
│
└── assets/
```

### Note

Avoid uploading:

- Dataset
- Trained weights (`best.pt`)
- `runs/` folder

Instead:

- Share download links.
- Use Git LFS for model weights.
- Add large files to `.gitignore`.

</details>

---

<details>
<summary><strong>📊 Results</strong></summary>

### Validation

| Metric | Value |
|--------|------:|
| mAP50 | **0.982** |
| mAP50-95 | **0.511** |

### Test

| Metric | Value |
|--------|------:|
| Precision | **0.985** |
| Recall | **0.967** |
| mAP50 | **0.987** |
| mAP50-95 | **0.475** |

Training plots and prediction examples are generated automatically by the notebook.

</details>

---

<details>
<summary><strong>🎯 Usage & Inference</strong></summary>

After training:

1. Load the trained `best.pt` model.
2. Provide an image or video.
3. Run inference.
4. Output files are saved inside:

```
runs/detect/predict-*/
```

</details>

---

<details>
<summary><strong>🔮 Future Work</strong></summary>

- Better data augmentation
- Experiment with YOLOv8m/YOLOv8l
- Real-time camera deployment
- Error analysis
- Quantity estimation
- Web/Desktop dashboard

</details>

---

