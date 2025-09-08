Real-Time Human Pose Detection using YOLOv8
This project uses the Ultralytics YOLOv8 pose model to perform human pose estimation on a video file. It saves both the full frames and cropped images of detected persons, and logs keypoints data into a CSV file.
📁 Project Structure
suspicious.mp4              - Input video file
yolo11s-pose.pt             - Pretrained YOLOv8 pose model
images/                     - Folder for full-frame images
images1/                    - Folder for cropped person images
nkeypoint.csv               - Output CSV with keypoint data
notebook.ipynb              - Jupyter notebook (your code)
requirements.txt            - Python dependencies
README.md                   - Project documentation

📦 Requirements
Install required Python libraries using:
pip install -r requirements.txt
🧠 Model Used
YOLOv8 Pose from Ultralytics (https://github.com/ultralytics/ultralytics)
The model detects human body keypoints (e.g., shoulders, elbows, knees) in real time.
🛠️ What It Does
- Loads a video (suspicious.mp4)
- Reads every frame from the video (no skipping)
- Uses YOLOv8 to detect people and their keypoints
- Saves:
  - Full-size frames → images/
  - Cropped detections → images1/
  - Keypoints → nkeypoint.csv

📊 Output Example
images/img_12.jpg: full frame
images1/person_nn_1545.jpg: cropped person
nkeypoint.csv:
image_name, x0, y0, x1, y1, ..., x16, y16
person_nn_1545.jpg, 0.34, 0.12, ..., 0.89, 0.77

🧪 How to Run (Notebook)
1. Launch the Jupyter Notebook:
   jupyter notebook

2. Open the provided notebook (e.g., pose_detect.ipynb or similar).

3. Run the code. It will:
   - Process the video
   - Save images
   - Generate nkeypoint.csv

📍 Notes
- You can change the confidence threshold (default: 0.5) to control the detection sensitivity.
- For larger or more accurate models, try yolov8m-pose.pt or yolov8l-pose.pt.

🤖 Future Enhancements
- Real-time webcam detection
- Action recognition based on keypoints
- Visualize skeletons on saved frames

👨‍💻 Author
- swayam sidgor
- akshat pandey
- risabh tadwal
- krishnakant mehra
- Project from MANIT Bhopal Internship (BFBF)
