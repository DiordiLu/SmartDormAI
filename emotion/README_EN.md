# 🧠 Emotion Detection Module (emotion)

## Module Overview
This module detects the user's emotional state based on their speech tone, wording, and context. It influences voice response style, GPT prompt guidance, and long-term emotional profiling via the memory module.

---

## Core Features
- Extract emotion cues from audio (e.g., tone, pace, pauses)
- Detect keywords from text content
- Track emotional trends over time
- Save each interaction's emotional tag into memory
- Adapt voice output tone (e.g., softer, calmer)
- Modify GPT prompt based on mood

---

## Example Output
```json
{
  "mood": "frustrated",
  "score": 0.88,
  "tone": "gentle",
  "suggestion": "respond with empathy and clarity"
}
```

---

## Usage Example
```python
from emotion import analyze_emotion

result = analyze_emotion("I’m so tired and overwhelmed")
print(result['mood'])  # Output: tired
```

---

## Recommended Tools / Models
- `textblob`, `VADER`: sentiment analysis for English
- `SnowNLP` or keyword dictionaries: for Mandarin
- `pyAudioAnalysis`: for vocal tone extraction
- `scikit-learn`: optional classifier for fine-tuning

---

## Target Emotion Labels (extendable)
- Positive: happy, excited, calm
- Neutral: focused, neutral
- Negative: tired, sad, angry, stressed

---

## Development Roadmap
- [x] Keyword-based emotion detection
- [x] Mood + intensity output
- [ ] Trend tracking and memory integration
- [ ] Speech-based tone analysis
- [ ] GPT style modulation interface
- [ ] TTS voice adaptation
