# Coding Raspberry Pi Pico

## Objectives
- Program a [Raspberry Pi Pico](https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html).
- Manipulate GPIO pins to
  - output PWM signal
  - call interrupt on changed input signal
- Write math expressions. 

## Requirements:
### 1 Coding Exercises
Complete following 2 exercises to realize required effects on the hardware.
> [!NOTE]
> Please acknowledge AI's contributions according to the policies in the [syllabus](https://linzhanguca.github.io/_docs/robotics1-2025/syllabus.pdf)

#### 1.1 (30%) LED Dimmer
Complete [fade_in_fade_out.py](/fade_in_fade_out.py) to **endlessly** repeat fade-in and fade-out effect on an LED.
- (15%) Ramp up the brightness of an LED (from off to maximum) in **2 seconds**.
- (15%) Ramp down the brightness of the LED in **1 seconds**.
> [!TIP]
> Plan duty cycle increment size, steps of increment carefully to achieve a **smooth** fading effect.

#### 1.2 (50%) Mode Switching LED
Complete [switch_mode.py](/switch_mode.py) and use a button to switch an LED's working mode.
- (15%) **Mode 1**: LED (endlessly) fade in and fade out with a frequency of 1/4 Hz (equally allocate fade-in and fade-out time). 
- (5%) **Mode 2**: LED be **constantly on**.
- (15%) Press and **release** the button to switch mode (DO NOT make it a one-time thing). 
- (15%) Mode switching happens **instantaneously** at the moment the button is released.
> [!IMPORTANT]
> Use [IRQ](https://docs.micropython.org/en/latest/library/machine.Pin.html#machine.Pin.irq) to interrupt main task and handle button released event.

> [!TIP]
> - `for` loop is not recommended. 
> - Plan a cycle of actions in a very short period of time (e.g. 10 milliseconds).
> - Need to store mode value in a `global` variable? Check this [guide](https://www.w3schools.com/python/python_variables_global.asp).
> - Interrupt [tutorial](https://randomnerdtutorials.com/raspberry-pi-pico-interrupts-micropython/).
> - [Raspberry Pi Pico Python SDK](https://datasheets.raspberrypi.com/pico/raspberry-pi-pico-python-sdk.pdf)

### 2 (10%) Circuit Picture
Upload a picture of your actual circuit and display it below 👇

![wiring_pic](wiring.png)

> [!WARNING]
> The circuit picture has to be clear about Pico's GPIO pins connection with the LED and the button.
> The circuit has to match your code, or the coding credits won't be redeemed.

### 3 (10%) Fading Scheduling
Let's formulate fading effect in coding exercises with math language. 
Let $T$ represent time required for ramping brightness of the LED from one extremity to another.
And $n$ indicates number of duty cycle increments in the period of $T$.
Use $D_{max}$ as the maximal value for PWM signal's duty cycle.
Please write out the equation of the duty cycle's **increment** value, $s$, below :point_down:

> Type equation with LaTex syntax here.

> [!TIP]
> - Writing mathematical expressions [guide](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
> - LaTex math [cheat sheet](https://tug.ctan.org/info/undergradmath/undergradmath.pdf) for undergrads

> [!NOTE]
> Please acknowledge AI's contributions according to the policies in the [syllabus](https://linzhanguca.github.io/_docs/robotics1-2025/syllabus.pdf)
