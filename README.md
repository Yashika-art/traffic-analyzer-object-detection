# 🚦 Traffic Analyzer – Object Detection

A computer vision project that detects and counts vehicles in traffic images and videos using **YOLOv8**, then estimates traffic density (Low / Medium / High).

## Problem Statement
Manual traffic monitoring is slow and error-prone. This project automates it by detecting cars, buses, trucks, motorcycles and bicycles, and using the counts to estimate congestion.

## How It Works
```
Input (image / video)
        ↓
Frame extraction (OpenCV)
        ↓
YOLOv8 detector (pretrained on COCO)
        ↓
Filter vehicle classes + count per class
        ↓
Traffic density level (Low / Medium / High)
        ↓
Annotated output + summary chart
```

## Tech Stack
- Python
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- OpenCV
- Matplotlib
- Google Colab

## How to Run
1. Open `Traffic_Analyzer_Object_Detection.ipynb` in [Google Colab](https://colab.research.google.com) (File → Upload notebook).
2. Click **Runtime → Run all**.
3. Upload a traffic image (and optionally a short `.mp4` video) when prompted.
4. View the detections, vehicle counts and traffic density.

## Density Rules
| Total vehicles | Density |
|----------------|---------|
| Less than 10   | Low     |
| 10 to 24       | Medium  |
| 25 or more     | High    |

## Results
The pretrained YOLOv8n model detects vehicles without extra training and produces annotated images, per-class counts and a density estimate.

## Future Improvements
- Fine-tune on a local traffic dataset
- Add object tracking (ByteTrack) to count unique vehicles
- Estimate vehicle speed
- Detect traffic violations

## Author
Yashika
