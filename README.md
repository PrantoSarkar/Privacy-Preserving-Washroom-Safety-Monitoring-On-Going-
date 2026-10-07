 # Privacy-Preserving Real-Time Washroom Safety Monitoring

> 🚧 **Research Status: Ongoing / Manuscript in Preparation**

This repository presents my ongoing research on a privacy-preserving
computer vision system for detecting abnormal washroom occupancy and
potential emergency situations.

The main idea is to avoid placing a camera inside the washroom.
Instead, a camera is positioned outside the washroom and monitors only
entry and exit activity.

## 🔬 Research Problem

Bathrooms and washrooms are high-risk environments, particularly for
elderly people and children.

Traditional camera-based monitoring creates serious privacy concerns,
while wearable devices and additional sensors may depend on user
compliance or require extra hardware.

This research investigates whether abnormal washroom occupancy can be
detected while preserving privacy by monitoring only the doorway.

## 💡 Proposed Approach

The proposed system uses:

- YOLOv8 for person detection
- ByteTrack for multi-object tracking
- Doorway Region of Interest (ROI) analysis
- Entry and exit event detection
- Per-person dwell-time estimation
- Threshold-based abnormal occupancy detection
- Telegram-based emergency alerts

The camera remains outside the washroom and does not capture the private
interior.

## 🏗️ System Pipeline

Camera Input
        ↓
Person Detection - YOLOv8
        ↓
Person Tracking - ByteTrack
        ↓
Doorway ROI Crossing Detection
        ↓
Entry / Exit Recognition
        ↓
Dwell-Time Calculation
        ↓
Normal / Abnormal Occupancy Decision
        ↓
Emergency Alert

## 📊 Current Experimental Work

The current evaluation includes CCTV-style doorway videos representing
different conditions, including:

- Normal short visits
- Prolonged occupancy
- Multiple-person scenarios
- Long-distance detection
- Low-light scenes
- False pass-by cases

The current prototype has been evaluated on 52 videos.

### Current Results

- System-level Accuracy: 84.6%
- Precision: 88.9%
- Recall: 72.7%
- Specificity: 93.3%
- F1 Score: 80.0%
- False Alarm Rate: 6.7%

Tracking performance remained strong across the tested scenarios, while
long-distance and low-light detection remain important challenges.

## 🔒 Privacy-Preserving Design

A key principle of this research is:

**Zero Camera Inside the Washroom**

The system:

- Does not record the washroom interior
- Does not perform face recognition
- Does not transmit private video
- Uses only doorway entry/exit information
- Sends only an emergency notification when abnormal occupancy is detected

## ⚠️ Current Limitations

The current system still has several limitations:

- Reduced detection performance at long distance
- Reduced performance in low-light environments
- Dependence on visible-light camera input
- Possible missed occupancy events when detection fails
- Threshold selection requires further validation

## 🔭 Ongoing Work

Current and future work includes:

- Improving low-light person detection
- Training with additional long-distance samples
- Testing infrared or low-light cameras
- Expanding the evaluation dataset
- Improving dwell-time decision logic
- Deploying the system on an edge device
- Evaluating more complex multi-person scenarios
- Exploring personalized occupancy thresholds

## 🧠 Research Areas

- Computer Vision
- Deep Learning
- YOLO
- Multi-Object Tracking
- ByteTrack
- Privacy-Preserving AI
- Ambient Assisted Living
- Smart Healthcare
- Emergency Detection
- Edge AI

## 📄 Research Status

🚧 Ongoing Research

The manuscript, complete dataset, and final experimental materials are
not publicly released at this stage.

Selected implementation details and research updates may be added as the
work progresses.

## 👨‍💻 Researcher

**Pranta Kumar Sarkar**

Research interests:
Machine Learning, Deep Learning, Computer Vision, NLP and Artificial Intelligence.
