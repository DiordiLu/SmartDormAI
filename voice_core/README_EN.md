# 🗣️ Voice Recognition & TTS Module (voice_core)

## Module Overview
This module handles voice input and output — turning your spoken language into text and generating voice replies from the assistant. It supports bilingual (Chinese-English) speech and aims to create a natural, personalized interaction experience.

---

## Core Features
- Speech-to-Text (STT)
- Text-to-Speech (TTS)
- Multi-language (auto detect English + Mandarin)
- Wake-word support (e.g., “Xiao Z”)
- Realistic voice synthesis (non-robotic)
- Multi-mic & multi-speaker deployment (multi-room coverage)

---

## Interaction Flow
1. Activated by wake word or passive listening
2. Speech transcribed to text using STT engine
3. Text passed to GPT or local handler
4. GPT reply converted to voice using TTS
5. Audio output through selected speaker(s)

---

## Recommended Dependencies
- `vosk`: lightweight offline STT
- `faster-whisper` or `openai-whisper`: high-accuracy STT
- `pyttsx3`, `gTTS`, `edge-tts`: voice synthesis engines
- `pyaudio`, `sounddevice`: audio I/O backend

---

## Example Usage
```python
from voice_core import listen_and_reply
listen_and_reply()
```

---

## Development Roadmap
- [x] Offline STT via VOSK
- [x] Chinese-English bilingual detection
- [x] Basic TTS support via edge-tts or gTTS
- [ ] Emotion tone detection & tag
- [ ] Multi-room voice I/O
- [ ] Switchable voice styles (e.g., female/natural)
- [ ] Wake-word training and customization
