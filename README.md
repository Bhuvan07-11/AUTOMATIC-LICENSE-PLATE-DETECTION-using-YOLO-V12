🚗 Automatic License Plate Detection using YOLOv2 & PaddleOCR
📌 Project Overview
With the rapid growth of vehicles and the increasing demand for smart transportation systems, Automatic Number Plate Recognition (ANPR) has become a crucial component in traffic management, parking automation, and law enforcement.
This project implements a deep learning-based ANPR pipeline using:
- YOLOv8 for real-time number plate detection
- PaddleOCR for text recognition
The system is capable of detecting and recognizing license plates from both images and video streams with high accuracy, even under challenging lighting and motion conditions.
<img width="943" height="373" alt="image" src="https://github.com/user-attachments/assets/e37d9d7b-267d-4cde-aaa3-e29ac9328fcc" />

<img width="914" height="161" alt="image" src="https://github.com/user-attachments/assets/6411d7df-8a22-4140-a831-8774468d3e22" />

<img width="932" height="341" alt="image" src="https://github.com/user-attachments/assets/46587217-b103-4fdc-a20e-97fbf5d39f24" />


✨ Features
- 🔍 Accurate Detection: YOLOv12 achieves ~98% detection accuracy
- 🔡 Reliable OCR: PaddleOCR provides ~96% text recognition accuracy
- ⚡ Real-Time Processing: End-to-end pipeline runs on live video feeds
- 📂 Custom Dataset: Built from CCTV footage and annotated using Roboflow
- 📝 Logging: Recognized plates with timestamps are automatically saved

🏗️ System Architecture
The pipeline consists of four main stages:
- Image/Video Input Acquisition – Frames captured via OpenCV
- Number Plate Detection – YOLOv12 localizes plates in frames
- Text Extraction – PaddleOCR reads alphanumeric characters
- Result Visualization & Logging – Outputs bounding boxes + saves text logs
📷 Figure 1: System Overview of Number Plate Detection
  <img width="838" height="283" alt="image" src="https://github.com/user-attachments/assets/1135a17e-b7c5-4bc9-ad30-33a08f0775b7" />


📊 Dataset Preparation
- Vehicle footage recorded via CCTV/video sources
- Frames extracted using OpenCV (~200 images)
- Annotated in Roboflow with bounding boxes labeled as Number Plate
- Dataset split: 80% training, 10% validation, 10% testing
📷 Figure 2: Dataset Images Extracted from CCTV Footage
<img width="903" height="240" alt="image" src="https://github.com/user-attachments/assets/7578e2cd-600c-4d4b-b9bd-14a9266a49ad" />

<img width="798" height="448" alt="image" src="https://github.com/user-attachments/assets/3ff0d0ca-57ef-40f2-a784-73b1b265f8d7" />


⚙️ Methodology
🔹 Model Training
- Framework: Ultralytics YOLOv12
- Environment: Google Colab (T4 GPU)
- Parameters:
- Epochs: 100
- Image Size: 640×640
- Batch Size: 16
- Optimizer: SGD
- Output: best.pt trained weights
🔹 Detection & Recognition
- YOLOv12 detects bounding boxes around plates
- Cropped ROIs passed to PaddleOCR
- Recognized text + timestamps logged automatically

📈 Results
- Detection Accuracy (YOLOv12): 98%
- OCR Accuracy (PaddleOCR): 94%
- End-to-End Accuracy: ~92%
- Robust performance under varying lighting, angles, and motion blur

🛠️ Tech Stack
- Python
- YOLOv8 (Ultralytics)
- PaddleOCR
- OpenCV
- CVZone
- Roboflow (annotation)
- Google Colab (training)

🚀 Applications
- Traffic surveillance & law enforcement
- Automated toll collection
- Parking management systems
- Border control & stolen vehicle tracking

🌍 SDG Alignment
This project supports:
- SDG 9 – Industry, Innovation, and Infrastructure
- SDG 11 – Sustainable Cities and Communities
By promoting AI-driven automation in smart city infrastructure.

📂 Repository Structure
├── dataset/              # Annotated images
├── models/               # Trained YOLOv12 weights (best.pt)
├── src/                  # Source code (YOLOv8 + PaddleOCR integration)
├── results/              # Output logs & screenshots
├── README.md             # Project documentation



📜 LicenseThis project is developed for academic purposes. For reuse or extension, please provide proper citation.
