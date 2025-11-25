all resistors and cap should be 0805 size SMD

C1 10uF 0805 (smoothing for LDO)
C2 22uf 0805 (smoothing for LDO)
C3 10nf 0805 *optional* (bypass cap for MCU)

R1 ???? 0805 (this is the resistor that gose to the DCC rail IDK what its value is)
R2, R3 1k 0805 (these are the base resistors for Q1 & Q2, there was a big deal made finding the value of these, truth be told its not that important here [i think])
R4, R5 1k 0805 (these are the current limiting resistors for the LEDs in the train car)
R6, R7 10k 0805 *optional* (these are the optional pull up or pull down resistors for the GPIO lines going to Q1 & Q2. if you have problems with both outputs turning on when they shouldnt these may help: BUT YOU MUST ALSO SOLDER EITHER THE UP OR DOWN JUMPER [probably the DOWN jumper, that makes them off by defualt] just to be clear you dont need to install these unless you have an issue)

D1 B05S (this is the rectifer, i think you where using a B05S this should be the right size for that if you want to be sure you can look at the datasheet for your part and see if it says pakage:To-269AA)
D2 ???? SOD-123 (this is the reverse current protection diode it is a SOD-123 pakage which is a very common SMD diode. i think it is what you where using.)

U1 AtTiny85 (this is the MCU)
U2 LDI11117-05U (this is the LDO, the voltage regulator. this is the only part i wasnt sure about: idk if this is what you where using. if you go looking for this part make sure its says 05 [thats the voltage] after the '-' [the letter after the 5 dose not matter for this] )

Q1 & Q2 (standard NPN transitors set up as BEC meaning pin 1 is the base, pin 2 is the collector, and pin 3 is the emitter: like the ones you have in the video )

J1 & J2 (these are standared pin headers, they will allow you to proggram the MCU just like the breakout board you had. might not fit on a breadboard tho)
J3 (this is the DCC 6 pin connector with pin one shown by the triangle)



