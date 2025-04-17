# Test Plan for STM32F4xx grblHAL Enhancements

## Hardware Required

- STM32F4 (Blackpill or Nucleo)
- STLink or debugger
- Stepper driver (e.g., A4988, TMC2209)
- Limit switches (optional)
- USB-to-serial adapter for PC interface

## Tests by Feature

### ✅ Basic Boot Tests

| Test | Pass/Fail | Notes |
|------|-----------|-------|
| MCU boots | ☐ | LED blinks or serial responds |
| Clock configured correctly | ☐ | Expected timer freq |

### 🧠 AI Interface

| Test | Result | Example |
|------|--------|---------|
| Serial command "status" | ☐ | AI replies with XYZ |
| Translate "Move 10mm right" | ☐ | Sends `G1 X10 F500` |

### 🛠 Motion + GPIO

| Test | Result |
|------|--------|
| Axis moves 10mm | ☐ |
| Limit switch triggers | ☐ |
| Spindle PWM | ☐ |

### 🧪 Stress

- [ ] 100 G-code lines in 5s
- [ ] Manual override mid-job
- [ ] AI interface stays responsive during cut

