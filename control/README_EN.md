# 💡 Peripheral Control Module (control)

## Module Overview
This module controls external dorm devices like lights, AC, fans, and door accessories. The goal is to provide smart control via voice or events, without modifying the original wiring of the devices.

---

## Control Methods
- ✅ Relay (e.g., smart plugs)
- ✅ Physical actuator (button pusher / servo press)
- ✅ Infrared transmitter (simulate remotes)
- ✅ Serial/Bluetooth (for smart devices)

---

## Devices (Based on Your Plan)
| Device     | Control Method    | Status     |
|------------|-------------------|------------|
| Light      | Physical button pusher | ✅ Planned |
| AC         | IR emitter         | ✅ Designed |
| Fan        | Relay/plug         | ✅ Expandable |
| Door-light | Trigger by camera  | ✅ Planned |
| Sleep Mode | One-command scene  | ✅ Supported |

---

## Interface Sample
```python
control_lamp("on")
control_ac("off")
control_scene("sleep_mode")
```

---

## Recommended Dependencies
- `serial` for serial comms
- `RPi.GPIO` or `gpiozero` for Pi-based boards
- `infrared` / IR libraries
- `time`, `json`, `os`

---

## Example Usage
```python
from control import control_lamp, control_ac

control_lamp("on")
control_ac("cooling", temperature=23)
```

---

## Extensions
- 🔌 Power state monitoring
- 🧠 Trigger control from GPT-generated intent
- 📶 Connect to ESP32 / Arduino ecosystem

---

## Development Roadmap
- [x] Abstracted device control APIs
- [x] Physical button pushing (servo/motor)
- [ ] IR-based AC control
- [ ] Scene-based batch control
- [ ] Device status memory/cache
