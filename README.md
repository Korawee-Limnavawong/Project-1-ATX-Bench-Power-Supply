# Project 1: ATX Bench Power Supply
This project is a mid-term exam for electronic circuit lab
## Project Overview & Team

*   **Team Members:** Korawee Limnavawong, pandin sriraso
*   **Individual Contributions:** Korawee wiring [e.g., electrical design, wiring and calculations], while pandin managed [e.g., Acrylic, design and Testing]
*   **Project Summary:** Conversion of a closed-case ATX PC power supply into a safe, multi-rail bench power source featuring fixed rails (+3.3V, +5V, +12V, -12V) and one adjustable buck-boost output.
*   **Source PSU:** SVOA 200w
*   **Accepted Requirements:** Provide properly fused and insulated fixed rails, an adjustable output, a dedicated PS_ON control, and clear standby/run indicators.

## Safety & Stop Conditions

*   **Safety Boundary:** The metal source PSU enclosure remains permanently closed. All internal high-voltage circuits are unmodified. Wiring changes are only performed with the AC cable physically removed.
*   **Risk Assessment:** Primary risks include accidental short circuits on the high-current rails and thermal overload.
*   **Stop Conditions:** Operation will immediately halt if rails repeatedly cycle, voltage exceeds ±5% of nominal, unexpected smoke/odor occurs, or fuses blow.

## Source PSU Specifications

*   **Label Transcription:** +3.3V (20A), +5V (20A), +12V (37.4A), +5VSB (3A). Total combined power: 450W.
*   **Verified Connector View:** <img width="1043" height="1000" alt="image" src="https://github.com/user-attachments/assets/cfec91a4-a2f1-4a5c-9faa-0c89e66f05dd" />


## Hardware Design

<img width="1129" height="1000" alt="image" src="https://github.com/user-attachments/assets/f73041de-12bc-460e-8b45-070280ae4555" />


### Bill of Materials (BOM)

| Identifier | Part Description | Rating | Cost (THB) | Datasheet/Source |
| :--- | :--- | :--- | :--- | :--- |
| **ENC1** | Acrylic Enclosure 20x20x3mm | 6 pieces | 120 | https://surl.li/oaeswx |
| **PSU1** | ATX Power Supply 200w | 1 piece | 100 | https://surl.li/wjwtxk |
| **MOD1** | Buck-Boost Converter Module | In: 5-30V, Out: 0.5-30V, 4A | 315 | https://surl.li/lyspwq |
| **Fuses** | Fast-acting Fuses 10A, 250V | 4 pieces | 1x4=4 | https://surl.li/ypimlq |
| **Banana jack** | Binding Posts 10A, 30VDC | 6 pieces | 12x6=72 | https://surl.li/ewixke |
| **Paint spay can** | Black color spays | 2 can | 2x65=130 | https://surl.li/hrrlbh |
| **LED strip** | Warm light 5v | 140mm | 14 | https://surl.lt/vojzup |
| **CLTF-006** | DC Socket 12V | 1 piece | 58 | https://surl.li/lwsadb |
| **LED diode** | Red and green | 2 pieces | 10 | https://surl.li/vroghq |
| **Switch** | SWITCH ROCKER SPST 10A 125V | 1 piece | 44 | https://surl.li/rikeey |
| **Total** | | | **867** | |

## Engineering Calculations

*   **Branch-Protection:** Calculated fuse limits based on 18 AWG wire ampacity (rated for up to 16A; 5A fuses selected for safety margin).
*   **Converter & Loss Calculations:** $P_{in} \approx V_{out} I_{out} \eta$ (Assuming 85% efficiency for buck-boost module).
*   **Thermal Calculations:** Expected power dissipation at full test load ($P=I^2R$), ensuring it remains below the 60°C component limit.

## Construction Evidence
**picture of a original wire from cutting all pin head**

<img width="281" height="367" alt="image" src="https://github.com/user-attachments/assets/58e33ac4-5e17-4220-ba36-7f88a90de681" />
 
 **Picture of front display side**

<img width="281" height="367" alt="image" src="https://github.com/user-attachments/assets/86e84773-fb4a-43ad-9c7c-97f34ec07abd" />

**Picture of completed project**

<img width="281" height="367" alt="image" src="https://github.com/user-attachments/assets/2b5d1934-aff7-4afc-8845-95e616a2c020" />
<img width="281" height="367" alt="image" src="https://github.com/user-attachments/assets/17573818-8147-4d0a-b81a-d8f08c1a66d1" />

## Testing & Acceptance Evidence

### Unpowered Checks: Resistance
*   From +3.3V to GND measured at [X] Ohms; no rail-to-rail shorts detected.
*   From +5V to GND measured at [X] Ohms; no rail-to-rail shorts detected.
*   From +12V to GND measured at [X] Ohms; no rail-to-rail shorts detected.

### First-Power & Minimum Load
*   **+3.3VSB:** verified at 3.47V. Supply latched successfully with zero external dummy load.
*   **+5VSB:** verified at 5.07V. Supply latched successfully with zero external dummy load.
*   **+12VSB:** verified at 12.3V. Supply latched successfully with zero external dummy load.

### Output & Thermal Verification
*   **Adjustable Output:** Verified sweep from 0V to 30V.
*   **Thermal Evidence:** Maximum recorded temperature on the +12V fuse holder after 15 minutes at 3A load was 38°C.

## Faults & Corrections

*   **Faults:** Switch are bypassed so supply are always activated.
*   **Corrections:** Change the location of switch.

## Operations & Maintenance

*   **Operating Instructions:** Connect AC. Verify standby LED is on. Flip the maintained PS_ON switch to activate main rails.
*   **Fuse Replacement:** Ensure AC is removed. Unscrew front-panel holders and replace only with 5A fast-acting 5x20mm glass fuses.
*   **Shutdown Procedure:** Turn off PS_ON switch, disable rear PSU power switch, unplug AC cable, and wait 30 seconds for capacitor discharge before removing load wiring.

## References
*   https://youtu.be/lqjbFdLXqzc?si=r5jWkOlRb0nyuO8n
*   https://youtu.be/SDymqPkvnT8?si=ZPhvJBW4Xwf9AMxp
*   https://youtu.be/n_A-jkpjpcM?si=-UoGcW_YMxG6ikI9
