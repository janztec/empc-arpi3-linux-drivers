# emPC-A/RPI3, emPC-A/RPI3+, emVIEW-7/RPI3 & emVIEW-7/RPI3+ by Janz Tec AG 

This script installs and configures Linux **Socket CAN**, **Serial port RS232/RS485** and **RTC** drivers.

## :large_orange_diamond: Installation Instructions

_Create a backup copy of your µSD card before applying these steps!_

**Step 1:**

Install the Raspberry Pi OS 32-bit:  
https://www.raspberrypi.com/software/

_The install script was tested with Kernel version 5.15, 5.10, 5.4 and 4.19._
_Older or later versions may not work!_


**Step 2a:**


```
sudo bash
cd /tmp
wget https://raw.githubusercontent.com/janztec/empc-arpi3-linux-drivers/master/install.sh -O install.sh
bash install.sh
```


<br />
<br />
<br />


**Step 2b (Alternative if step 2a fails):**

Depending on the installed Linux kernel version it might be possible, that no matching kernel headers are available in the official Rasbian repository and step 2a fails. In this case it is possible to install the specific kernel version 20220308-2_armhf with matching kernel headers manually.
Select "No" in the "Do you want to install the latest kernel headers" prompt!

```
cd /tmp
sudo bash
wget https://archive.raspberrypi.org/debian/pool/main/r/raspberrypi-firmware/raspberrypi-kernel_1.20220308-2_armhf.deb
dpkg -i raspberrypi-kernel_1.20220308-2_armhf.deb
wget https://archive.raspberrypi.org/debian/pool/main/r/raspberrypi-firmware/raspberrypi-kernel-headers_1.20220308-2_armhf.deb
dpkg -i raspberrypi-kernel-headers_1.20220308-2_armhf.deb

reboot

sudo bash
cd /tmp
wget https://raw.githubusercontent.com/janztec/empc-arpi3-linux-drivers/master/install.sh -O install.sh
bash install.sh
```

<br />
<br />
<br />

## Product page
https://www.janztec.com/industrie-pcs

**emPC-A/RPI3**

![emPC-A/RPI3](https://www.janztec.com/wp-content/uploads/2020/03/emPC_A_RPI_front.png.webp)

**FEATURES emPC-A/RPI3**
* Processor 
  * Based on Raspberry Pi 3, Model B 
  * Broadcom BCM2837 processor 
  * Quad-Core CPU based on ARM Cortex-A53 
  * Fanless cooling concept 
  * Realtime clock, battery buffered 
* Memory 
  * System memory 1 GB 
  * External accessible ÂµSD card slot  
* Graphics 
  * HDMI graphic interface  
* Connectors  
  * 1 x 10/100 MBit/s Ethernet 
  * 4 x USB (v2.0) 
  * 1 x 9-pin D-SUB connector for serial debug console 
  * 1 x CAN (ISO/DIS 11989-2, opto-isolated, termination settings via jumper) 
  * 1 x RS232 (Rx, Tx, RTS, CTS) or switchable to RS485 (half duplex; termination settings via jumper)  
  * Internal I/O  
    * 4 x digital inputs (12 - 24VDC) 
    * 4 x digital outputs (12 - 24VDC)  
* Power Supply  
  * Input 9 â€¦ 32 VDC 
* DIN rail, wall mounting or desktop 

-------

**emVIEW-7/RPI3**

https://www.janztec.com/panel-pcs

![emVIEW-7/RPI3](https://www.janztec.com/wp-content/uploads/2020/03/janz_tec_produkte_embedded_emVIEW-7_RPI3_front-1.png.webp)

**FEATURES emVIEW-7/RPI3**
* LCD Display
   * 7.0" WSVGA display size
   * LED backlight technology
   * Resolution 800 x 480
   * Projected capacitive touch screen (PCAP) (with multitouch capabilities)
   * Glass surface
* Same I/O as emPC-A/RPI3


