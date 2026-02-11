# Real-Time Crowd Detection System 🚶‍♂️🚶‍♀️

## 📌 Project Overview

The **Real-Time Crowd Detection System** is an AI-powered solution designed to identify, count, and monitor people in real time using CCTV or live camera feeds. By leveraging **deep learning** and **computer vision**, the system estimates crowd density, generates heatmaps, and triggers alerts when crowd levels exceed safe limits.

This project is useful for:

* Managing large gatherings
* Preventing overcrowding
* Supporting emergency response
* Enhancing public safety

---

## 🎯 Objective

To develop a scalable and real-time crowd monitoring system that can:

* Detect and count people in live video streams
* Estimate crowd density using density maps
* Highlight overcrowded zones
* Raise alerts when crowd thresholds are exceeded

---

## 📂 Dataset Overview

**Dataset Used:** ShanghaiTech Crowd Counting Dataset

### Dataset Features

* Contains both **high-density** and **low-density** crowd images
* Includes **ground-truth density maps**
* Large variation in scale, perspective, and illumination
* Ideal for training density-estimation models like **CSRNet**

### Key Insights

* Highly crowded scenes require **density-map-based estimation** rather than direct detection
* Significant variation in images makes deep learning essential
* Dataset imbalance exists with fewer low-density scenes

---

## 🧠 Methodology

1. Capture video from CCTV or webcam
2. Extract frames in real time
3. Preprocess frames (resize, normalize)
4. Pass frames through deep learning model (CSRNet / YOLO)
5. Generate density maps and crowd count
6. Detect overcrowding and raise alerts
7. Display results on a live dashboard

---

## 🔍 Exploratory Data Analysis (EDA)

* Wide range of crowd densities observed
* Dense scenes show concentrated point annotations
* Large variations in lighting and camera angles
* Dataset imbalance identified

**EDA helped in:**

* Understanding model limitations
* Improving preprocessing techniques
* Fine-tuning model architecture

---

## 📊 Visualization

* Original input frame
* Predicted density map (heatmap overlay)
* Live crowd count display
* Highlighted overcrowded zones

---

## ⚙️ Data Preprocessing

* Frame extraction from video
* Image resizing (e.g., 640×480)
* Pixel value normalization
* Noise removal and brightness adjustment
* Conversion to tensor format
* Data augmentation techniques:

  * Rotation
  * Cropping
  * Scaling
  * Flipping

---

## 🧩 Feature Extraction

* **Low-level features:** edges, corners, textures, density variations
* **High-level features (CNN):**

  * Human shapes
  * Repetitive patterns
  * Scale variations in dense crowds

The model focuses on **density-rich regions** for accurate people counting.

---

## 🏗️ Model Architecture

**Model Used:** CSRNet (Congested Scene Recognition Network)

### Components

* **Frontend:** Pre-trained VGG16 (layers 1–10)
* **Backend:** Dilated convolution layers
* **Output:** Density map representing people distribution

### Why CSRNet?

* Excellent performance in highly crowded scenes
* No need for bounding boxes
* Handles scale and perspective variations effectively

---

## 🏋️ Training and Evaluation

### Training Details

* Loss Function: Mean Squared Error (MSE)
* Optimizer: Adam
* Trained for multiple epochs on ShanghaiTech dataset

### Evaluation Metrics

* MAE (Mean Absolute Error)
* MSE (Mean Squared Error)
* Visual accuracy of density maps

### Training Results

* Smooth loss convergence
* Accurate density estimation
* Good generalization on test images

---

## ✅ Results

* Real-time crowd detection achieved
* High accuracy in high-density scenes
* Robust performance under varying lighting conditions
* Clear density heatmaps generated
* Live dashboard displays crowd count
* Overcrowding alerts triggered correctly

---

## 🖥️ User Interface

* Live video feed
* Crowd count display
* Heatmap overlay
* Overcrowding alerts

---

## ⚠️ Challenges

* Extremely dense crowds
* Lighting variations in real-time videos
* Motion blur from moving people
* Maintaining real-time performance on CPU
* Occlusion-heavy scenes
* OpenCV and NumPy compatibility issues
* Webcam access restrictions in Streamlit Cloud

---

## 🔮 Future Scope

* Drone-based aerial surveillance
* Multi-camera crowd tracking
* Predictive analytics for crowd growth
* Integration with smart city systems
* GPU optimization for faster processing
* SMS/Email alert system
* 3D crowd analysis using depth sensors

---

## 🏁 Conclusion

This project demonstrates a **real-time AI-based crowd detection system** capable of estimating crowd density, generating heatmaps, and triggering alerts in overcrowded situations. It is scalable and adaptable for deployment in:

* Malls
* Railway stations
* Public events
* Smart city infrastructure

---

## 🙏 Acknowledgements

* ShanghaiTech Crowd Counting Dataset
* Open-source deep learning frameworks

---

⭐ *If you like this project, don’t forget to star the repository!*
