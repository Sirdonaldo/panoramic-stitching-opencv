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

## 📁 Project Structure

```text
panoramic-stitching-opencv/
├── scripts/
│   ├── stitch_pano.py              # Base stitching script
│   └── stitch_compare.py           # Comparison script for SIFT vs ORB
│
├── input/
│   ├── Street_Pano/                # Street panorama image set
│   │   ├── IMG_8660.jpeg
│   │   ├── IMG_8661.jpeg
│   │   └── IMG_8662.jpeg
│   │
│   └── SF_Pano/                    # San Francisco panorama image set
│       ├── image2.jpeg
│       ├── image5.jpeg
│       ├── image6.jpeg
│       ├── image8.jpeg
│       └── image11.jpeg
│
├── results/
│   ├── pano_sift.jpg               # Panorama created using SIFT
│   ├── pano_orb.jpg                # Panorama created using ORB
│   ├── pano_sift_pair_matches.jpg  # SIFT feature matches
│   ├── pano_orb_pair_matches.jpg   # ORB feature matches
│   ├── panorama_street.jpg         # Final stitched street panorama
│   └── panorama_bridge.jpg         # Additional Golden Gate panorama
│
└── README.md


## ⚙️ How It Works

The project performs automatic image stitching and panorama generation using OpenCV.

1. **Feature Detection**  
   - Keypoints are detected in overlapping images using SIFT or ORB.
   - SIFT focuses on scale-invariant features, while ORB is faster but less precise.

2. **Feature Matching & Homography Estimation**  
   - Matched keypoints are used to compute a transformation (homography) between images.
   - RANSAC is applied to remove mismatches and improve accuracy.

3. **Image Warping & Blending**  
   - Images are warped using the estimated homography matrix.
   - The final panorama is blended to produce a seamless output.

4. **Comparison of Algorithms**  
   - The project compares SIFT and ORB based on the number of matched keypoints, inliers, and visual stitching quality.


## 🖼️ Results & Visuals

Below are the outputs generated using different feature detection algorithms (SIFT and ORB) for both street and Golden Gate Bridge panoramas.

### 📍 Street Panorama
| Algorithm | Panorama Output | Feature Matches |
|------------|----------------|-----------------|
| **SIFT** | ![SIFT Panorama](results/pano_sift.jpg) | ![SIFT Matches](results/pano_sift_pair1_matches.jpg) |
| **ORB** | ![ORB Panorama](results/pano_orb.jpg) | ![ORB Matches](results/pano_orb_pair1_matches.jpg) |

### 🌉 Golden Gate Bridge Panorama
| Scene | Output |
|--------|---------|
| **Golden Gate Panorama** | ![Golden Gate Panorama](results/panorama_bridge.jpg) |

---

### 🔍 Observations
- **SIFT** produced more accurate alignment and smoother blending, especially in areas with complex textures.  
- **ORB** was faster but resulted in slightly less precise stitching.  
- The difference highlights how feature detection choices directly affect panorama quality.

