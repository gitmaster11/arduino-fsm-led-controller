# Arduino FSM LED Controller

This project demonstrates a **professional Arduino LED control system**
using **Timer1 interrupts** and a **Finite State Machine (FSM)** approach.

The LEDs work in a timed sequence, support an **ALL ON / ALL OFF** mode,
and include an **EMERGENCY STOP** feature.

---

## 🚀 Features

- ⏱ Timer1 interrupt (1 second tick)
- 🧠 Finite State Machine (FSM) design
- 🔁 Sequential LED blinking
- 💡 ALL LEDs ON / OFF modes
- 🚨 Emergency stop button (instant shutdown)
- 📦 Clean and scalable code structure

---

## 🔌 Hardware Requirements

- Arduino Uno / Nano
- 3 LEDs (Red, Yellow, Green)
- 3 × 220Ω resistors
- 2 Push buttons
- Breadboard & jumper wires

---

## 📍 Pin Configuration

| Component | Pin |
|---------|-----|
| LED 1 | D2 |
| LED 2 | D3 |
| LED 3 | D4 |
| START Button | D5 |
| EMERGENCY Button | D6 |

Buttons are configured with `INPUT_PULLUP`.

---

## 🧠 State Machine Logic

### States:
- `IDLE` – LED sequence preparation
- `SEQUENCE` – LEDs turn ON one by one
- `ALL_ON` – All LEDs ON for 2 seconds
- `ALL_OFF` – All LEDs OFF, reset cycle

---

## ⏲ Timer Configuration

- Timer: **Timer1**
- Mode: **CTC**
- Prescaler: **1024**
- Interval: **1 second**

---

## 🛑 Emergency Mode

When the **EMERGENCY button** is pressed:
- All LEDs turn OFF immediately
- Timer counters reset
- System returns to `IDLE` state

---

## 📂 Project Structure

