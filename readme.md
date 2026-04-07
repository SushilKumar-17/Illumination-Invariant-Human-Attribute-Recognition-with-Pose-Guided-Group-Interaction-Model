

# Context-Aware Public-Space Safety Monitoring

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/YOLOv5-FFCC00?style=for-the-badge&logo=darkreader&logoColor=black"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/DeepSORT-0A192F?style=for-the-badge&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-FA8C16?style=for-the-badge&logo=jupyter&logoColor=white"/>
</p>

**Context-Aware Public-Space Safety Monitoring** is a real-time intelligent surveillance framework designed to transform traditional CCTV systems into assistive decision-support systems.

Unlike conventional systems that only record video, this framework integrates **person detection, multi-object tracking, attribute recognition, and contextual reasoning** to generate **interpretable safety cues** for human operators.

Developed as an academic research project, the system focuses on **assistive surveillance**, ensuring ethical deployment by avoiding:

- Identity recognition
- Crime prediction
- Autonomous enforcement

---

## Problem Motivation

Traditional CCTV systems:

- Require continuous human monitoring
- Lead to **operator fatigue** and missed events
- Provide **raw data without interpretation**

This project addresses the gap between:

> **Detection → Understanding → Actionable Insight**

---

## Key Contributions

- **Context-Aware Surveillance Pipeline**
- **Group Composition & Scene Understanding**
- **Real-Time Feed Prioritization**
- **Illumination-Robust Processing**
- **Privacy-Preserving Design (No Identification)**

---

## System Overview

<div align="center">
  <img src="assets/architecture.png" width="500"/>
</div>

The system converts raw video feeds into structured safety indicators through a multi-stage pipeline.

---

## Core Modules

### 1. Visual Intelligence Layer

- **Person Detection**
  - Detects individuals in real-time using deep learning

- **Multi-Object Tracking**
  - Maintains temporal consistency across frames
  - Assigns unique IDs (non-identifiable)

- **Attribute Recognition**
  - Extracts minimal contextual attributes:
    - Gender distribution (aggregate only)
    - Spatial positioning
    - Temporal presence
    - SOS gesture detection

---

### 2. Context Aggregation Layer

Combines multiple signals to build scene-level understanding:

- Crowd density
- Group composition
- Spatial clustering
- Time-of-day context
- Illumination conditions

---

### 3. Context-Aware Risk Modeling

The system constructs a contextual state:
Cf(t) = {Nt, Gt, St, Tt, Lt}

Where:

- Nt → Number of people
- Gt → Gender distribution
- St → Spatial clustering
- Tt → Temporal persistence
- Lt → Lighting condition

---

### 4. Risk Scoring Mechanism

Context is converted into a **priority score (not prediction):**
Rf(t) = w1Gt + w2St + w3Tt + w4Lt

- Uses **rule-based reasoning**
- No probabilistic crime prediction
- Purely assistive signal

---

### 5. Intelligent Feed Prioritization

Feeds are ranked into:

- **High Priority**
- **Medium Priority**
- **Normal**

With temporal smoothing:

- Uses **rule-based reasoning**
- No probabilistic crime prediction
- Purely assistive signal

---

### 5. Intelligent Feed Prioritization

Feeds are ranked into:

- **High Priority**
- **Medium Priority**
- **Normal**

With temporal smoothing:
R̄f(t) = average over sliding window

✔ Reduces false alarms  
✔ Avoids noise spikes  
✔ Ensures stability

---

### 6. Operator Support Interface

- Highlights important feeds
- Reduces cognitive overload
- Keeps **human-in-the-loop decision making**

---

## System Pipeline

<div align="center">
  <img src="assets/pipeline.png" width="1000"/>
</div>

**Flow:**

1. Multi-CCTV Input
2. Detection + Tracking
3. Attribute Extraction
4. Context Formation
5. Risk Scoring
6. Feed Prioritization
7. Operator Dashboard

---

## Performance Summary

| Metric                    | Value   |
| ------------------------- | ------- |
| Detection Accuracy (mAP)  | 92.4%   |
| Tracking Stability (MOTA) | 88.7%   |
| Attribute Accuracy        | 90.1%   |
| Processing Speed          | ~24 FPS |
| Low-Light Retention       | 85%     |

✔ Stable real-time performance  
✔ Works under varying illumination  
✔ Reduces unnecessary alerts (~17%)

---

## Key Advantages

- Converts **raw detection → meaningful insights**
- Reduces **operator fatigue**
- Maintains **ethical boundaries**
- Works in **real-time multi-feed environments**
- Supports **proactive monitoring without prediction**

---

## Ethical Considerations

This system is intentionally designed to be:

- ❌ No facial recognition
- ❌ No identity tracking
- ❌ No crime prediction
- ❌ No behavioral profiling

✔ Only **contextual interpretation for assistance**

---

## Applications

- Smart city surveillance systems
- Campus safety monitoring
- Public transport hubs
- Traffic and crowd monitoring
- Security control rooms

---

## Limitations

- Requires calibration for different environments
- Performance affected in:
  - Extreme low-light
  - Heavy occlusion
  - Dense crowds
- Uses heuristic thresholds (not adaptive learning yet)

---

## Future Work

- Adaptive threshold learning
- Cross-environment generalization
- Improved dense crowd tracking
- Edge deployment optimization

---

## Demonstration

<div align="center">
  <img src="assets/vid.gif" width="800" alt="Video">
</div>

---

## Contributors

- **Sushil Kumar Patra** 
- Sushant Mahajan
- Parth Atal
- Vansh Rana
- Preeti Khera

---

## License

This project is developed for academic and research purposes.

Unauthorized reproduction, modification, or distribution is strictly prohibited without permission.

---
