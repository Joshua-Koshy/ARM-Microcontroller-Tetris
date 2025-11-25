# ARM Microcontroller Tetris – Custom Handheld System

This project implements a fully self-contained, handheld Tetris system built on an ARM Cortex-M0 microcontroller and a custom-designed PCB.  
The device integrates physical push-buttons, an analog slide-pot input, an ST7735R LCD, and audio output through a 12-bit DAC.

---

## 🧩 Hardware Overview

- **Custom PCB** designed for a standalone handheld game device  
- **ARM Cortex-M0 microcontroller** running all game logic in C  
- **ST7735R LCD** for sprite rendering and UI  
- **Push-buttons** for directional control and rotation  
- **Slide-pot (ADC)** used as an analog input method  
- **12-bit DAC** for generating game audio  
- Runs entirely on embedded hardware with **no external OS** or high-level libraries  

---

## 🛠 Firmware Architecture

### **Interrupt-Driven Control**
Hardware interrupts are used for:
- Button input sampling  
- ADC updates from the slide-pot  
- Periodic game ticks and drop timing  
- Audio waveform generation for game sound  

### **Finite State Machine**
The central FSM manages:
- Active gameplay  
- Tetromino spawning and movement  
- Locking, line clearing, and scoring  
- Menu and idle states  
- Audio timing and playback sequencing  

### **Rendering Engine**
Optimized drawing pipeline supporting:
- Moving tetromino sprites  
- Score and line count updates  
- Multi-language text  
- Partial-screen updates to maintain responsiveness  

---

## 🔌 Peripheral Integration

- **ADC** — reads slide-pot input for analog control  
- **DAC** — drives audio output via simple tone generation  
- **GPIO** — handles all physical button inputs  
- **SPI** — controls the ST7735R LCD display  
- **SysTick / hardware timers** — regulate real-time game loop timing  

---

## 📄 Summary

This project demonstrates a complete embedded game system built from the ground up—hardware, firmware, graphics, I/O, and timing—all running in real time on a Cortex-M0.  
It showcases interrupt-driven design, real-time processing, low-level peripheral control, and efficient rendering on a custom handheld PCB.

