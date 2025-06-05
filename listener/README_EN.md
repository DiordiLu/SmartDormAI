# 🎙️ Listener Module (listener)

## Module Overview
This module listens to user voice input and performs local speech recognition. It supports mixed Chinese and English and uses models like `whisper` or `faster-whisper`, optimized for offline usage on low-end machines. It serves as the input gateway for the entire SmartDormAI system.

## Core Features
- Real-time microphone input monitoring
- Offline speech-to-text conversion (no internet required)
- Optional wake-word trigger
- Optional language auto-detection

## Recommended Dependencies
- `faster-whisper` (preferred)
- `pyaudio` or `sounddevice` (for capturing input)
- `langdetect` (optional)

## Usage
You can either import this module in the main program or run it independently:
```bash
python listener.py
```

## Development Progress
- [x] Basic speech listener
- [ ] Add wake-word detection
- [ ] Add multilingual input support
- [ ] Decouple from the main assistant logic
