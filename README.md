<div align="center">

# 🛡️ AEGIS

### AI-Powered Military Object Detection System

**Real-time detection of military assets using deep learning.**
*Enhancing surveillance — with intelligence and precision.*

</div>

---

## 📋 Table of Contents

1. [What is Aegis?](#-what-is-aegis)
2. [The Problem](#-the-problem)
3. [The Solution](#-the-solution)
4. [How It Works](#-how-it-works)
5. [Dataset](#-dataset)
6. [Tech Stack](#-tech-stack)
7. [Quick Start](#-quick-start)
8. [Workflow](#-workflow)
9. [Results](#-results)
10. [Future Scope](#-future-scope)
11. [Team](#-team)

---

## 🚀 What is Aegis?

**Aegis** is an AI-based object detection system built using **YOLOv8** that can identify military and civilian objects from images and video streams in real time.

It is designed for applications such as:

* Surveillance
* Threat detection
* Battlefield awareness

---

## ❗ The Problem

Modern surveillance systems face several challenges:

| Problem              | Limitation                           |
| -------------------- | ------------------------------------ |
| Manual monitoring    | Slow and error-prone                 |
| Traditional systems  | Lack real-time intelligence          |
| Complex environments | Difficult to detect multiple objects |
| Human dependency     | Risky in defense scenarios           |

---

## 💡 The Solution

Aegis uses **deep learning (YOLOv8)** to automatically detect objects in a single pass.

### Key Idea:

* Input: Image / Video frame
* Model processes frame
* Output: Detected objects with bounding boxes and labels

This enables:

* Fast detection
* Multi-object recognition
* Real-time processing

---

## ⚙️ How It Works

```
[Input Image/Video] → [YOLOv8 Model] → [Object Detection] → [Output with Labels]
```

### Step-by-Step:

1. Load pre-trained YOLOv8 model
2. Train on custom military dataset
3. Model learns object features
4. Detect objects in new images
5. Display results with bounding boxes

---

## 📊 Dataset

* **Dataset:** Military Object Detection Dataset (Ryan Madhuwala)
* **Total Images:** 26,315

| Split      | Images |
| ---------- | ------ |
| Training   | 21,978 |
| Validation | 2,941  |
| Testing    | 1,396  |

### Classes (12):

camouflage_soldier, weapon, military_tank, military_truck, military_vehicle,
civilian, soldier, civilian_vehicle, military_artillery, trench,
military_aircraft, military_warship

---

## 🖥️ Tech Stack

| Layer     | Technology           |
| --------- | -------------------- |
| Language  | Python               |
| Model     | YOLOv8 (Ultralytics) |
| Framework | PyTorch              |
| Vision    | OpenCV               |

---

## ⚡ Quick Start

### 🔹 Installation

```bash
git clone https://github.com/your-username/aegis.git
cd aegis
pip install ultralytics opencv-python
```

---

### 🔹 Training

```python
from ultralytics import YOLO

model = YOLO("yolov8m.pt")

model.train(
    data="military_dataset.yaml",
    epochs=25,
    imgsz=640
)
```

---

### 🔹 Prediction

```python
from ultralytics import YOLO

model = YOLO("best.pt")

results = model("test_image.jpg")
results.show()
```

---

## 🔁 Workflow

```
Dataset → Annotation → YOLO Format → Training → Evaluation → Testing
```

---

## 📈 Results

* Successfully detects multiple military objects
* Works on both images and video
* Moderate accuracy (improves with training and data)

---

## 🔮 Future Scope

* Improve accuracy with more data
* Deploy on Raspberry Pi
* Integrate with drones for surveillance
* Add GPS-based tracking system
* Real-time battlefield monitoring

---

## 🤝 Team

* Ritesh Rawat
* Yuvraj Kabadwal

---

<div align="center">
  <i>Building intelligent systems for smarter surveillance.</i>
</div>
