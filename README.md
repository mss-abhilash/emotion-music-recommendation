# Emotion-Based Music Recommendation System

### Detect your mood. Play your vibe.

Emotion-Based Music Recommendation System is a Python application that uses real-time computer vision to detect facial emotions from a webcam feed and recommend matching music through Spotify.
It combines an emotion detection model, OpenCV-based video processing, and Spotify playback control to create a seamless, interactive experience.
The system is designed to be fast, practical, and easy to extend for future AI and product features.

## Features

- Real-time emotion detection using webcam
- Music recommendation based on detected emotion
- Integration with Spotify API for playback
- Fast and responsive runtime flow
- Modular and scalable code structure

## Tech Stack

- Python
- OpenCV
- YOLO (emotion detection model)
- Spotify Web API (via Spotipy)
- NumPy
- Ultralytics

## Project Structure

```text
Emotion-based-music-recommendation-system/
|-- main.py
|-- config.py
|-- spotify_config.py
|-- best.pt
|-- requirements.txt
|-- utils/
|   |-- camera.py
|   |-- emotion_to_song.py
|   |-- spotify_client.py
```

- `main.py`: Application entry point. Handles webcam loop, key controls, emotion capture, and playback trigger.
- `config.py`: Core settings such as model path, confidence threshold, and emotion labels.
- `spotify_config.py`: Local Spotify credentials and redirect URI configuration.
- `utils/`: Helper modules for camera/model inference, emotion-to-playlist mapping, and Spotify authentication/playback.
- `best.pt`: Trained YOLO model weights used for emotion detection.

## How It Works

1. Capture webcam input in real time.
2. Detect face and emotion using the trained model.
3. Map the detected emotion to a music category or playlist.
4. Fetch and control playback through Spotify API.
5. Play the recommended music for the detected emotion.

## Installation & Setup

1. Clone the repository:

```bash
git clone https://github.com/your-username/emotion-based-music-recommendation-system.git
cd emotion-based-music-recommendation-system
```

2. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Configure Spotify credentials (recommended: environment variables).

5. Run the project:

```bash
python main.py
```

## Configuration

Set credentials using environment variables (recommended):

```powershell
$env:SPOTIFY_CLIENT_ID = "your_spotify_client_id"
$env:SPOTIFY_CLIENT_SECRET = "your_spotify_client_secret"
$env:SPOTIFY_REDIRECT_URI = "http://127.0.0.1:8080/callback"
```

Or create a local file named `spotify_config.py` in the project root (kept out of Git by `.gitignore`) and add:

```python
CLIENT_ID = "your_spotify_client_id"
CLIENT_SECRET = "your_spotify_client_secret"
REDIRECT_URI = "http://127.0.0.1:8080/callback"
```

Make sure the same redirect URI is configured in your Spotify Developer Dashboard.

## Screenshots

- Add screenshot here: Webcam emotion detection window
- Add screenshot here: Spotify authentication screen
- Add screenshot here: Playback/recommendation result

## Future Improvements

- Improve emotion detection accuracy with a larger and more diverse dataset
- Build a richer user interface for better interaction
- Extend to mobile/web version
- Add advanced playlist personalization based on user behavior

## Disclaimer

- Do not expose API keys or secrets in public repositories.
- This project is intended for educational and learning purposes.

## Author

**Abhilash M**

Building AI-powered experiences that turn real-world signals into meaningful, user-focused products.
