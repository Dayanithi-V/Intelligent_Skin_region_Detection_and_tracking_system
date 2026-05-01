# 🧠 Intelligent Skin Region Detection & Tracking System

> 🚀 A computer vision project that detects and segments human skin regions from images and real-time video using color-space-based techniques.

---

## 📌 Introduction

Skin detection is a fundamental task in computer vision, widely used in applications such as **face recognition, gesture detection, surveillance, and human-computer interaction**.

This project implements an efficient and lightweight approach using **HSV and YCbCr color spaces** to accurately identify skin pixels under different conditions.

---

## 🎯 Objectives

* Detect skin regions from images and video streams
* Improve detection accuracy using multiple color spaces
* Compare predicted results with ground truth masks
* Enable real-time skin detection using webcam

---

## ⚙️ System Workflow

```id="workflow1"
Input Image / Webcam
        ↓
   Preprocessing
        ↓
Color Space Conversion (HSV + YCbCr)
        ↓
   Skin Segmentation
        ↓
   Mask Refinement
        ↓
   Evaluation & Output
```

---

## 🧠 Core Concept

Instead of using RGB (which is sensitive to lighting), this project uses:

* **HSV (Hue, Saturation, Value)** → Better color separation
* **YCbCr (Luminance + Chrominance)** → Handles lighting variations

👉 Combining both improves detection accuracy significantly.

---

## 🛠️ Tech Stack

| Category         | Tools Used   |
| ---------------- | ------------ |
| Language         | Python       |
| Image Processing | OpenCV       |
| Numerical Ops    | NumPy        |
| Visualization    | Matplotlib   |
| Evaluation       | Scikit-learn |

---

## 📂 Project Structure

```id="structure1"
ipcv_project/
│── dataset/
│   ├── Pratheepan_Dataset/
│   ├── Ground_Truth/
│
│── skin_detection_hsv_ycbcr.ipynb
│── README.md
```

---

## 🔬 Methodology

### 🔹 1. Preprocessing

* Resize input image
* Apply Gaussian blur to reduce noise
* Enhance image quality

---

### 🔹 2. Skin Detection

* Convert image to:

  * HSV color space
  * YCbCr color space
* Apply thresholding to extract skin pixels

---

### 🔹 3. Mask Refinement

* Remove unwanted noise
* Apply morphological operations
* Improve segmentation quality

---

### 🔹 4. Evaluation Metrics

| Metric     | Description                               |
| ---------- | ----------------------------------------- |
| Accuracy   | Correct predictions                       |
| IoU        | Overlap between prediction & ground truth |
| Dice Score | Similarity measure                        |

---

## 🎥 Real-Time Detection

The system uses OpenCV webcam capture:

```python id="code1"
cap = cv2.VideoCapture(0)
```

👉 Detects skin regions live from camera input

---

## 📊 Output Results

* 🖼️ Original Image
* 🎯 Detected Skin Mask
* 🧾 Ground Truth Mask

---

## ⚠️ Challenges

* Sensitive to lighting conditions
* Similar color backgrounds may cause false detection

---

## 🚀 Future Enhancements

* Deep Learning (CNN / U-Net) based segmentation
* Better illumination handling
* Mobile & real-time optimization

---

## 🧪 How to Run

### 1️⃣ Clone Repository

```bash id="run1"
git clone https://github.com/Dayanithi-V/Intelligent_Skin_region_Detection_and_tracking_system.git
cd Intelligent_Skin_region_Detection_and_tracking_system
```

---

### 2️⃣ Install Dependencies

```bash id="run2"
pip install numpy opencv-python matplotlib scikit-learn notebook
```

---

### 3️⃣ Run Project

```bash id="run3"
python -m notebook
```

👉 Open notebook → Run all cells

---

## 💡 Key Highlights

✔ Lightweight (no deep learning required)
✔ Real-time capable
✔ Uses dual color-space approach
✔ Easy to understand & implement

---

## 👨‍💻 Author

**Dayanithi V**
📧 [230701064@rajalakshmi.edu.in](mailto:230701064@rajalakshmi.edu.in)

---

## ⭐ Conclusion

This project demonstrates how classical image processing techniques can effectively solve real-world problems like skin detection without requiring heavy models.

---

## 🙌 Acknowledgment

Developed as part of academic learning in **Image Processing & Computer Vision**.
