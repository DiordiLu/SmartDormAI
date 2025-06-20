# 💡 外设控制模块（control）

## 模块简介
本模块用于控制宿舍中的外部设备，包括灯光、空调、风扇、门锁等。目标是在不改动原有电路结构的前提下，实现语音智能控制与自动化响应。

---

## 控制方式
- ✅ 继电器控制（智能插座等）
- ✅ 板机控制（用于机械式开关）
- ✅ 红外遥控（模拟遥控器信号）
- ✅ 串口/蓝牙控制（部分智能家电）

---

## 已支持设备（根据你设想）
| 设备     | 控制方式     | 实现状态 |
|----------|--------------|----------|
| 灯       | 板机物理按压 | ✅ 已规划 |
| 空调     | 红外模块     | ✅ 已设想 |
| 风扇     | 继电器/插座  | ✅ 可拓展 |
| 门灯联动 | 门磁/摄像头  | ✅ 摄像头触发时自动开灯 |
| 全局关闭 | 场景语音指令 | ✅ 支持睡前/外出模式 |

---

## 控制接口结构建议
```python
control_lamp("on")
control_ac("off")
control_scene("sleep_mode")
```

---

## 推荐依赖
- `serial`：串口通信
- `gpiozero` / `RPi.GPIO`：树莓派用
- `infrared`（红外控制包）
- `time`, `json`, `os`

---

## 使用示例
```python
from control import control_lamp, control_ac

control_lamp("on")
control_ac("cooling", temperature=23)
```

---

## 拓展建议
- 🔌 电源状态监控
- 🧠 根据 GPT 生成意图自动触发控制命令
- 📶 接入 ESP32/Arduino 等设备

---

## 开发计划
- [x] 控制接口结构化封装
- [x] 板机驱动原始灯控
- [ ] 红外空调控制
- [ ] 全局语音场景
- [ ] 设备状态记忆缓存
