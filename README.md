# MP Doom — Doom (1993) with MediaPipe for immersive controls

MP Doom maps hand and body gestures (via MediaPipe) to controls for the classic Doom engine using ViZDoom and the Fredoom WAD. You can move, aim, and shoot using gestures captured from a webcam.

### [Project video](https://youtu.be/Pw6oNyOBjBM)

![Screenshot](assets/screenshot.png)

## Overview

This project demonstrates gesture-based control for Doom using MediaPipe models and ViZDoom. It is intended as a research/learning prototype and it's still in development.

## Requirements

- Windows
- Python 3.11+
- pip

## Installation

1. Clone the repository:

```bash
git clone https://github.com/lucaslimb/mpdoom.git
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
# Windows PowerShell
.\venv\Scripts\Activate.ps1
# Windows cmd
.\venv\Scripts\Activate.bat
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## How to run

Start the project:

```bash
python mpdoom.py
```

- Press `SPACE` to show/hide tracking overlays
- Press `ESC` to exit

## Gesture controls

The system maps simple hand and pose gestures to in-game actions. Below is a quick reference based on the implementation:

| Gesture | In-game action | Notes |
|---|---:|---|
| Right forearm extended | Move forward | Index fingertip vertically distant from the shoulder |
| Right arm retracted | Stop | Index fingertip near the shoulder vertically |
| Right forearm lateral movement | Aim / move camera | Wrist horizontal movement controls camera yaw |
| Index finger extend → retract | Shoot | Relative positions of Index TIP/DIP/PIP/MCP used to detect trigger |

## Stack
- Python 3.11
- MediaPipe + OpenCV
- VizDoom 1.3.0