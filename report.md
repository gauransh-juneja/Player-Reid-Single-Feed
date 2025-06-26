# Report: Player Re-Identification in a Single Camera Feed

## 🎯 Objective
The goal of this project was to detect and track soccer players from a single 15-second video. The challenge was to assign each player a unique ID and maintain that identity even if the player temporarily leaves and re-enters the frame.

---

## 🧠 Approach

### Detection
- Used a fine-tuned version of Ultralytics YOLOv11 (`yolo_reid.pt`) to detect players in each frame.
- Filtered detections to exclude the ball and referees.

### Re-Identification (Tracking)
- For each detection, calculated the centroid of the bounding box.
- Matched detections to previously seen players using Euclidean distance between centroids.
- Assigned the same ID if the centroid was close to a previously tracked one.
- Assigned a new ID if no match was found.

---

## ✅ Outcome
- Successfully tracked players in real-time across the video.
- IDs remained consistent for players who remained in-frame or briefly disappeared.
- Basic but effective re-identification achieved using only spatial proximity.

---

## ⚠️ Challenges
- If players disappeared for too long or reappeared in a new position, IDs could get reassigned.
- No use of deep features (e.g., jersey color or embeddings), which would improve accuracy.

---

## 🔮 Future Work
- Add appearance-based tracking (e.g., DeepSORT or custom Re-ID model).
- Handle longer occlusions using player history or jersey number recognition.
- Evaluate tracking accuracy using ground truth (if available).

---

## 👤 Author
**Gauransh Juneja**
