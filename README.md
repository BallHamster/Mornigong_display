# Mornigong_display
Welcome all to my project mornigong, and this part of it: Mornigong display.
This project uses a cheap aliexpress eink raw screen (Image below), a raspberry pi zero 2 w, and a custom made driver board for the screen.
<img src="Images/screen.png" alt="Screen" width="600">
## The board I made
<img src="Images/schematic.png" alt="Schematic" width="600">
This is the schematic of my board. The connector is an FPC 24 pin cable, carrying SPI data, and power for the screen. As the screen has no power onboard, I had to make the power boost circuit too. It is largely based on the official Waveshare esp32 driver board V3.(Source: https://files.waveshare.com/wiki/E-Paper-ESP32-Driver-Board/E-Paper_ESP32_Driver_Board_V3.pdf?)
<img src="Images/pcb.png" alt="PCB" width="600">
This is the final PCB layout, and routing. Everything is close to the components it needs to be. (Or I hope so...)
<img src="Images/table.png" alt="Table of resistors" width="600">
This is a help table for the resistor voltages with the reference numbers.

<img src="Images/3d.png" alt="3d render" width="600">
This is the 3d render of the board. It is designed to be a hat for the zero 2 w.

## Software
The software I used, is as open-source project, called Inkypi, made by Faith Ak. (https://github.com/fatihak/InkyPi)
### Installation guide
- Write an image of an official Raspberry pi OS lite 64bit on your sdcard/usb drive.
- Clone the repository: ```git clone https://github.com/fatihak/InkyPi.git```
- Navigate to the project directory: ```cd InkyPi```
- Run the installation script with sudo: ```sudo bash install/install.sh -W epd7in5b_HD``` (as the screen I am using is an exact copy of the Waveshare 7.5 in model.)
- Restart your pi
- Head to https://<your_pi_ip> for configuration and first time setup.

### Example software
There is a copy of an example software in this repo, called "ex_software.bin" which is an image of the directory of Inkypi on my RPI with my screen model.

# Important
- This project is not tested yet, it only works in theory.
- All the credits go to Faith ak, for the Inkypi software.
# BOM
| Reference number | Description | LCSC part number | Needed number | Minimum order number | Price of minimal order number/needed number ($) | link |
|---|---|---|---|---|---|---|
| C7, C8, C10, C12, C13, C14, C15, C16, C17, C18, C19 | 1 uF 50 V X7R 0805 MLCC, Kyocera AVX 08055C105KAT2A | C2167382 | 11 | 15 | 2.5 | https://www.lcsc.com/product-detail/C2167382.html |
| C20 | 10 uF 25 V X5R 0805 MLCC, Samsung CL21A106KAYNNNE | C15850 | 1 | 20 | 0.88 | https://www.lcsc.com/product-detail/C15850.html |
| C21 | 100 nF 50 V X7R 0805 MLCC, Samsung CL21B104KBCNNNC | C1711 | 1 | 20 | 0.28 | https://www.lcsc.com/product-detail/C1711.html |
| D1, D2, D3 | Schottky diode 30 V 0.5 A SOD-123, onsemi MBR0530T1G | C82046 | 3 | 10 | 0.63 | https://www.lcsc.com/product-detail/C82046.html |
| L1 | 47 uH shielded inductor 4.8x4.8x2.8 mm, Bourns SRR4028-470Y | C2041925 | 1 | 1 | 0.43 | https://www.lcsc.com/product-detail/C2041925.html |
| Q1 | N-MOSFET 30 V SOT-323, Vishay Si1308EDL-T1-GE3 (Si1304BDL helyett) | C469327 | 1 | 5 | 1.31 | https://www.lcsc.com/product-detail/C469327.html |
| R1 | 0.47 ohm 1% 0805, Yageo RL0805FR-070R47L | C705493 | 1 | 50 | 0.73 | https://www.lcsc.com/product-detail/C705493.html |
| R2 | 100 kohm 1% 0805, Yageo RC0805FR-07100KL | C96346 | 1 | 100 | 0.47 | https://www.lcsc.com/product-detail/C96346.html |
| R5 | 3 ohm 1% 0805, Yageo RC0805FR-073RL | C137528 | 1 | 50 | 0.94 | https://www.lcsc.com/product-detail/C137528.html |
| U1 | FPC connector 24 pin 0.5 mm, SHOU HAN FPC 0.5-24P | C6364666 | 1 | 5 | 0.86 | https://www.lcsc.com/product-detail/C6364666.html |
| J1 | 2x20 pin 2.54 mm pin header | C2977589 | 1 | 5 | 1.62 | https://www.lcsc.com/product-detail/C2977589.html |
| - | Screen | - | 1 | 1 | 15 | https://www.aliexpress.com/item/1005006901112592.html |
| U2 | Raspberry pi zero 2 w | - | 1 | 1 | 20 | https://malnapc.hu/raspberry-pi-zero-2-w?src=raspberrypi |
