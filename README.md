# 🚨 Real-Time Panic Detection System using Computer Vision

A real-time **panic and abnormal crowd behavior detection system** built using **Computer Vision, Optical Flow, and YOLO**.  
The system detects sudden panic situations by analyzing **motion intensity, direction changes, and velocity anomalies** from CCTV or video feeds.

---
Problem Statement
In crowded public spaces (stations, malls, religious events), panic situations escalate within seconds and often go unnoticed until damage occurs.  
This project aims to **automatically detect panic-like behavior early** using live camera feeds, enabling faster intervention.

Solution Overview
This system combines:
- **Human detection** using YOLO
- **Motion analysis** using Optical Flow
- **Behavioral heuristics** to detect panic

If there is:
- Sudden spike in motion velocity  
- Abrupt direction changes  
- Abnormal crowd flow  

The system raises a **panic alert**.

Tech Stack
- **Python**
- **OpenCV**
- **YOLO (Ultralytics)**
- **Optical Flow (Farneback)**
- **NumPy**
- **Real-time video processing**
  
System Architecture
1. Video Input
   - CCTV feed / recorded video / webcam
2. Human Detection
   - YOLO detects people in each frame
3. Motion Analysis
   - Optical Flow calculates movement vectors
4. Panic Detection Logic
   - Sudden velocity or direction change triggers panic
5. Alert Syste
   - Visual / audio alerts (configurable)

Features
- Real-time processing
- Works on CCTV and live webcam
- Lightweight and fast
- Modular panic logic (easy to tune)
- No training required (rule-based + CV)

Installation
```bash
git clone https://github.com/jinay-k-jain/Panic_detector_CCTV.git
cd Panic_detector_CCTV/test3
pip install -r requirements.txt
```
Run on Video File
python main.py --video path/to/video.mp4

Project Structure
├── main.py              
├── alarm.py             
├── requirements.txt     
├── assets/              
├── README.md

Panic Detection Logic (High Level)
Track optical flow between frames
Measure:
Average motion magnitude
Direction variance
If values cross a threshold → panic detected
Thresholds are configurable inside the code.

**Limitations:** 
Rule-based (not deep behavioral learning)
Extreme camera shake may cause false positives
Works best in medium-to-high crowd density

Future Improvements
ML-based behavior classification
Crowd density heatmaps
Integration with control rooms
Automatic alert dispatch to authorities
Edge deployment (Jetson / CCTV NVRs)

**Use Case**
Public events
Railway stations
Religious gatherings
Stadiums
Malls & metros


Author: 
Jinay Jain
B.Tech, IIT (ISM) Dhanbad
Smart India Hackathon Winner
