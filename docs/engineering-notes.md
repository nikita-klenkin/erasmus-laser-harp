# Technical and development notes

This document summarizes the available project log and saved visual documentation. It does not include the project's original software, schematics or CAD source files.

## Project purpose and result

Build an eight-beam interactive musical instrument that detects interrupted laser beams and plays corresponding notes. A Raspberry Pi acts as the main software controller; the ESP32 handles sensor events. The final instrument was assembled and demonstrated at the end of the Erasmus+ project in Slovakia in September 2026.

## Key architectural elements

- **Inputs:** eight laser beams and corresponding light sensors.
- **Microcontroller:** ESP32 detects the beam interruptions; sensor values were inspected in the serial monitor during early tests.
- **Interface:** USB serial transmission to the Raspberry Pi.
- **Processing:** a Python application handles incoming events and triggers corresponding musical notes through FluidSynth.
- **User interaction:** touchscreen GUI built as an additional interface for settings such as instrument and sound selection.
- **Mechanical integration:** 3D-printed housing elements plus a laser-cut acrylic front panel.

## Selected milestones

| Date | Milestone |
|:--|:--|
| Before 20 September 2026 | Project idea, concept and component selection in Germany |
| 21 September | First laser, LDR and ESP32 tests; sensor readings in the serial monitor |
| 22 September | LDRs and phototransistors evaluated; one interrupted beam successfully detected |
| 23 September | Raspberry Pi set up; Python and FluidSynth produced first note |
| 24 September | More stable single-beam prototype; automated USB-port detection in Python |
| 25–28 September | 3D printing, acrylic work, GUI development, soldering and assembly |
| 29 September | Final integration, system test and project presentation |

## Problems and responses

**Sensor choice**  
The team initially tested light-dependent resistors but selected phototransistors after observing more reliable beam detection. The saved record does not document numerical comparative sensor accuracy.

**Mechanical instability**  
An improvised build caused false triggers during hand movement. A custom 3D-printed holder improved alignment and triggering stability.

**Startup/setup issue**  
A defective SD card delayed the Raspberry Pi setup. The system was configured with a working card during subsequent development.

**Device-port assignment**  
The Python script was extended to automatically detect the USB port for the ESP32, rather than assuming one constant device name.

**Scope adjustment**  
The initial design aimed to detect hand distance for octave control. Because the initial distance sensor readings were unreliable, the team focused on eight individually triggered laser strings.

## Available documentation vs. missing artifacts

**Available:** project narrative, milestone history, photos of the electronics and mechanical design, and demonstrations of the working final instrument.

**Not available in this repository:** full circuit diagram and pin mapping, original project code, package versions, production-ready CAD source files, tested assembly instructions or a bill of materials. No claim is made that the project can be fully reproduced from these notes alone.

## Individual participation

I contributed to several parts of the team effort. I did not independently build every component. Technical decisions and final outcomes are documented as shared team work.
