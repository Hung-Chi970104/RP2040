# RP2040 Hacker Board
- Demo video (with radio nrf24l01): https://youtu.be/eCMlnlmFBuc
- Demo video (radio control nrf24l01): https://youtu.be/_LA9TkBpY54

<img width="1920" height="1080" alt="RP2040_v2" src="https://github.com/user-attachments/assets/b3d5e7ee-f6e9-466a-8d1d-d9b3aecefc3c" />

- Upgraded flash storage from 2MB (W25Q16JVUXIQ TR) to 16MB (W25Q64JVXGIQ)
- Replaced MCP1700x-330xxTT (linear regulator) with RT6154AGQW (buck-boost switching regulator)
- Added Schottky Diode to allow external power supply
- Added a RESET button
- Changed 33pF crystal cap to 15pF to match the crystal I ordered

# Components
- RP2040
- 12MHz Crystal (ABM8-272-T3)
- 8MB Flash Storage (W25Q64JVXGIQ)
- Buck-Boost Switching Regulator (RT6154AGQW)
- USB-C (TYPE-C-31-M-12)

# Pinouts
| Pin Number (Left) | Description | Pin Number (Right) | Description |
| ------------- | ------------- | ------------- | ------------- |
| 1 | GPIO0 | 1 | VBUS |
| 2 | GPIO1 | 2 | VSYS |
| 3 | GND | 3 | GND |
| 4 | GPIO2 | 4 | GPIO28_ADC2 |
| 5 | GPIO3 | 5 | GPIO27_ADC1 |
| 6 | GPIO4 | 6 | 3V3 |
| 7 | GPIO5 | 7 | GPIO26_ADC0 |
| 8 | BOOTSEL | 8 | GND |
| 9 | GPIO6 | 9 | GPIO25 |
| 10 | GPIO7 | 10 | GPIO24 |
| 11 | GPIO8 | 11 | GPIO23 |
| 12 | GPIO9 | 12 | GPIO22 |
| 13 | GND | 13 | GND |
| 14 | GPIO10 | 14 | GPIO21 |
| 15 | GPIO11 | 15 | GPIO20 |
| 16 | GPIO12 | 16 | GPIO19 |
| 17 | GPIO13 | 17 | GND |
| 18 | GND | 18 | GPIO18 |
| 19 | GPIO14 | 19 | GPIO17 |
| 20 | GPIO15 | 20 | GPIO16 |

# PCBs

<img width="3168" height="1344" alt="demo_version2" src="https://github.com/user-attachments/assets/04ad3416-53a8-4cf7-979e-631923a92d10" />

- 2 layers
- Single-sided component placement
- 2.6mm board thickness
- HASL (with lead) surface finish
- 1oz outer copper weight

## PCB Schematic
<img width="2494" height="1814" alt="schematic" src="https://github.com/user-attachments/assets/2f404124-1a71-4bbb-a923-e40980d9ec2b" />

## PCB Layouts
<img width="227" height="461" alt="RP2040-B_Cu" src="https://github.com/user-attachments/assets/fef38dcd-ef37-42c8-be01-e9e805ce5d51" />
<img width="227" height="461" alt="RP2040-F_Cu" src="https://github.com/user-attachments/assets/1d6bd538-083b-46fe-a89b-8cda920bdbac" />

## 3D Model
<img width="1723" height="1012" alt="RP2040_front" src="https://github.com/user-attachments/assets/9be14ca6-f8fb-4720-85a3-5f705b16f463" />
<img width="1723" height="1012" alt="RP2040_back" src="https://github.com/user-attachments/assets/f1cf6687-d56a-4b40-b47f-1ff2e26d6f65" />

# Rendered Demo
<img width="2752" height="1536" alt="demo_2" src="https://github.com/user-attachments/assets/5446685d-ca1d-42a6-a059-7040e3894b44" />
<img width="2752" height="1536" alt="demo_3" src="https://github.com/user-attachments/assets/e5f58f69-4009-4052-be19-d63ecf7dbf12" />
<img width="1344" height="768" alt="demo_4" src="https://github.com/user-attachments/assets/7f9a6255-9d00-45be-b553-bae965c0db1b" />


