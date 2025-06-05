# 🧠 GPT Communication Module (chatgpt_interface)

## Module Overview
This module handles communication with GPT models (e.g., OpenAI’s ChatGPT) and acts as the brain of SmartDormAI. It supports real-time online use as well as offline queuing and deferred processing.

---

## Core Features
- Sends user input to GPT and receives natural replies
- Supports emotion-aware and contextual memory
- Allows nightly updates for memory/personality sync
- Stores and batches requests for efficient processing

---

## Communication Strategies

### ✅ Mode 1: Real-Time Chat (Online)
> Standard ChatGPT-like behavior

- User input → sent to GPT → response → played by TTS
- Local logs are recorded for all conversations

### ✅ Mode 2: Local Proxy Forwarding
> The assistant sends messages to GPT on your behalf

- Assistant listens → formats prompt → sends to GPT
- Replies are spoken aloud and logged
- Allows future training or fine-tuning

### ✅ Mode 3: Nighttime Sync & Memory Training
> For privacy, cost control, and low-resource systems

- Logs stored locally during the day
- At night, logs are uploaded and summarized
- Summaries are used to update local personality/memory

---

## Suggested Dependencies
- `openai`: official API client
- `requests`: fallback HTTP client
- `dotenv`: load secrets safely
- `json`: for log and cache management

---

## Example Usage
```python
from send_to_gpt import ask_gpt
reply = ask_gpt("I'm feeling overwhelmed today.")
print(reply)
```

---

## Development Roadmap
- [x] Real-time GPT connection
- [x] Error handling
- [x] Local Q&A cache
- [ ] Nighttime summary upload
- [ ] Emotion-aware integration
- [ ] Memory system interface

---

## Estimated Cost 💰

| Mode               | Usage Pattern       | Daily Tokens  | Cost Estimate (at $10 per million tokens) |
|--------------------|---------------------|---------------|--------------------------------------------|
| Real-Time Dialogue | 10–30 messages/day  | 5,000–15,000  | $0.05 – $0.15 / day                        |
| Night Sync         | 1 upload per night  | 4,000–8,000   | $0.04 – $0.08 / day                        |
| Cached Requests    | Batch-uploaded logs | Variable      | Lower, depends on compression strategy     |

> Rough monthly cost: **$5 – $10 USD**  
> Heavy users (100+ msgs/day): may cost **$20+**, caching recommended
