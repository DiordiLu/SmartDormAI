# 🎥 Camera & Door Recognition Module (vision)

## Module Overview
This module manages visual surveillance for the dorm door. It leverages real-time camera input, facial recognition, and intelligent control of lighting and recording to detect and respond to entry events.

---

## Core Features
- Starts recording immediately when the door opens
- Simultaneously triggers physical mechanism to turn on lights
- Continues recording for 30 seconds after door closes
- Performs facial recognition on captured video or photos
- Automatically deletes footage if it’s you; retains unknown faces
- Only runs recognition when the PC is powered on (to save resources)

---

## Workflow
1. Door is detected open via sensor or signal
2. Triggers:
   - Starts camera recording
   - Activates lighting actuator
3. If PC is on:
   - Perform facial recognition
   - Delete footage if it's you
   - Save unknowns, log timestamp
4. After door closes, continue recording for 30 seconds

---

## Suggested Dependencies
- `opencv-python` for video
- `face_recognition` for face ID
- `datetime`, `os`, `shutil` for file operations

---

## Example Usage
```python
from vision import handle_door_event
handle_door_event("door_open")
```

---

## Recommended Structure
- `photos/`: snapshots
- `videos/`: recorded clips
- `faces/`: reference photos of you
- `logs/`: logs of unknown entries

---

## Development Roadmap
- [x] Camera capture and video
- [x] Facial recognition and deletion
- [x] Delay stop logic
- [ ] Directional motion analysis
- [ ] Real-time alert system
- [ ] Privacy-aware encryption support
