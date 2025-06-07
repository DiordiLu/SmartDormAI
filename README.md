# 🧠 SmartDormAI — 原创设计声明 / Original Design Statement

SmartDormAI 是由 **Diordi Lu** 于 2025 年 6 月首次提出并设计的宿舍智能语音助手系统。  
本项目构想、模块架构、语音逻辑、情绪机制及 GPT 集成策略均为原创设计。

本项目面向学习/展示用途，支持研究性毕业设计、私有部署、非商业化拓展。  
任何形式的再发布、修改或改编请注明原始作者与项目链接。

---

SmartDormAI was originally conceptualized and designed by **Diordi Lu** in June 2025.  
Its modular system, voice interaction framework, memory logic, and GPT integration are original and structured for educational use.

This project is intended for academic research, private deployment, and non-commercial showcase.  
Please attribute the original author and link if reused or modified.

# 🧠 SmartDormAI：宿舍智能语音助手系统

SmartDormAI 是一个本地运行的宿舍语音助手系统，目标是打造一个拥有语音理解、情绪感知、设备控制、身份识别和记忆功能的 AI 助理，运行在低功耗小主机上，支持中英文混合语音交互，最大限度保护隐私并提升生活便利。

---

## 📦 模块结构

| 模块目录             | 功能说明                                     | 当前状态             |
|----------------------|----------------------------------------------|----------------------|
| `listener/`           | 麦克风监听与唤醒检测                         | 📄 文档完成 / 待开发 |
| `voice_core/`         | 语音识别（STT）与语音合成（TTS）             | 📄 文档完成 / 待开发 |
| `speaker/`            | 播报模块，负责播放助手的语音回复             | 📄 文档完成 / 待开发 |
| `chatgpt_interface/`  | GPT 接口通信，生成文本回复                   | 📄 文档完成 / 待开发 |
| `memory/`             | 本地记忆与历史管理                           | 📄 文档完成 / 待开发 |
| `cloud_sync/`         | 云端同步与夜间记忆优化                       | 📄 文档完成 / 待开发 |
| `vision/`             | 摄像头拍照与人脸识别                         | 📄 文档完成 / 待开发 |
| `control/`            | 控制灯光、空调、门禁等外设                   | 📄 文档完成 / 待开发 |
| `emotion/`            | 识别情绪状态，调节语气与行为                 | 📄 文档完成 / 待开发 |
| `multiroom/`          | 多房间麦克风/扬声器支持                      | 📄 文档完成 / 待开发 |
| `device_setup/`       | 项目部署与初始化指南                         | 📄 文档完成 / 可使用 |
| `scheduler/`          | 定时任务执行（如夜间上传、定时提醒）         | 📝 规划中             |
| `main_assistant.py`   | 主入口脚本，集成所有模块                     | ⏳ 草图设计中         |

---

## 🧠 核心功能

- 🗣️ 支持中英文混合语音交互
- 😌 自动识别用户情绪并调节语气
- 👤 人脸/声纹识别与权限判断
- 💾 本地记忆 + 云端周期性更新
- 🔊 多房间麦克风与扬声器协同
- 🤖 GPT-4o 接入，支持持续成长

---

## 💻 推荐硬件平台

| 组件类型     | 推荐设备                        | 说明                        |
|--------------|----------------------------------|-----------------------------|
| 主机         | ThinkCentre Tiny / Dell Micro   | 二手高性价比，支持长时运行 |
| 麦克风       | USB 麦克风 / 阵列麦克风          | 精准拾音                    |
| 扬声器       | 蓝牙或 USB 音响                  | 多房间语音播放              |
| 摄像头       | 普通 USB 摄像头                  | 用于门控、记录或识别        |

---

## 🚀 快速部署步骤（Ubuntu）

```bash
sudo apt update && sudo apt install python3-pip git ffmpeg portaudio19-dev -y
git clone https://github.com/your_username/SmartDormAI.git
cd SmartDormAI
pip3 install -r requirements.txt
python3 main_assistant.py
```

---

## 📍 项目开发进度追踪

| 项目项                        | 当前状态         |
|-------------------------------|------------------|
| 功能模块设计与文档            | ✅ 已完成         |
| 语音识别/播报系统接入         | ⏳ 未开始         |
| 摄像头模块与视觉处理          | ⏳ 未开始         |
| 多设备控制通信接口            | ⏳ 未开始         |
| GPT 调用与缓存策略            | 📝 设计中         |
| UI 提示与警报窗口机制         | 📝 设计中         |
| 总控制程序架构                | ⏳ 草图设计中     |

---

## 💰 成本估算

| 项目                | 说明                                | 预计月费用         |
|---------------------|-------------------------------------|--------------------|
| 本地语音/硬件控制   | 全本地，免费                         | ✅ 免费             |
| GPT-4o API 使用费    | 每日交互 20–30 次，按 token 计费     | $30 – $50 USD      |
| 云同步存储          | GitHub / 自建 NAS / Server 均可使用 | 通常免费或极低成本 |

---

## 📄 使用许可

本项目面向学习/展示用途，支持研究性毕业设计、私有部署、非商业化拓展。
