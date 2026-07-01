cat > README.md << 'EOF'
# Player Tracking & Re-Identification Pipeline

An end-to-end computer vision pipeline for tracking and re-identifying players throughout a football match video.

## What it does
- Detects every player per frame using **YOLOv8**
- Tracks players across frames using **BoT-SORT** with Kalman filtering
- Automatically classifies players into two teams using **KMeans clustering**
- Recovers lost player identities after occlusions using **appearance-based Re-ID**
- Isolates and follows a single targeted player throughout the match

## Results
- Raw tracking: 169 fragmented IDs
- After Re-ID: 87 stable IDs (49% reduction in ID switches)

## Tech Stack
- YOLOv8 (Ultralytics)
- BoT-SORT
- OpenCV
- KMeans (scikit-learn)
- Cosine similarity Re-ID

## How to run
1. Install dependencies: `pip install ultralytics supervision transformers scikit-learn opencv-python-headless`
2. Open `player_tracking_pipeline.ipynb`
3. Set your video path and run cells top to bottom
EOF
git add README.md
git commit -m "Add README"
git push
