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

### 2.2. (60%) Two LEDs
Complete the coding tasks in [glow_leds.py](glow_leds.py), so the $\color{green}{\text{green}}$ and $\color{red}{\text{red}}$ LEDs run simultaneously.
- Green LED (**Breathing**): Implement an infinite breathing cycle using [`machine.PWM`](https://docs.micropython.org/en/latest/rp2/quickref.html#pwm-pulse-width-modulation).
  Fade in smoothly over 2.0 seconds ($0% to 100% duty cycle) and fade out over 1.0 second (100% to 0% duty cycle).
- Red LED (**Blinking**): Blink continuously at 5 Hz.
- Control at least one LED using a MicroPython [`machine.Timer`](https://docs.micropython.org/en/latest/rp2/quickref.html#timers) callback.
  Both LEDs must operate at the same time without blocking each other.
- (+5% Bonus) Drive the Green LED's PWM brightness updates entirely inside a `Timer` callback.
- (+5% Bonus) Use two separate `Timer` instances (one dedicated to the Green LED and one to the Red LED) to eliminate standard loops completely.

### 2.2. (20%) Observe and log the rail test
Observe closely and record your observations from the rail test directly in the designated section of [README](/README.md).

### 2.3. (10%) Analyze the rail test
Answer all post-test analysis questions in [README](/README.md) based on the observed result of your rail test.

### (10%) 2.4. Please acknowledge AI's contributions.
If you used generative AI tools during this assignment (e.g., for Markdown formatting or troubleshooting):
- Add an AI Acknowledgment section at the bottom of your README.md.
- State which tool was used and briefly describe how it assisted you.
- If no AI tools were used, explicitly state: "No AI tools were utilized for this assignment."

## 3. Reading Resources
- [Github documentation syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Engineering drawing views reference](https://engineering.stackexchange.com/questions/15885/top-view-front-view-left-view-and-right-view-help)
