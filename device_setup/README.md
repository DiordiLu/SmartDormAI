# 💻 设备初始化与部署模块（device_setup）

## 模块简介
本模块用于指导如何在新设备上部署 SmartDormAI 系统，包含操作系统准备、依赖安装、语音模型下载、后台启动配置等内容。支持在树莓派、小主机（如 ThinkCentre Tiny）、NUC 等硬件上运行。

---

## 适配平台建议
| 平台               | 推荐 | 说明                          |
|--------------------|------|-------------------------------|
| ThinkCentre Tiny    | ✅   | 高性价比，性能远超树莓派       |
| Dell Micro Optiplex | ✅   | 二手主机兼容性好               |
| 树莓派 4B           | ⚠️   | 可用但 TTS/GPT 接口速度受限    |
| Mac Mini (Intel/M1) | ✅   | macOS用户原生运行              |

---

## 部署流程（建议标准 Ubuntu 20.04+）

### 第一步：系统更新
```bash
sudo apt update && sudo apt upgrade -y
```

### 第二步：安装 Python 和必要工具
```bash
sudo apt install python3 python3-pip git ffmpeg portaudio19-dev -y
```

### 第三步：克隆项目
```bash
git clone https://github.com/你的用户名/SmartDormAI.git
cd SmartDormAI
```

### 第四步：安装依赖
```bash
pip3 install -r requirements.txt
```

### 第五步：下载语音模型（如 faster-whisper）
```bash
# 示例：下载 tiny 模型
wget https://huggingface.co/ggerganov/whisper.cpp/resolve/main/models/ggml-tiny.en.bin -P voice_core/models/
```

### 第六步：设置 API 密钥
创建 `.env` 文件：
```
OPENAI_API_KEY=sk-xxxxxx
MODEL=gpt-4o
```

### 第七步：测试启动
```bash
python3 main_assistant.py
```

---

## 自动开机启动（可选）
使用 systemd 或 crontab 将助手开机启动：
```bash
crontab -e
@reboot cd /home/youruser/SmartDormAI && python3 main_assistant.py
```

---

## 其他建议
- 建议使用 Chrome + Edge TTS 浏览器作为备用输出方式
- 使用独立蓝牙音箱/USB声卡作为多房语音设备
- 用 `psutil` 检测系统负载，动态调节模块调用频率

---

## 开发计划
- [x] Ubuntu & macOS 部署文档
- [x] 模型一键下载脚本
- [ ] GUI 安装器 for Windows 用户
- [ ] 硬件资源占用监控脚本
