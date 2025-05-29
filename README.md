Opamp based headphone amplifier. 

**Digital Side**

Momentary push button feeds a schmitt trigger and D flip flop to turn the board on and off. A USB-C connector with 5.1k resistors on the CC pins sets it up for 5V 3A max - this is mainly because I couldn't find a sufficiently simple USB-C PD Sink IC that I liked. Even the simple ones seemed overly complex so my conclusion is I'm not the target audience of where the industry is headed.

**Analog Side**

Isolated DC/DC converter takes 5V in and spits out +/-12V. This then feeds through an LDO to regulate the split rails at roughly +/-10V. Audio path is a 10k potentiometer, OPA1656 provides high and low pass filtering along with gain, then parallel stages of OPA1678 provide the output stage.

Sound quality is excellent although I already have a list of issues and improvements for next time. [Fixed] indicates the files uploaded here have this incorporated. I don't have a scope to make any measurements - only thing I checked was voltage rails and DC offset with my multimeter.

1. [Fixed] Connect LDO enable to VIN. (I had to make a daughterboard on the revision I built).
2. Anti-pop circuit on output.
3. [Fixed] Add cap (C35) so the on/off circuit defaults to off at power application.
4. Add switchable dummy load for testing before connecting headphones.
5. Trimpot for LED brightness.
6. Adjustable gain
