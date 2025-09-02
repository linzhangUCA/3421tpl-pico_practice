# Coding on Raspberry Pi Pico

## Objectives
- Practice programming a [Raspberry Pi Pico](https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html).
- Practice operations on GPIO pins.
- Get familiar with [coding tools](https://docs.micropython.org/en/latest/library/rp2.html).

## Requirements:
Please complete the two python scripts prepared in this repository. Verify the required functionalities.

### (40%) LED Dimmer
Work in [fade_in_fade_out.py](/fade_in_fade_out.py) and realize following effect on an LED.
Repeat the process of gradually increasing and decreasing the brightness of an LED using Raspberry Pi Pico.
- (10%) Ramp up the brightness of the LED in 2 seconds.
- (10%) Ramp down the brightness of the LED in 1 seconds.
- (20%) Repeat previous two steps **forever**.

**Tips**: 
- To create an increasing sequence: `range(n)`. To create a decreasing sequence: `reversed(range(n))`
- Maximum PWM duty cycle is `65025`.
- `for` loop is optional.

### (60%) [`switch_mode.py`](/switch_mode.py)
Make an LED running under two modes. Use a button to switch the mode.
- (12%) **Mode 1**: set the LED to **endlessly** fade in and fade out. Please equally allocate fade-in and fade-out time. Set the frequency to 1/4 Hz.
- (8%) **Mode 2**: set the LED to **constantly on**.
- (20%) Press (and release) the button to switch between the modes. This function is expected to be valid all the time. **DO NOT make it a one-time thing**.
- (20%) Mode switching happens **instantaneously**.

**Tips**: 
- Try to plan actions in a very short period of time (e.g. 10 milliseconds).
- Try to switch mode with [interrupt](https://www.upesy.com/blogs/tutorials/hardware-interrupts-rpi-pico-on-micropython?srsltid=AfmBOooNL06A7YB1HmKTClu3PhqEixfZSOmMBzPt_Qr6z3RMDosgF3Pl) mechanism.
- Can't switch mode in irq handling function? You may need help from [global variable](https://www.w3schools.com/python/python_variables_global.asp).
- Using `for` loop could be a bad choice. 
- You can either start with **Mode 1** or **Mode 2**.
 
## Further Instructions
- You can use the built-in LED or an external LED.
- Solderless breadboard is optional.
- Refer to the wiring diagrams in this [tutorial](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/6).
- For more details on coding Raspberry Pi Pico using Micropython, refer to the official [handbook](https://datasheets.raspberrypi.com/pico/raspberry-pi-pico-python-sdk.pdf?_gl=1*1ydsxhc*_ga*NjEyNDE4MjQ3LjE3MjUwNTIzMzE.*_ga_22FD70LWDS*MTcyNTQ4NTEyMy4zLjEuMTcyNTQ4NTIyOC4wLjAuMA..).
