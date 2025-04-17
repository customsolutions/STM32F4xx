# grblHAL STM32F4xx AI-Enhanced Development Roadmap

## 🛠️ Phase 1: Foundation & Safety

- [ ] Forked experimental branch created
- [ ] Local dev environment (IDE + toolchain) functional
- [ ] Flash/debug tool verified (e.g., STLink or Blackmagic)
- [ ] Test harness and basic motion tests defined

## 🚀 Phase 2: Code Optimization

- [ ] Profile ISR timing and planner jitter
- [ ] Review interrupt and HAL routines for bottlenecks
- [ ] Refactor low-level drivers for modularity and clarity
- [ ] Document timing-critical paths

## 🧠 Phase 3: AI Integration

- [ ] Add serial/NATURAL interface for command routing
- [ ] Create English → G-code translation script (Python)
- [ ] Connect to ChatGPT or local LLM via USB/serial
- [ ] Build context-aware diagnostics (e.g., last commands, job history)

## 🔁 Phase 4: Testing & Training

- [ ] Scripted motion tests (homing, jog, spindle, limits)
- [ ] Stability testing with AI feedback layer active
- [ ] Capture logs for training/debugging
- [ ] Version AI-interaction logic

## 🧭 Milestones

| Milestone | Status | Notes |
|-----------|--------|-------|
| Boot & blink | ☐ | Confirm dev board boots firmware |
| Basic motion | ☐ | Validate planner & step outputs |
| AI bridge | ☐ | Python CLI or LLM connected |
| Real feedback | ☐ | AI gives useful, state-aware responses |

