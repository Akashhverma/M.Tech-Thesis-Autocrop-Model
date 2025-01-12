# YOLOv8 hCG Auto-Crop Model for Early-Stage Pregnancy Detection

This repository contains the trained YOLOv8 model weights and associated files for performing auto-cropping of Regions of Interest (ROI) in hCG test strips for early-stage pregnancy detection using smartphone images.
The model automatically detects key regions to prepare images for colorimetry-based analysis.

## Project Overview

The goal of this project is to develop a smartphone-based system that can detect hCG concentration for early-stage pregnancy detection. The project involves:

1-Building an object detection model using YOLOv8 to detect and crop Regions of Interest (ROI) in hCG test strips.
2-Performing colorimetry analysis using image processing techniques (RGB and HSV) for qualitative and quantitative detection.
3-Ensuring high accuracy and reliability in detecting critical regions to enhance the system's performance in real-world applications.

### Files Included--

best.pt: Trained YOLOv8 model weights file.
dataset.yaml: Dataset configuration file used for model training.
predict.py: Python script for running predictions on new images.
README.md: Project documentation file.

### How to Use the Model--

#### 1️⃣ Clone the Repository
git clone https://github.com/Akashhverma/M.Tech-Thesis-Autocrop-Model.git
cd M.Tech-Thesis-Autocrop-Model

#### 2️⃣ Install Required Libraries
Make sure you have Python 3.8+ installed.
Run the following command to install the required libraries:
pip install ultralytics

#### 3️⃣ Run Inference on New Images
You can run the model on a new image using the predict.py script or directly through Python.

### Using the predict.py Script:
python predict.py --source path_to_image.jpg

from ultralytics import YOLO

#### Load the model
model = YOLO('best.pt')

#### Run inference
results = model.predict(source='path_to_image.jpg', save=True)

#### Display the results
results.show()
![1000miuN(25)](https://github.com/user-attachments/assets/aeaae47d-1a2f-4bff-8494-c25c0efff0cd)

## 📈 Model Performance
The model was trained on a custom dataset of 850+ images and achieved the following performance metrics:

F1 Score: 0.97
Precision: 97.2%
Recall: 96.0%
mAP@50: 97.3%
These results demonstrate the model's high accuracy in detecting key regions in test strips.

### Use Cases--

Early-stage pregnancy detection using smartphone-captured images.
Colorimetry-based analysis for detecting faint test lines that are hard to interpret visually.
Automated image preprocessing to prepare images for further analysis.

### Future Work--

Improve the colorimetry analysis by refining the RGB and HSV detection methods.
Integrate the system into a user-friendly mobile application.
Enhance the model's performance across varying lighting conditions and smartphone devices.

### 📧 Contact--
For any questions or collaboration opportunities, feel free to contact me:
Name: Akash Verma
Email: [akashverma3572@gmail.com]
GitHub: [https://github.com/Akashhverma]
LinkedIn: [https://www.linkedin.com/in/akash-verma-525a88145/]






