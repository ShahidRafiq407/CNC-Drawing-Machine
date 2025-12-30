# CNC Drawing Machine – Setup and Usage Guide

This repository provides a complete guide to set up and operate a CNC Drawing Machine using Arduino with GRBL, Inkscape, and UGS (Universal G-code Sender).

## Required Software

- Arduino IDE  
- Inkscape  
- UGS (Universal G-code Sender)

## Arduino IDE and GRBL Setup

### Install Arduino IDE

Download and install the Arduino IDE on your computer. Connect your Arduino board (Arduino Uno or Nano) to the computer using a USB cable.

### Add GRBL Library to Arduino IDE

The GRBL library is required to control the CNC drawing machine.

1. Download the GRBL library provided in this repository  
2. Open Arduino IDE  
3. Go to `Sketch → Include Library → Add .ZIP Library`  
5. Select zip file 
6. The GRBL library will be added successfully  

### Upload GRBL Firmware to Arduino

1. Open Arduino IDE  
2. Go to `File → Examples → grbl → grblUpload`  
3. The GRBL upload sketch will open  
4. Select the correct board and COM port  
5. Click Upload  
6. Wait until the upload process is completed  

After this step, the Arduino is ready to receive G-code commands.

## Inkscape and G-code Extension Setup

Inkscape software install it first is used to create drawings and convert them into G-code.
inkscape download link: https://inkscape.org/release/inkscape-0.92/?latest=1

### Install Inkscape G-code Extension

1. Download the extension ZIP file provided in this repository  
2. Extract the ZIP file  
3. Open the extracted folder  
4. Copy all files inside the folder  

### Locate Inkscape Extensions Folder

1. Right Click On Inkscape > click one > open file location 
2. then open the Share Folder  
3. Find the Extensions folder and open it.
The path usually looks like:
`Inkscape/share/extensions`

### Paste Extension Files

Paste all copied extension files into the extensions folder.  
After restarting, Inkscape will be able to convert drawings into G-code.

## UGS (Universal G-code Sender) Setup

UGS is used to send G-code files to the CNC drawing machine and control its movement.

### Install UGS

Download and install UGS on your computer. Connect the Arduino CNC machine to the computer using a USB cable.
https://winder.github.io/ugs_website/download/

### Run G-code on the Machine

1. Open UGS  
2. Select the correct COM port and baud rate  
3. Load the G-code file generated from Inkscape  
4. Click Run or Send  

The CNC drawing machine will start working.

## Workflow Summary

Arduino IDE → Upload GRBL  
Inkscape → Drawing to G-code  
UGS → Send G-code to Machine

## Notes

- Always test axis movement before running a full drawing  
- Start with simple designs before moving to complex drawings  
- Make sure pen height and alignment are properly adjusted  
- Stop the machine immediately if any unexpected movement occurs  

## Support

If you face any issues, feel free to open an issue in this repository or contribute improvements.
