# Smart Dorm AI Assistant (Campus JARVIS)

This project aims to build an intelligent voice assistant tailored for dormitory life. It combines local speech recognition, speech synthesis, device control, GPT dialogue integration, memory logging, and emotion-aware interaction—all running **without relying on the cloud**.

---

## 🌟 Core Features

- ✅ Local speech recognition (supports mixed English + Chinese)
- ✅ Human-like voice responses (female voice style)
- ✅ GPT-based smart conversation (cloud-assisted if enabled)
- ✅ Control devices via voice: lights, AC, door
- ✅ Face recognition at the door for identity filtering
- ✅ Memory logging and daily upgrade via GPT summarization
- ✅ Private data remains local by default
- ✅ Modular design for future smart room expansion

---

## 📁 Project Structure

```bash
SmartDormAI/
├── main_assistant.py           # Main script
├── listener/                   # Speech recognition module
├── speaker/                    # Speech synthesis (TTS)
├── chatgpt_interface/          # GPT communication module
├── memory/                     # Logging and memory management
├── cloud_sync/                 # Optional cloud sync and upgrades
├── control_modules/            # Physical device control logic
├── ui_monitor/                 # Optional UI status panel
└── README.md                   # This documentation
```

---

## 💻 Recommended Environment

- Hardware: Second-hand desktop (preferred over Raspberry Pi)
- OS: Windows / Linux / macOS
- Language: Python 3.10+
- Key Tools:
  - Speech-to-text: `faster-whisper` (local)
  - TTS: `Edge-TTS`
  - Face recognition: `face_recognition` or OpenCV + YOLO

---

## 🧠 Development Roadmap (by Priority)

| Priority | Feature Module             | Description                                         |
|----------|----------------------------|-----------------------------------------------------|
| ①        | Local speech input/output  | Listen and respond naturally via voice              |
| ②        | GPT interface              | Enable “soulful” conversation                       |
| ③        | Conversation logging       | Store all interactions locally                      |
| ④        | Physical control modules   | Control lights, AC, etc. via voice                  |
| ⑤        | Door control + monitoring  | Face ID filter, log entries, auto-light on entry    |
| ⑥        | Cloud sync + daily upgrade | Summarize daily logs to update memory/personality   |
| ⑦        | Emotion/personality engine | Adjust assistant tone based on emotional feedback   |
| ⑧        | UI & desktop notifier      | Optional: GUI to notify alerts                      |

---

## 🔐 Privacy and Licensing

- All data is stored locally by default
- GPT summaries (optional) upload logs only at night
- Planned license: MIT

---

## ✨ Vision

> “I want an AI that doesn’t interrupt, but is always there.  
She listens, helps, remembers, and evolves to understand me.”

---

📌 Project Status: Early Development (June 2025)  
🧠 Author: Diordi Lu + ChatGPT collaborative design  
🛠️ Contributions & suggestions welcome!
