# 🧠 情绪识别模块（emotion）

## 模块简介
本模块用于识别用户在对话中的情绪状态，结合语音语调、用词习惯与上下文信息，输出当前情绪类别、强度与建议回应策略。识别结果将影响语音播报风格、GPT 回复提示，以及长期记忆生成。

---

## 核心功能
- 提取语音中的情绪信号（如音调、节奏、停顿）
- 提取文字内容中的情绪关键词（如“烦”、“太难了”、“我崩溃了”）
- 结合历史对话与行为生成情绪趋势
- 与 memory 模块联动，记录每次情绪波动
- 与 voice_core 模块联动，调整语音语调（如更温柔/更积极）
- 与 GPT 通信模块联动，动态生成个性化 system prompt

---

## 示例输出格式
```json
{
  "mood": "tired",
  "score": 0.75,
  "tone": "soft",
  "suggestion": "use short comforting sentences"
}
```

---

## 使用方式
```python
from emotion import analyze_emotion

result = analyze_emotion(text="我真的太累了，啥也不想干")
print(result['mood'])  # 输出：tired
```

---

## 推荐方法与模型
- `textblob` / `VADER`：文本情感分析（英文友好）
- `SnowNLP` / 自定义关键词：中文情绪识别
- `pyAudioAnalysis`：语音特征提取
- `scikit-learn`：训练情绪分类模型（可选）

---

## 目标情绪类别（可扩展）
- 正面：happy, excited, relaxed
- 中性：neutral, focused
- 负面：tired, frustrated, anxious, sad

---

## 开发计划
- [x] 文本关键词识别
- [x] 输出情绪标签 + 强度
- [ ] 情绪趋势追踪（存入 memory）
- [ ] 声音特征提取（语调/能量）
- [ ] GPT 回答风格调整接口
- [ ] 与 TTS 播报风格联动
