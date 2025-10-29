# panoramic-stitching-opencv

# Image Stitching &amp; Panorama Generation using OpenCV (SIFT Feature Detection)
# 🧠 Panoramic Stitching with OpenCV
Image Stitching & Panorama Generation using SIFT and ORB Feature Detection
📸 Overview

This project demonstrates automatic image stitching and panorama generation using OpenCV in Python. The implementation compares two feature detection algorithms — SIFT (Scale-Invariant Feature Transform) and ORB (Oriented FAST and Rotated BRIEF) — to evaluate their performance and stitching quality.

# ⚙️ Objectives

Implement a Python-based panoramic stitching pipeline.

Compare the feature detection capabilities of SIFT and ORB.

Visualize feature matches and homography estimation.

Generate smooth panoramic outputs from overlapping images.

# 🧩 Tools & Libraries

Python 3.13

OpenCV (cv2)

NumPy

Pillow (PIL)

# 🗂️ Project Structure
panoramic-stitching-opencv/
│
├── scripts/
│   ├── stitch_pano.py          # Base stitching script
│   └── stitch_compare.py       # Comparison script for SIFT vs ORB
│
├── input/
│   ├── Street_Pano/            # Street panorama image set
│   └── SF_Pano/                # San Francisco panorama image set
│
├── results/
│   ├── pano_sift.jpg           # Panorama created using SIFT
│   ├── pano_orb.jpg            # Panorama created using ORB
│   ├── pano_sift_pair_matches.jpg  # SIFT feature matches
│   ├── pano_orb_pair_matches.jpg   # ORB feature matches
│   └── panorama_bridge.jpg         # Additional Golden Gate panorama
│
└── README.md
