# AI-Proctoring-System
AI-powered proctoring system using Face Recognition, YOLOv8, and Gaze Tracking to detect cheating in real-time.

It includes:
👤 Face Recognition (Dataset-based)
👥 Multiple Person Detection
📱 Mobile Phone Detection (YOLOv8)
👀 Gaze Tracking
📸 Evidence Capture System
🧠 Features

✔ Face authentication using dataset
✔ Auto-exit on unauthorized face
✔ Capture cheating screenshots
✔ Detect multiple persons
✔ Detect phone usage
✔ Detect looking away (gaze tracking)
✔ Dataset creation tool (collect_faces.py)

🛠️ Technologies Used
• Python
• OpenCV
• face_recognition
• NumPy
• MediaPipe
• Ultralytics YOLOv8

📦 Requirements
Install dependencies:
-> pip install opencv-python face-recognition numpy mediapipe ultralytics

📁 Project Structure
AI-Proctoring-System/
│
├── dataset/                # Face dataset
│   ├── Person1/
│   │   ├── img1.jpg
│   │   ├── img2.jpg
│   │
│   ├── Person2/
│
├── cheating/               # Auto-created (stores evidence)
│
├── yolov8n.pt              # YOLO model
├── main.py                 # Main proctor system
├── collect_faces.py        # Dataset creation script
├── requirements.txt
└── README.md

📸 Step 1: Create Dataset (IMPORTANT)
Run:
-> python collect_faces.py

👉 How it works:
1.Enter your name
2.Webcam will open
3.Press S key to capture image
4.Images are saved automatically in:
- dataset/YourName/
5.Press Q to exit
  
✔ Capture 3–5 images
✔ Use different angles
✔ Keep good lighting

▶️ Step 2: Run AI Proctor System
- python main.py
Press Q to exit

⚙️ System Working
🔹 1. Dataset Loading
      • Loads images from dataset/
      • Converts into face encodings
🔹 2. Face Recognition
        • Matches live face with dataset
        • If mismatch:
          · Marked as "Unknown"
          · Exit after 3 attempts
🔹 3. YOLO Object Detection
    Detects:
  👤 Person
  📱 Mobile Phone
🔹 4. Gaze Detection
      • Uses MediaPipe Face Mesh
      • Detects:
        · Left
        · Right
        · Center

📂 Output (Evidence)
All cheating screenshots are saved in:
- cheating/
   phone_101523.jpg
   multiple_101530.jpg
   gaze_101540.jpg
   unknown_face_101550.jpg

⚠️ Important Notes
• Webcam must be enabled
• Keep proper lighting
• YOLO model file must be present
• Face recognition may fail in low light

📄 requirements
• opencv-python
• face-recognition
• numpy
• mediapipe
• ultralytics


👨‍💻 Author
MOHAMMAD FAIZAN
Computer Engineering Student
