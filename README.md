# High-Precision Flock Counter

An advanced real-time object-tracking system built with **Streamlit** and **YOLO11**, specifically designed to detect and count birds with high precision.

## Overview
This application provides a user-friendly dashboard to monitor live camera feeds and track individual birds. It leverages the state-of-the-art **YOLO11** object detection model, specifically configured to target bird classes (class index 14), with custom-tuned tracking via the **BoT-SORT** algorithm.

## Features
- **Real-time Streamlit Dashboard**: Web-based interface for live monitoring and interactive controls.
- **AI Sensitivity & Calibration**: Adjustable confidence thresholds and dynamic tripwire alignment.
- **Unique Bird Tracking**: Maintains a global set of unique 	rack_ids with BoT-SORT for accurate cumulative counting.
- **Custom Telemetry**: Real-time performance tracking and inference metrics.
- **Optimized Performance**: Utilizes high_quality_tracker.yaml with optimized BoT-SORT parameters, including ReID and camera motion compensation.

## Demo
https://github.com/user-attachments/assets/4ed087d2-73eb-4c8b-92d0-7e87a0a25c53

## Prerequisites
- Python 3.x
- ultralytics (YOLO11 support)
- opencv-python
- streamlit
- pyyaml

## Usage
Ensure the yolo11n.pt model file is available (automatically downloaded by ultralytics).

Launch the application:

`ash
python -m streamlit run new.py
`

Once running, use the web interface to:
- Select your camera channel.
- Adjust the AI sensitivity (Confidence Threshold) and Tripwire position.
- View live detection metrics and processing speed.

## Technical Highlights
- **Architecture**: Upgraded to **YOLO11** for superior detection accuracy.
- **Tracking Algorithm**: Implements a custom **BoT-SORT** configuration (high_quality_tracker.yaml) featuring:
    - Sparse Optical Flow for camera motion compensation.
    - Appearance-based re-identification (ReID).
    - Optimized thresholding for stable tracking.
- **Pipeline**: High-efficiency frame processing with live Streamlit UI integration.
