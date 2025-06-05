# ☁️ Cloud Sync Module (cloud_sync)

## Module Overview
This module handles data transfer between the local SmartDormAI system and the cloud (e.g., GPT servers). Its purpose is to upload logs, receive GPT-generated summaries, and update memory/personality configurations. Ideal for low-frequency syncs (e.g., nightly).

---

## Core Features
- Upload daily logs and emotion tracking
- Receive GPT-generated summaries and keyword extractions
- Sync memory/personality configuration files
- Encrypted transmission & local archive management

---

## Usage Strategies

### ✅ Nightly Auto Sync (Recommended)
- Scheduled sync when network is available
- Batch upload logs from local `logs/` folder
- Download updates and apply to memory

### ✅ Manual Trigger
- Useful for testing or on-demand syncing

---

## Recommended File Layout
- `logs/` → where daily `.json` logs are stored
- `summaries/` → downloaded GPT summaries
- `sync_config.json` → contains sync frequency and endpoint settings

---

## Suggested Dependencies
- `requests`, `os`, `json`
- Can connect to OpenAI API, AWS S3, Cloudflare, GitHub, etc.

---

## Example Usage
```python
from cloud_sync import nightly_sync
nightly_sync("logs/2025-06-05.json")
```

---

## Development Roadmap
- [x] Manual upload/download
- [x] Summary applied to memory
- [ ] Scheduled nightly sync
- [ ] Configurable summarization logic
- [ ] Secure cloud identity/authentication
