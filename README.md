# comaparative analysis of deepsort vs bytesort on mot 17 benchmark

A rigorous side-by-side evaluation of two state-of-the-art multi-object tracking (MOT) algorithms — **DeepSORT** and **ByteTrack** — benchmarked on the MOT17 dataset using industry-standard metrics.

---

##  Overview

Multi-object tracking (MOT) is a core challenge in computer vision. This project compares:

| Algorithm | Core Approach |
|-----------|--------------|
| **DeepSORT** | Kalman filter + deep appearance features (Re-ID) |
| **ByteTrack** | Tracks every detection box, including low-confidence ones |

The goal is to understand when each algorithm excels and what trade-offs exist in real-world tracking scenarios.

---


## ✨ Features

- ✅ Standard metrics: MOTA, MOTP, IDF1, ID Switches, FP, FN
  
- ✅ Detailed analysis report 

---

## 🛠️ Tech Stack

- **Language:** Python 3.9+
- **Tracking:** DeepSORT, ByteTrack
- **Vision:** OpenCV, PyTorch
- **Evaluation:** py-motmetrics


---

## 📁 Project Structure

```
deepsort-vs-bytetrack-mot17/
│
├── data/                   # MOT17 dataset (download separately)
├── results/                # Output metrics and comparisons
├── notebooks/              # Analysis notebooks
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/SharmaRaj-0605/deepsort-vs-bytetrack-mot17.git
cd deepsort-vs-bytetrack-mot17
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the MOT17 dataset
Get it from [motchallenge.net](https://motchallenge.net/data/MOT17/) and place it in the `data/` folder.

### 4. Run DeepSORT
```bash
python deepsort/run_tracker.py --sequence MOT17-02
```

### 5. Run ByteTrack
```bash
python bytetrack/run_tracker.py --sequence MOT17-02
```

### 6. Evaluate & Compare
```bash
python evaluation/compare_metrics.py
```

---

## 📷 Sample Output


<img width="1717" height="956" alt="image" src="https://github.com/user-attachments/assets/c0df0e30-527b-42ed-b3bb-a4d11f3ebf0a" />

---

## 📄 References

- [DeepSORT Paper](https://arxiv.org/abs/1703.07402)
- [ByteTrack Paper](https://arxiv.org/abs/2110.06864)
- [MOT17 Challenge](https://motchallenge.net/data/MOT17/)
