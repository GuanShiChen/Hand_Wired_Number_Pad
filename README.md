
# Custom Hand-Wired Number Pad

A DIY hand-wired number pad using a **Pro Micro controller**, **QMK firmware**, and a **fully 3D printed case and plate**. This project is ideal for hobbyists and mechanical keyboard enthusiasts looking to build their own compact keypad.

---

## Features

- 17-key standard numpad layout  
- Hand-wired matrix circuit with diodes  
- Powered by an ATmega32u4 Pro Micro  
- Fully compatible with QMK Firmware  
- 3D printed case and plate  
- Fully customizable layout  

---

## Materials

| Item                      | Quantity | Notes                          |
|---------------------------|----------|--------------------------------|
| Pro Micro (ATmega32u4)    | 1        | Micro USB or USB-C             |
| Mechanical Switches       | 17       | MX-compatible                  |
| Keycaps                   | 17       | Numpad set                     |
| Stabilizers (2U)          | 3        | For `0`, `+`, and `Enter`      |
| Diodes (1N4148)           | 17       | For matrix wiring              |
| Solid Core Wire           | -        | Used for matrix rows/columns   |
| 3D Printed Case & Plate   | 1 each   | STL files included             |
| USB Cable                 | 1        | To connect Pro Micro to PC     |

---

## Wiring Overview

- Diodes are placed on the **row side**, with the **cathode (marked side)** facing the row wire  
- Each switch is connected to a **row and a column wire** to form a matrix  
- Wires are soldered directly to switch terminals and routed to the Pro Micro pins  

---

## Firmware Setup (QMK)

### QMK Setup

1. **Clone the QMK repository:**

        git clone https://github.com/qmk/qmk_firmware.git
        cd qmk_firmware
        qmk setup

2. **Create a new keyboard layout:**

        qmk new-keyboard

3. **Follow the prompts and create your directory under:**

       keyboards/handwired/numpad

4. **Customize the following files:**

    * `info.json`
    * `keymap.c`

    <br>

    *Sample code can be found in the `/Code/` directory


### Build & Flash

    qmk compile -kb handwired/numpad -km default
    qmk flash -kb handwired/numpad -km default


*Make sure your Pro Micro is in **bootloader mode** (double tap reset) when flashing.

---

## 3D Printed Case and Plate

* CAD and STL files are located in the `/CAD/` directory
* Designed in **Autodesk Inventor**

**Print Settings:**

* Printer: Bambu Lab P1S
* Layer Height: `0.2mm`
* Infill: `20–30%`
* Supports: **Yes** (for screw holes)

---

## Gallery

### Finished Numpad
<img src="/Pictures/Final Side.jpg" alt="Final Side" width="500"><br>
<img src="/Pictures/Final Front.jpg" alt="Final Front" width="500"><br>

### Wiring View
<img src="/Pictures/Soldering In Progress.jpg" alt="Soldering In Progress" width="500"><br>
<img src="/Pictures/Testing Back.jpg" alt="Testing Bac" width="500"><br>
<img src="/Pictures/Testing Front.jpg" alt="Testing Front" width="500"><br>
<img src="/Pictures/Back Neat.jpg" alt="Back Neat" width="500"><br>

---

## Acknowledgments

* Based on the [QMK hand-wiring guide](https://docs.qmk.fm/#/hand_wire)
* Inspired by builds on [r/MechanicalKeyboards](https://www.reddit.com/r/MechanicalKeyboards/)
