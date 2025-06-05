# 🧠 Memory & Logging Module (memory)

## Module Overview
This module records all interactions between the user and the assistant, forming the local "memory core." It enables emotion tracking, long-term preference extraction, and pattern recognition for future personalization or training.

---

## Core Features
- Save all user-assistant dialogues with timestamps
- Annotate conversations with mood, topics, keywords
- Extract long-term preferences and habits
- Sync memory with GPT for personalization

---

## Storage Structure
- Raw logs saved as `.json`
- Each entry structured like this:
```json
{
  "timestamp": "2025-06-05 10:24:31",
  "user": "I'm really tired today",
  "assistant": "Would you like me to help you relax?",
  "mood": "tired",
  "tags": ["emotion", "fatigue"]
}
```

---

## Log Analysis & Update Strategies

### ✅ Local Analysis Mode
- Periodically process logs with Python scripts
- Generate user profile (e.g., mood trends, topics, language usage)

### ✅ GPT-Assisted Summary Mode
- Upload recent logs at night
- GPT returns memory summary, personality tuning suggestions
- Updates written to local config files

---

## Recommended Dependencies
- `datetime`, `json`, `os`
- Optional: `pandas`, `matplotlib` for visualization

---

## Example Usage
```python
from memory_logger import log_conversation
log_conversation("Play something relaxing", "Sure, playing 'Moonlight'.", mood="relaxed")
```

---

## Development Roadmap
- [x] Basic log saving
- [x] Timestamp and mood tags
- [ ] Log visualization and analytics
- [ ] GPT-based memory summarization
- [ ] Local personality file updating
