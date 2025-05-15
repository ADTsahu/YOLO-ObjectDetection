# YOLO-ObjectDetection
Here is your `README.md` file written in **GitHub-friendly Markdown** format—ready to be used in a GitHub repository for your YOLOv8 project:

---

```markdown
# 🚀 YOLOv8 Custom Object Detection

This repository demonstrates training, validating, and performing inference using a **custom object detection model** with **YOLOv8** from [Ultralytics](https://github.com/ultralytics/ultralytics). Built and tested in Google Colab.

---

## 📂 Repository Structure

```

YOLOv8-Custom/
├── data/
│   ├── images/
│   ├── labels/
│   └── data.yaml
├── runs/
│   └── detect/
├── Yolov8.ipynb
└── README.md

```

---

## ⚙️ Environment Requirements

This notebook runs in **Google Colab** with GPU. All libraries are installed within the notebook.

**Core Dependencies:**
- Python ≥ 3.8
- `ultralytics==8.0.20`
- `opencv-python`
- `matplotlib`
- `PIL` (Python Imaging Library)

---

## 🚀 Setup Instructions

1. **Upload your dataset** to Google Drive with the following structure:
```

data/
├── train/
│   ├── images/
│   └── labels/
├── val/
│   ├── images/
│   └── labels/
└── data.yaml

````

2. **Open `Yolov8.ipynb` in Google Colab**

3. **Mount Google Drive** in the notebook:
```python
from google.colab import drive
drive.mount('/content/drive')
````

4. **Install YOLOv8**:

```bash
!pip install ultralytics==8.0.20
```

---

## 🧠 Training the Model

Use the following command in the notebook:

```bash
!yolo task=detect mode=train model=yolov8s.pt data=data.yaml epochs=25 imgsz=224 plots=True
```

* `model=yolov8s.pt`: Use the YOLOv8-small base model
* `epochs=25`: Number of training epochs
* `imgsz=224`: Image input size
* `plots=True`: Save training plots and metrics

---

## ✅ Model Validation

Evaluate model performance with:

```bash
!yolo task=detect mode=val model=runs/detect/train5/weights/best.pt data=data.yaml
```

---

## 🔍 Inference on Custom Images

Run predictions on test images:

```bash
!yolo task=detect mode=predict model=runs/detect/train5/weights/best.pt conf=0.5 source=your/test/images/path
```

* `conf=0.5`: Confidence threshold for detection

---

## 📊 Outputs and Visualizations

* `results.png`: Training performance graphs
* `confusion_matrix.png`: Model classification confusion matrix
* `val_batch0_pred.jpg`: Sample prediction visual from validation set

Use the provided OpenCV + Matplotlib code to:

* Draw bounding boxes
* Label predictions with confidence scores
* Visualize predictions in the notebook

---

## 📌 Notes

* Use Google Colab with **GPU runtime**:
  `Runtime > Change runtime type > Hardware Accelerator > GPU`
* You can try different YOLOv8 variants like `yolov8n.pt`, `yolov8m.pt`, etc.
* Ensure `data.yaml` correctly references class names and image directories.

---

## 👩‍💻 Author

**Aditi Sahu**
[LinkedIn](linkedin.com/in/aditi-sahu-5b5265287) | 

---

## 📜 License

This project is for educational purposes. Refer to the [Ultralytics License](https://github.com/ultralytics/ultralytics/blob/main/LICENSE) for usage rights.

---

```

---

You can now:
1. Save this as `README.md` in your GitHub repository.
2. Preview it directly on GitHub—it’s fully Markdown-compatible.

Let me know if you want help pushing this to GitHub or linking to datasets, notebooks, or output images.
```
