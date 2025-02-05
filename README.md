# Football Analysis Project

## Introduction
The **Football Analysis Project** aims to detect, track, and analyze football players, referees, and the ball in a video using **YOLO (You Only Look Once)**, a state-of-the-art AI-based object detection model. This project extends beyond basic object detection by introducing additional analytical capabilities, such as team classification based on jersey color, ball possession tracking, speed estimation, and movement analysis. 

### Key Features:
- **Player, Referee, and Ball Detection:** Identifies and tracks all key elements in the match.
- **Team Classification:** Uses **K-means clustering** to segment and classify players into teams based on their jersey colors.
- **Ball Possession Measurement:** Tracks which team controls the ball the most during the game.
- **Camera Movement Compensation:** Uses **Optical Flow** to analyze the motion of the camera across frames, improving tracking accuracy.
- **Perspective Transformation:** Adjusts for depth perception, converting pixel-based measurements into real-world distances.
- **Distance and Speed Calculation:** Estimates the movement of players in meters and calculates their speed.

By implementing these features, this project provides valuable insights into football match dynamics, making it useful for sports analysts, coaches, and machine learning enthusiasts.

## Modules Used
The project utilizes multiple Python libraries and machine learning techniques to achieve accurate tracking and analysis:

### 1. **YOLO (You Only Look Once)**
   - A real-time object detection algorithm that detects and tracks players, referees, and footballs.
   - We have used a **trained YOLO v5 model** to improve detection accuracy.

### 2. **K-means Clustering**
   - A machine learning algorithm used for pixel segmentation and clustering.
   - Helps classify players into teams based on jersey colors.

### 3. **Optical Flow**
   - Measures camera movement between frames, allowing for better tracking of player positions even when the camera is moving.

### 4. **Perspective Transformation**
   - Converts the 2D video feed into a real-world perspective.
   - Helps measure a player's movement in meters instead of pixels.

### 5. **Speed and Distance Calculation**
   - Uses tracking data and transformed coordinates to estimate the speed of players.
   - Measures the total distance covered by each player.

## Trained Models
The project leverages a pre-trained **YOLO v5 model** for object detection. You can download the trained model from the following link:

[Download YOLO v5 Model](https://drive.google.com/file/d/1DC2kCygbBWUKheQ_9cFziCsYVSRw6axK/view?usp=sharing)

## Sample Video
For demonstration purposes, you can download a sample football match video used for testing:

[Download Sample Video](https://drive.google.com/file/d/1t6agoqggZKx6thamUuPAIdN_1zR9v9S_/view?usp=sharing)

## Requirements
To run this project, you need to have the following dependencies installed:

### **Python Version:**
- Python 3.x (Recommended: Python 3.8 or later)

### **Required Python Libraries:**
Install the required libraries using the following command:
```bash
pip install ultralytics supervision opencv-python numpy matplotlib pandas
```

- **Ultralytics:** Required for YOLO object detection.
- **Supervision:** Used for annotation and visualization of detected objects.
- **OpenCV:** Image processing and computer vision tasks.
- **NumPy:** Numerical computations and array operations.
- **Matplotlib:** Visualization of results.
- **Pandas:** Data manipulation and analysis.

## How to Run the Project
Follow these steps to execute the project:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repository-link.git
   cd football-analysis-project
   ```

2. **Download the trained YOLO model** and place it in the appropriate directory.

3. **Run the script** to analyze a football match video:
   ```bash
   python main.py --input video.mp4 --output results.mp4
   ```

   - Replace `video.mp4` with the path to your input video.
   - The output file `results.mp4` will contain the analyzed match with tracking annotations.

## Future Enhancements
- **Real-time analysis:** Extend the project to process live football matches.
- **Advanced AI techniques:** Integrate deep learning models to refine tracking accuracy.
- **Player performance analysis:** Generate detailed statistics on players' movements, passes, and ball possession.

## Conclusion
This project provides an in-depth analysis of football matches using AI and computer vision techniques. By detecting players, referees, and the ball, classifying teams, measuring ball possession, and calculating player movement, this project brings powerful sports analytics capabilities to researchers, analysts, and sports enthusiasts. 

Feel free to contribute to this project by suggesting new features or improvements!

---
**Author:** Muhammad Saadullah
