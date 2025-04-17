# 🧰 Development Environment Setup: STM32F4xx grblHAL

This guide walks you through setting up a development environment for working with this grblHAL fork on STM32F4xx boards (e.g., Blackpill, Nucleo-64). It covers firmware building, flashing, and optional AI CLI integration.

---

## 🖥️ Host Machine Setup (PC / Linux / Mac)

### ✅ Required Tools

- [ ] **VS Code**, **STM32CubeIDE**, or your preferred C IDE
- [ ] **ARM toolchain**
  - Install via package manager or from [ARM Developer](https://developer.arm.com/downloads/-/gnu-rm)
  - Command-line compiler: `arm-none-eabi-gcc`
- [ ] **Flashing tools**:
  - [ ] OpenOCD
  - [ ] STLink utility or STM32CubeProgrammer
  - [ ] BlackMagic Probe (optional)

### ✅ Optional Tools

- Python 3.x with:
  - `pyserial` for AI interaction testing: `pip install pyserial`
  - CLI tool like `minicom` or `screen` for serial debugging
- Git installed and configured

---

## 🧱 STM32 Hardware Setup

### Required

- STM32F4-based board (Blackpill, Nucleo-64)
- USB cable (data capable)
- Flashing/debugging tool (e.g., ST-Link V2, J-Link, BMP)
- Stepper driver (e.g., A4988, TMC2209) and test motor (optional)

### Recommended

- Logic analyzer or oscilloscope for pulse validation
- Limit switches (for homing tests)
- Power supply (5V or 12V) if driving motors

---

## 🧪 Build + Flash Steps (Generic Flow)

```bash
# Example using Makefile + GCC toolchain
make BOARD=STM32F411

# Flash with OpenOCD
openocd -f interface/stlink.cfg -f target/stm32f4x.cfg \
        -c "program build/firmware.elf verify reset exit"
