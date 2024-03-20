# Introduction

 This is a kit for the VORON 0.2. FYSETC Voron 0. 2 Pro R1 Kit.

# Feature 

The new **Voron 0. 2 Pro R1 Kit** has a new design for the electronic part, which is easier to connect and configure, and is as close as possible to out-of-the-box use.

# BOM

[Voron 0.2 R1 Pro](https://github.com/FYSETC/FYSETC-Voron-0.2/blob/main/0.2%20R1/BOM.md)


# STL changes

### Additional STLs

Check it [here](https://github.com/FYSETC/FYSETC-Voron-0.2-Pro/tree/main/0.2%20R1/STL/ADD).


### Hotend Mount

Check it [here](https://github.com/FYSETC/FYSETC-Voron-0.2-Pro/blob/main/0.2%20R1/STL/Toolheads/Hotend_Mounts/Fan_Saver/%5Ba%5D_FS_Hotend_Mount_Dragon.stl)


### Unnecessary STLs
- Rear_Bed_Mount_Right_x1.stl
- Front_Bed_Mount_x1.stl
- Rear_Bed_Mount_Left_x1.stl
- Drag_Chain_Spacer_x1.stl
- PCB_DIN_Clip_x2.stl
- PCB_DIN_Clip_x2.stl
- Fan_Mount_Bottom_x1.stl
- VHB_DIN_Mount.STL
- VHB_DIN_Mount.STL
- Fan_Mount_Top_x1.stl
- M2_Nut_Adapter_Rotated_x5.stl

# Wiring

### R1 Pro kit

Following is our Catalyst board wiring diagram for VORON 0.2 R1 pro kit.

![](https://github.com/FYSETC/FYSETC-Voron-0.2-Pro/blob/main/0.2%20R1/Fysetc%20Voron%20V0.2%20R1%20umbilical%20Wiring.jpg)

# Installation Guide 

### Page 190 "ELECTRONICS & WIRING"

Following the Catalyst board wiring diagram for VORON 0.2 pro R1 kit.

Check it [here](https://github.com/FYSETC/FYSETC-Voron-0.2-Pro/blob/main/0.2%20R1/Fysetc%20Voron%20V0.2%20R1%20umbilical%20Wiring.pdf).


# Firmware&OS

## CM68 OS 

<p style="color: green">
<strong>
The control board of this kit has been installed with Klipper OS and MCU Klipper firmware at the factory. And it's pre-configured.
As long as the wiring is correct, it can be used after power on.
</strong>
</p>

<p style="color: red">
<strong>
Do not perform the following steps unless you are sure you want to reinstall the firmware.
</strong>
</p>

The control board uses the CM68 core based on RK3568 as the upper computer of Klipper. Its system is compiled based on Debian 10, and the environment and plug-ins required by Klipper are pre-installed. After burning, it can be used directly.

In general, the pre-installed system can be used directly without re-flashing, unless you encounter unsolvable program problems.

The OS of CM68 (voron-02-pro):

1. Install klipper and its necessary plug-ins in the initial version (Debian10):</br>
file name: rk3568-debian10-voron02pro-mainsail.rar</br>
Download：</br>
https://drive.google.com/file/d/13Tcclv2N4jrMm01r_HPVqZ3v6CVUCk1H/view?usp=drive_link


2. bugfix (Debian10) Install klipper and its necessary plug-ins:</br>
file name: cm68-debian10-voron02pro-mainsail-20230923-154632.img</br>
Fix "vdd_cpu: ramp_delay not set" warning</br>
Download：</br>
https://drive.google.com/file/d/13Tcclv2N4jrMm01r_HPVqZ3v6CVUCk1H/view?usp=drive_link


3. 5.1 kernel, Debian11, install klipper and its necessary plug-ins:</br>
file name: cm68-debian11-voron02pro-part-20231107-1211.img</br>
Download：</br>
https://drive.google.com/file/d/1rhYSTQhsnIySWOnArb-KzfS_5ioayIdm/view?usp=drive_link</br>

4. 5.1 kernel, Debian11, install all plug-ins supported by kiauh.</br>
**file name:** cm68-debian11-voron02pro-all-20231107-1157.img</br>
**Download:** </br>
https://drive.google.com/file/d/1RwSsYh74uzc6N8ZZUWCPG4JZDjomelVW/view?usp=drive_link
Google Docs

**5 & 6 Fixed the RTL8188EUS WIFI Diver issue** </br>

5. 5.1 kernel, Debian11, install all plug-ins supported by kiauh.</br>
**file name:** cm68-debian11-voron02pro-all-20231215.rar</br>
**Download:** </br>
https://drive.google.com/file/d/1aGxkKDje69fH9lJNZlRNIsSG2d_Z3Y20/view?usp=drive_link/</br>

6. 5.1 kernel, Debian11, install klipper and its necessary plug-ins:</br>
**file name:** cm68-debian11-voron02pro-part-20231215.rar</br>
**Download:** </br>
https://drive.google.com/file/d/1jtd5bbeK2osySYbc_Y-N9HqvL0vuzt-D/view?usp=drive_link/</br>


Update steps:
1. Power on VORON with AC Power. Then plug in the USB3.0 A-A cable into the interface on the upper layer of the blue USB3.0 socket.
2. Open the "RKDevTool_Release",
4. Click the Upgrade Firmware (升级固件) tab, click the Firmware (固件) button to select the firmware, and click the Upgrade button to upgrade  
   ![image](https://github.com/Psych0h3ad/FYSETC-Voron-0.2-Pro/assets/41975091/b0f80d14-62ae-452b-8478-029408acbbba)  
   After selected firmware, it will show like as below  
   ![image](https://github.com/Psych0h3ad/FYSETC-Voron-0.2-Pro/assets/41975091/6ede78d2-f826-43d7-ac16-405932acffeb)  
5. Hold the recovery button, click the reset button while holding recovery button (No need to hold reset button), when the RKDevTool found device, release the recovery button.
   ![image](https://github.com/Psych0h3ad/FYSETC-Voron-0.2-Pro/assets/41975091/6e3dc06d-0e17-4388-9369-1f6fb3cce675)  
6. Wait for the upgrade to complete. Remember not to cut off the power or unplug the data cable during the process, otherwise the upgrade will fail or even damage the CM68.  
   ![image](https://github.com/Psych0h3ad/FYSETC-Voron-0.2-Pro/assets/41975091/e04d7625-4fd1-4907-bf31-b128d4f48915)  

## MCU Firmware

<p style="color: red">
<strong>
Do not perform the following steps unless you are sure you want to reinstall the firmware.
</strong>
</p>

If you know the structure of Klipper, then you should understand that the firmware of the MCU is compiled and installed by the host computer (CM68). This is the way we recommend.

Of course, you can also use other methods to burn the MCU, such as through the "STM32CubeProgrammer" on the computer, or with the help of burning tools such as STlink. These need to be studied by yourself, and our control board also provides corresponding interfaces.

The MCU model we use is STM32F401RCT6, with an external 8Mhz crystal oscillator, and uses PA11/PA12 as USB communication. The following is the MCU configuration and burning process:

1. MCU enters DFU mode:

   - Powered off the whole machine
   - Use a jumper cap to connect 3V3 and B0(boot0)
   ![image](https://github.com/FYSETC/Catalyst_Kit/assets/16657422/43ac39e2-d3b0-4992-9f57-127489c44fe9)
  
   - Power on the whole machine and wait for it to start

2. Use putty or similar SSH tools to connect to CM68 using IP or host name

    ```
    host name: voron-02-pro.local
    Username: linaro
    Password: linaro
    If you are not very familiar with linux, do not use the root user to log in. Misoperation may cause damage to the system.
    Username: root
    Password: root
    ```

3. Configure the firmware:

    - use "lsusb" to ensure the mcu enter dfu mode,

       ```
       lsusb
       ```

    - configure the firmware
    
       ```
       cd ~/klipper
       make clean
       make menuconfig
       ```

4. update the firmware and reboot

    - Compile and burn the firmware:
    
      ```
       make flash FLASH_DEVICE=0483:df11
      ```
    
    - Powered off the whole machine
    - Use a jumper cap to connect B0(boot0) and G(GND)
      ![image](https://github.com/FYSETC/Catalyst_Kit/assets/16657422/9fbd1c61-a14d-4de4-b591-93dc6437292f)

    - Power on the whole machine and wait for it to start

# Print

## Connect via Ethernet

The control board defaults to obtain IP automatically, make sure your router can provide DHCP service normally. You only need to plug in the Internet cable, and when you see the green and yellow lights on, indicates that it is connected to the network.

You have two methods to login the mainsail webpage:

### IP address
you need to go to your router to find the device named voron-02-pro, and write down the IP address
### Host name
The kit has already installed the required plug-ins, and you can access the mainsail page through the pre-set host name: voron-02-pro.local

## Connect via WiFi

- First connect the machine to your LAN via Ethernet, make sure you can log in to CM68 via SSH.
- Plug the included USB wifi into any USB interface on CATALYST board
- Use the following command checks whether the wifi module is recognized:
```
sudo ifconfig
```
- Use the following command to connect to wifi
```
sudo wifi_sta_start.sh ssid password
```
- Use the following command checks whether the wifi module is connected to your router, and get the ip address:
```
sudo ifconfig
```

# FAQ

## 1. Can't find mcu/unable to connect to mcu
Reason:
       It may be that the status of boot0 is uncertain, causing the STM32 to enter the DFU mode, resulting in the connection error.
Solution:
   - Powered off the whole machine
   - Use a jumper cap to connect B0(boot0) and G(GND)
   - Power on the whole machine and wait for it to start
## 2. Mcu firmware version too low
Reason:
The factory version of the Klipper host is the same as that of the MCU. Maybe you have clicked the update button on the mainsail webpage to update the Klipper host. As a result, the version of the host is newer than the firmware of the MCU.
Solution:
update the mcu firmware: Refer to the Firmware&OS==>MCU Firmware
## 3. Temperature error
Reason:
You may have forgotten to connect the MX3.0 16P cable, or it may not be connected firmly.
Solution:
Make sure the MX3.0 16P cable is connected and secure.
## 4. How to use the accelerometer
Refer to Klipper document: 
https://www.klipper3d.org/Resonance_Compensation.html

## 5. Wifi Connection Issues
If you are having problems with your Catalyst wifi, please fix using the following solution. 

SSH into the Catalyst, and run the following command `sudo nano /etc/network/interfaces`

Once you have run the command, add the following lines 

```
auto wlan0
iface wlan0 inet dhcp
wpa-ssid Your Network Name Here
wpa-psk Your Password Goes Here
```
example if your wifi name is fysetcwifi and password was ItRocks:
```
auto wlan0
iface wlan0 inet dhcp
wpa-ssid fysetcwifi
wpa-psk ItRocks
```


# Support
Voron community: 
https://discord.gg/voron
FYSETC Facebook group: 
https://www.facebook.com/groups/238970713918171
FYSETC Discord:
https://discord.gg/T3XcJPgr 
# Buy Link
https://www.aliexpress.us/item/3256805148633512.html




