
# 🧠 SmartDormAI: Dormitory Smart Voice Assistant System

SmartDormAI is a locally-run assistant system designed for dormitory scenarios. It integrates voice understanding, emotion recognition, device control, identity authentication, and memory features. It runs on affordable second-hand mini PCs and supports bilingual speech interaction (Chinese + English) to ensure privacy and improve everyday convenience.

---

## 📦 Module Structure

| Module Directory        | Description                                      | Status                  |
|-------------------------|--------------------------------------------------|--------------------------|
| `listener/`             | Microphone listening and wake-word detection     | 📄 Docs ready / Pending  |
| `voice_core/`           | Speech-to-text (STT) and text-to-speech (TTS)    | 📄 Docs ready / Pending  |
| `speaker/`              | Playback module for assistant speech             | 📄 Docs ready / Pending  |
| `chatgpt_interface/`    | GPT communication interface                      | 📄 Docs ready / Pending  |
| `memory/`               | Local memory and history management              | 📄 Docs ready / Pending  |
| `cloud_sync/`           | Cloud syncing and nighttime memory optimization  | 📄 Docs ready / Pending  |
| `vision/`               | Camera-based capture and face recognition        | 📄 Docs ready / Pending  |
| `control/`              | Device control: lights, AC, door, etc.           | 📄 Docs ready / Pending  |
| `emotion/`              | Emotion detection and behavioral adaptation      | 📄 Docs ready / Pending  |
| `multiroom/`            | Multi-room mic/speaker coordination              | 📄 Docs ready / Pending  |
| `device_setup/`         | Setup and installation instructions              | 📄 Docs ready / Usable   |
| `scheduler/`            | Task scheduling (e.g., night sync, reminders)    | 📝 In planning           |
| `main_assistant.py`     | Main script integrating all modules              | ⏳ In sketching phase     |

---

## 🧠 Key Features

- 🗣️ Bilingual (Chinese + English) voice interaction
- 😌 Emotion-aware tone and response
- 👤 Identity & permission recognition (face/voice)
- 💾 Local-first memory with optional cloud sync
- 🔊 Multi-room input/output voice architecture
- 🤖 GPT-4o powered interaction and learning

---

## 💻 Recommended Hardware Platform

| Component     | Recommended Device                  | Description                  |
|---------------|--------------------------------------|------------------------------|
| Main PC       | ThinkCentre Tiny / Dell Micro        | Affordable & efficient       |
| Microphone    | USB or microphone array              | Accurate voice capture       |
| Speaker       | USB/Bluetooth speaker                | For voice feedback per room  |
| Camera        | Standard USB webcam                  | Door monitoring & recognition|

---

## 🚀 Quick Start (Ubuntu Example)

```bash
sudo apt update && sudo apt install python3-pip git ffmpeg portaudio19-dev -y
git clone https://github.com/your_username/SmartDormAI.git
cd SmartDormAI
pip3 install -r requirements.txt
python3 main_assistant.py
```

---

## 📍 Development Progress

| Feature Area                  | Status               |
|-------------------------------|----------------------|
| Module Documentation          | ✅ Completed          |
| Voice Recognition / Playback  | ⏳ Not started        |
| Vision & Camera Processing    | ⏳ Not started        |
| Device Control Interface      | ⏳ Not started        |
| GPT Integration & Caching     | 📝 In design          |
| UI Window & Notification      | 📝 In design          |
| Main Integration Architecture | ⏳ Early sketching    |

---

## 💰 Cost Estimation

| Item                    | Description                                 | Monthly Estimate     |
|-------------------------|---------------------------------------------|----------------------|
| Local Voice + Hardware  | All modules run offline, no fees            | ✅ Free               |
| GPT-4o API Usage        | 20–30 interactions/day via token pricing    | $30 – $50 USD        |
| Cloud Sync              | GitHub / Self-hosted storage available      | Free or very low     |

---

## 📄 License

This project is for educational and prototyping purposes only. Feel free to adapt it for academic or private use.
