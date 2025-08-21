## Pose Estimation (MediaPipe, Python)

This repository demonstrates a minimal, real‑time human pose estimation app using MediaPipe and OpenCV. It can run with a webcam or a local video file and overlays detected pose landmarks on each frame with an FPS counter.

### Features
- Real‑time inference via webcam
- Video file input for offline testing
- Pose landmarks drawing with MediaPipe connections
- FPS overlay for quick performance feedback

### Repository structure
- `Poz_kestirimi(Pose Estimation).py` — main script
- `Screenshots/` — sample outputs
- `video*.mp4` — example videos for testing
- `requirements.txt` — Python dependencies
- `.gitignore` — basic Python/IDE ignores

### Requirements
- Python 3.9+
- Windows/macOS/Linux
- Packages: OpenCV, MediaPipe, NumPy

Install dependencies:
```bash
pip install -r requirements.txt
```

### Quick start
Run with the default webcam:
```bash
python "Poz_kestirimi(Pose Estimation).py"
```

Run with a video file:
1) Open the script and switch the capture source, for example:
```python
#cap = cv2.VideoCapture("video5.mp4")
cap = cv2.VideoCapture(0)
```
Change it to:
```python
cap = cv2.VideoCapture("video5.mp4")
#cap = cv2.VideoCapture(0)
```
2) Save and run the script again.

### Tips
- If frames do not show, verify that the webcam index `0` exists or try `1`.
- If the video path is not found, place the file next to the script or use an absolute path.
- Close the output window to stop the program.

### Screenshots
See the `Screenshots/` folder for example results.

### Troubleshooting
- MediaPipe build errors: upgrade `pip` and `setuptools`, then reinstall.
  ```bash
  python -m pip install --upgrade pip setuptools
  pip install -r requirements.txt --upgrade --force-reinstall
  ```
- Webcam returns empty frames: another app may be using the camera; close it and retry.
- Performance: reduce input resolution or increase `waitKey` delay.

### Roadmap
- Optional keypoint export to CSV/JSON
- Simple activity/angle calculations

---
For the Turkish documentation, see `README_TR.md`.


