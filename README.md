# Lobola — Open-Source Pap-Cooking Robot

**Lobola** is an open-source robotic system that automates the cooking of *pap* (also known as *sadza* or maize porridge). This repository contains the complete material design and control software for the system: electrical schematics, mechanical CAD models, and the embedded firmware.

## Overview

The robot mechanises the manual steps of cooking pap — feeding maize meal, stirring, lid actuation, and heat control — using a combination of stepper, servo, and DC motors driven by an Arduino. The intended cooking sequence is documented in [`Sequence for Cooking Pap.pdf`](Sequence%20for%20Cooking%20Pap.pdf).

## Hardware

| Subsystem | Actuator | Function |
|---|---|---|
| Lid | Stepper motor | Raises / lowers the pot lid |
| Lead screw | Stepper motor | Drives the screw mechanism |
| Feed | Servo motor | In/out maize-meal feed motion |
| Stove | Servo motor | On/off heat control |
| Mixer | DC motor | Stirring (speed set by a potentiometer) |

Operation is driven by panel buttons (lid, feed, screw, stove) and a potentiometer for mixer speed. The full wiring is in [`circuit diagram.pdf`](circuit%20diagram.pdf).

## Repository contents

| Path | Description |
|---|---|
| [`CAD model/`](CAD%20model) | Autodesk Inventor parts and assemblies |
| `button_version.ino` | Arduino firmware (button-driven control) |
| `circuit diagram.pdf` | Electrical schematic |
| `Sequence for Cooking Pap.pdf` | Cooking process / control sequence |
| [`images/`](images) | Renders and photographs of the assembly |

### CAD

The main assembly is **`rapid-prototype.iam`**. Sub-assemblies include `feed.iam`, `mixer.iam`, `lid_assembly.iam`, `roller.iam`, and `LeadScrewMotor.iam`. Open these in **Autodesk Inventor** or **Fusion**.

### Firmware

`button_version.ino` targets the **Arduino IDE** and depends on the `Servo`, `AccelStepper`, and `MultiStepper` libraries. Install these via the Arduino Library Manager, then upload to your board.

## License

Released under the terms in [`LICENSE.txt`](LICENSE.txt).

## Contact

For questions, email **rabs.mike@yahoo.com** with the subject **"open-source-lobola"**.
