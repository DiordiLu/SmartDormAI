# 🔊 Speaker Module (speaker)

## Module Overview
This module converts text into speech and plays it back using local TTS (Text-to-Speech) engines. It supports bilingual (Chinese & English) output with human-like female voice tones. This is the “mouth” of the SmartDormAI assistant.

## Core Features
- Offline TTS output
- Auto-detects language (Chinese / English)
- Smooth response transitions in dialogue
- Works seamlessly with the speech input module

## Recommended Dependencies
- `edge-tts` (recommended: Microsoft's high-quality TTS)
- `gTTS` (Google's TTS as fallback)
- Audio playback via `playsound`, `pydub`, or system player

## Usage Example
```bash
python tts_player.py "Hello, I am your AI roommate."
```

## Development Progress
- [x] Basic TTS speaking
- [x] Chinese speech synthesis
- [x] English speech synthesis
- [ ] Mixed-language sentence support
- [ ] Voice tone personalization
