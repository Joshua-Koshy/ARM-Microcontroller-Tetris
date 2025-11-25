ARM Microcontroller Tetris – Custom Handheld System
This project implements a fully self-contained, handheld Tetris system built on an ARM Cortex-M0 microcontroller and a custom-designed PCB.
The device integrates physical push-buttons, an analog slide-pot input, an ST7735R LCD, and audio output through a 12-bit DAC.

Hardware Overview


Custom PCB designed for a standalone handheld game device


ARM Cortex-M0 microcontroller running all game logic in C


ST7735R LCD for sprite rendering and UI


Push-buttons for directional control and rotation


Slide-pot (ADC) used as an alternative or analog input method


12-bit DAC for generating game audio


Powered entirely on embedded hardware with no external OS or libraries



Firmware Architecture
Interrupt-Driven Control


Hardware interrupts used for:


Button input sampling


ADC updates from slide-pot


Periodic game ticks and drop timing


Audio waveform generation




Finite State Machine


Central FSM controlling:


Active gameplay


Piece spawning and movement


Locking, clearing, and scoring


Menu/idle states


Audio timing and playback




Rendering Engine


Efficient drawing routines for:


Moving tetromino sprites


Score and line count


Multi-language text elements


Partial-screen updates to minimize latency




Peripheral Integration


ADC: Reads slide-pot input for analog controls


DAC: Generates simple tones and sound effects


GPIO: Handles physical buttons


SPI: Drives the ST7735R LCD display


SysTick or timer interrupts: Regulates game loop timing



Summary
This project demonstrates a complete embedded game system built from the ground up—hardware, firmware, graphics, I/O, and timing—all running in real time on a Cortex-M0.
It combines low-level control, interrupt-driven design, and peripheral coordination to create a responsive handheld Tetris experience on custom hardware.

If you want, I can also generate:


A schematic diagram section


A gif-style README header for GitHub


A “Features” table formatted like professional embedded repos


A photos section if you upload PCB or device pictures

