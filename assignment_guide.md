# Pico Practice

## 1. Overview
A robot needs a brain.
In Robotics I, a [Raspberry Pi Pico](https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html#pico2) serves as the core.
Let's get a head start on the course by practicing basic hardware wiring and coding with the Pico 2 board.

In this assignment, you will
- Set up a basic electronic circuit.
- Practice programming GPIO pins of the Pico 2 board.
- Familiarize pulse with modulation (PWM), timer, and interrupt. 
- Document math expressions.

## 2. Requirements

### 2.1. (15%) Wiring Up Pico and Peripherals
Wire up the the circuit as shown in the diagram below.
- (5%) Take a picture of your physical circuit and display it in [README](README.md).
- (8%) Images must be scaled to 800 × 600 pixels with a horizontal orientation.
- (2%) Please organize your circuit and reveal the connections with a clear view (position camera aptly and do not obscure key connections).

![wiring_diagram](/assets/images/wiring_diagram.png)

### 2.2. (40%) Light Up LEDs
Complete the coding tasks in [glow_leds.py](glow_leds.py) so the $\color{green}{\text{green}}$ and $\color{red}{\text{red}}$ LEDs run simultaneously.
- Green LED (**Breathing**): Implement an infinite breathing cycle using [`machine.PWM`](https://docs.micropython.org/en/latest/rp2/quickref.html#pwm-pulse-width-modulation).
  Fade in (0% brightness to 100%) smoothly over 2.0 seconds and fade out (100% brightness to 0%) over 1.0 second.
- Red LED (**Blinking**): Blink continuously at 5 Hz.
- Control at least one LED using a MicroPython [`machine.Timer`](https://docs.micropython.org/en/latest/rp2/quickref.html#timers) callback.
  Both LEDs must operate at the same time without blocking each other.
- (+5% Bonus) Drive the Green LED's PWM brightness updates entirely inside a `Timer` callback.
- (+5% Bonus) Use two separate `Timer` instances (one dedicated to the Green LED and one to the Red LED) to eliminate standard loops completely.

### 2.3. (40%) Switch Display Mode
Complete the coding tasks in [switch_mode.py](switch_mode.py) to control the $\color{green}{\text{green}}$ LED across two operational modes using a pushbutton .
- Mode 1 (Breathing): Green LED continuously fades in over 2.0 seconds and fades out over 2.0 seconds using [PWM](https://docs.micropython.org/en/latest/rp2/quickref.html#pwm-pulse-width-modulation).
- Mode 2 (Solid on): Green LED glows continuously at 100% brightness.
- Configure an interrupt ([`Pin.irq()`](https://docs.micropython.org/en/latest/library/machine.Pin.html#machine.Pin.irq)) on the pushbutton GPIO pin to handle state toggling via an Interrupt Service Routine (ISR) callback function.
- Mode switching must trigger upon releasing the button.
- LED modes must execute smoothly without stalling or preventing hardware interrupt detection.

### 2.4. (10%) Plan Breathing Schedule for LED 
Answer all post-test analysis questions in [README](/README.md) based on the observed result of your rail test.

### (10%) 2.4. Please acknowledge AI's contributions.
If you used generative AI tools during this assignment (e.g., for Markdown formatting or troubleshooting):
- Add an AI Acknowledgment section at the bottom of your README.md.
- State which tool was used and briefly describe how it assisted you.
- If no AI tools were used, explicitly state: "No AI tools were utilized for this assignment."

