# Understanding Affective Responses Through Design Style Detection
## 📖 Project Overview
User interface elements have enabled the giving of various users’ sensibility about websites and applications, but current work offers limited connection between these UIs and affective computing. In this work, our study detects the user interface elements with YOLOv8, and identifies the design styles such as edge types and colors using OpenCV. 
Furthermore, we analyze the users’ affective responses based on User Experience Questionnaire (UEQ-S) survey about visual styles in user interface elements. 
Our work helps designers supplement the perspective of a new design space, and this new design perspective gives a visually comfortable experience to people.

## 📊 Dataset
- VINS: Visual Search for Mobile User Interface Design(https://github.com/sbunian/VINS)
  - training : 3,580 / validation : 963

## ✨ Key Features
- YOLOv8: Detects UI elements in user interfaces
- OpenCV: Extracts edge types (sharp-angled/curved) and color palettes based on hue-pie classification

## ⚙️ Dependency
```bash
conda create -n yolo8 python=3.10 -y
conda activate yolo8

pip install ultralytics opencv-python
pip install torch torchvision matplotlib jupyter
pip install ipykernel
python -m ipykernel install --user --name=yolo8 --display-name "Python (yolo8)"
```

## 📂 Folder structure
VINS_DETECTION/
├── vins_detection.ipynb         
├── ui_result.jpg                
├── yolov8n.pt          
├── yolov11n.pt                
│
├── images/                   
├── labels/                      
├── labels_all/                
│
├── runs/
│   └── detect/               
│
└── data.yaml  

## 💻 Code
- The main implementation is provided in `vins_detection.ipynb`

## ✅ Result
- The total mAP is **77.1%** on the validation dataset
<img src = "https://github.com/user-attachments/assets/cd365f47-9bc0-48ae-8a8c-23eab8b95e30">

- The types of elements with confidence score, edge types, and colors
<img src = "https://github.com/user-attachments/assets/fbceef45-cb95-4a02-a66f-a59a9c851b71">
