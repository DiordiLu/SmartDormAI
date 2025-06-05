# 🏠 Multi-Room Audio System Module (multiroom)

## Module Overview
This module enables SmartDormAI to operate across multiple rooms, supporting multiple microphones and speakers for localized voice interaction. It provides spatial awareness and ensures replies are played in the appropriate area.

---

## Core Features
- Listen from multiple microphones simultaneously
- Detect which room is active based on input loudness
- Output voice reply through the corresponding speaker
- Sync voice messages across rooms
- Toggle listening zones (e.g., privacy mode)
- Integrates with `listener` and `speaker` modules

---

## Example Use Cases
- Say “Jarvis” in the bedroom → only bedroom mic triggers
- Say “turn on light” in kitchen → only kitchen responds
- Gaming mode disables PC mic, uses corner mic instead

---

## Recommended Architecture
```python
from multiroom import RoomManager

rm = RoomManager()
rm.start_all()
rm.disable_room("bedroom")
rm.enable_room("living_room")
```

---

## Technical Notes
- Input: Use `sounddevice` or `pyaudio` to separate mics by ID
- Output: Set device ID for each speaker
- Config: Use `multiroom_config.json` to map devices to rooms
- Use threading or multiprocessing for real-time streaming

---

## Suggested Folder Structure
- `rooms/` → each file handles a room’s mic and speaker
- `multiroom_config.json` → maps rooms to devices

---

## Development Roadmap
- [x] Multi-input listening support
- [x] Per-room speaker routing
- [ ] Dynamic room-device config
- [ ] Voice sync across rooms
- [ ] Privacy toggles per zone
