# 💻 Device Setup & Deployment Module (device_setup)

## Module Overview
This module contains instructions to set up SmartDormAI on new machines. It includes OS preparation, Python environment setup, model downloads, auto-start configurations, and resource optimization tips. Supports Raspberry Pi, Tiny PCs, NUC, and Mac Mini.

---

## Recommended Platforms
| Device                | Recommended | Notes                          |
|-----------------------|-------------|--------------------------------|
| ThinkCentre Tiny PC   | ✅ Yes      | Excellent performance per $    |
| Dell OptiPlex Micro   | ✅ Yes      | Easy to find used              |
| Raspberry Pi 4B       | ⚠️ Limited | May struggle with TTS / GPT    |
| Mac Mini (Intel/M1)   | ✅ Yes      | Native Python, low noise       |

---

## Setup Steps (Ubuntu 20.04+ suggested)

### 1. Update System
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Python & tools
```bash
sudo apt install python3 python3-pip git ffmpeg portaudio19-dev -y
```

### 3. Clone Repo
```bash
git clone https://github.com/your_username/SmartDormAI.git
cd SmartDormAI
```

### 4. Install Python Dependencies
```bash
pip3 install -r requirements.txt
```

### 5. Download Whisper Model
```bash
wget https://huggingface.co/ggerganov/whisper.cpp/resolve/main/models/ggml-tiny.en.bin -P voice_core/models/
```

### 6. Configure API
Create `.env`:
```
OPENAI_API_KEY=sk-xxxxxx
MODEL=gpt-4o
```

### 7. Run the Assistant
```bash
python3 main_assistant.py
```

---

## Auto-Start (Optional)
```bash
crontab -e
@reboot cd /home/youruser/SmartDormAI && python3 main_assistant.py
```

---

## Tips
- Edge TTS via browser fallback if local TTS fails
- Use USB mic/speakers for modular room setup
- Monitor CPU/memory usage with `psutil`

---

## Development Roadmap
- [x] Ubuntu/macOS setup
- [x] Model auto-download script
- [ ] GUI installer for Windows
- [ ] System resource manager
