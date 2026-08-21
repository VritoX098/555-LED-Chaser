# LED Chaser (Blinky Board)

A 10-LED chaser board built with a 555 timer and CD4017 counter. My first PCB design, made through Hack Club's Forge program.

---

![Schematic Render](Images/Schematic.png)

---

![PCB Render](Images/PCB.png)

---

## What it does

10 LEDs light up in sequence, one after another, creating a chasing effect. There's a potentiometer (RV1) that lets you adjust the speed of the chase, turn it one way and it goes fast, the other way and it slows down.

## How to use

1. Power it with 5V via the J1 header (2-pin socket)
2. The LEDs (D1-D10) will start chasing in sequence
3. Twist RV1 to change the blink speed

Pretty simple honestly. Plug it in and watch it go.

## Why I made this

Wanted to get into hardware and PCB design. This was the perfect beginner project to learn KiCad, understand how oscillators and counters work, and actually ship something physical. Also the batman shaped board just looks cool lol.

## What I learned

- How a 555 timer works (astable mode generates a clock pulse)
- How a CD4017 decade counter distributes that pulse across 10 outputs
- Difference between SMD and THT components
- What global labels are and why power flags exist
- How to import custom footprints (CD4017 wasn't in KiCad by default)
- PCB routing is harder than it looks (redid mine twice)


## BOM

| Reference | Qty | Value | Footprint | Datasheet |
|-----------|-----|-------|-----------|-----------|
| C1 | 1 | 1 uF | Capacitor_THT:CP_Radial_D5.0mm_P2.00mm | |
| C2 | 1 | 0.01 uF | Capacitor_THT:C_Disc_D7.5mm_W2.5mm_P5.00mm | |
| D1-D10 | 10 | LED | LED_THT:LED_D3.0mm | |
| J1 | 1 | Conn_01x02_Socket | Connector_PinHeader_2.54mm:PinHeader_1x02_P2.54mm_Vertical | |
| J2 | 1 | Conn_01x01_Socket | Connector_PinHeader_2.54mm:PinHeader_1x01_P2.54mm_Vertical | |
| R1 | 1 | 1k | Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P7.62mm_Horizontal | |
| R2 | 1 | 470 | Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P7.62mm_Horizontal | |
| RV1 | 1 | 50k | Potentiometer_THT:Potentiometer_Vishay_T93YA_Vertical | |
| U1 | 1 | NE555P | Package_DIP:DIP-8_W7.62mm | [Datasheet](http://www.ti.com/lit/ds/symlink/ne555.pdf) |
| U2 | 1 | 4017 | CD4017:N16 | [Datasheet](http://www.intersil.com/content/dam/Intersil/documents/cd40/cd4017bms-22bms.pdf) |

## Credits

Built through [Hack Club's Forge](https://forge.hackclub.com) program. 
