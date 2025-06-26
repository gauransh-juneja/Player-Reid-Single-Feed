# Player Re-Identification in a Single Camera Feed 🎥🧠

## 📌 Objective
This project aims to identify and track players in a single 15-second soccer video using a YOLOv11 object detection model and a basic centroid-based tracking system. The goal is to maintain consistent player identities even as they move or reappear.

## 🚀 How It Works
- **Detection:** Uses a fine-tuned YOLOv11 model to detect players in each frame.
- **Tracking:** Assigns unique IDs using centroid distance tracking.
- **Visualization:** Displays bounding boxes with player IDs over the video.

## 🧰 Requirements
- Python 3.x
- Ultralytics
- OpenCV
- Google Colab (recommended)

## 🗂 Files
- `Player Re-Identification.ipynb`: Main script with detection + tracking
- `yolo_reid.pt`: Trained YOLOv11 model ([Download Link](https://drive.google.com/file/d/1-5fOSHOSB9UXyP_enOoZNAMScrePVcMD/view))
- `15sec_input_720p.mp4`: Video file ([Download Link](https://drive.google.com/drive/folders/1Nx6H_n0UUI6L-6i8WknXd4Cv2c3VjZTP?usp=sharing))
- `report.md`: Brief write-up of methodology

## ▶️ Running the Code
You can run the code on Google Colab:
1. Upload `yolo_reid.pt` and `15sec_input_720p.mp4`
2. Run `untitled3.py` cell-by-cell

## 📌 Notes
- This is a baseline solution using centroid distance.
- It works well for short videos, but may struggle when players disappear for too long or move drastically.

## ✍️ Author
Gauransh Juneja
