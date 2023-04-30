# ELRS-433
Pioneering an end-end ELRS 433 setup as of early 2023. Here you will find STLs to print a case for the TX and RX as well as instructions on how to get it all working. The TX case allows for mounting to a standard JR bay and the RX case allows for easy mounting to any flat surface. It's a 50mw bidirectional link, with an estimated range of many hundreds of km.

![image](https://user-images.githubusercontent.com/1324144/235009558-79952516-3b14-47f2-b9f9-011f956f0802.png)
![image](https://user-images.githubusercontent.com/1324144/235009440-e0f3cc6b-6ad9-4de3-b4aa-b2fab7c1f22f.png)
![image](https://user-images.githubusercontent.com/1324144/235009537-a800d56e-89f2-4df9-a196-2cfdcba78d30.png)

# MATERIALS
- You will need 2 of the LILYGO® TTGO LoRa32 V2.1_1.6 Version 433 boards: https://www.aliexpress.us/item/2251832685763835.html
- PLA or PETG + a 3D printer for the casing
- Dragonlink or other 433mhz antennas (moxon on TX and dipole on RX)

# INITIAL SETUP
First you need to "setup the toolchain" which means install VSCode + PlatformIO extension and download the ELRS source code to your computer (by cloning the repo) so you can compile it and flash the modules. Instructions here: https://www.expresslrs.org/software/toolchain-install/

Change the values in user_defines for bind phrase and locality like below

![image](https://user-images.githubusercontent.com/1324144/235010505-0ef366d9-d8af-443b-ba6a-2cdf8ad0a7cc.png)

# FLASHING
In the PlatformIO menu (left side of VS code) click on the "Unified_ESP32_900_TX_via_UART", then wait a few seconds as it loads, then click "Upload" with the module plugged in. Do the same for the RX ("Unified_ESP32_900_TX_via_UART")

![image](https://user-images.githubusercontent.com/1324144/235013543-5b0bdb49-be01-4555-b2ef-55fc8d8b9250.png)

As you flash the TX, you will get a prompt like this. Please choose 4.

![image](https://user-images.githubusercontent.com/1324144/235009215-3ea17c77-f1fc-4ed1-8400-7234bbca62b6.png)

After flashing please use the latest LUA script on your radio as well. https://www.expresslrs.org/quick-start/transmitters/lua-howto/

# WIRING
The TX board needs a 5v supply, so a BEC will be needed to step down VBat coming out of the JR bay pins. Connect pin 13 of the TTGO to the bottom pin of the JR bay.

![image](https://user-images.githubusercontent.com/1324144/235010749-d7dbcea0-d19f-4793-8351-5112d85d16ec.png)

![image](https://user-images.githubusercontent.com/1324144/235010916-2626b5ed-dd53-4765-8f19-79d09643d214.png)

The RX also needs a 5v supply. Get it from anywhere on the FC such as the servo rail. RX and TX (TX0 and RX0 pads for the CRSF output) on the TTGO must be connected to RX and TX of the FC (RX going to TX and TX going to RX). 

# PRINTING
Print tx1/2/3 and glue 2 -> 3. User threaded inserts (m3) to screw on 1 -> 2 with the TTGO screwed to 2.
Print rx1/2 and use threaded inserts + m3 bolts to secure.

![image](https://user-images.githubusercontent.com/1324144/235009618-a2c45e54-861e-47f1-8bfe-cbe38fe6d290.png)
![image](https://user-images.githubusercontent.com/1324144/235009630-33849ab2-aecf-466a-a638-a8ffd6c59b3b.png)
![image](https://user-images.githubusercontent.com/1324144/235009672-126ab23e-eb7e-4eae-91cd-2ddf52bc0f2b.png)
![image](https://user-images.githubusercontent.com/1324144/235009690-777a73d9-c1b0-4a22-b1ba-680090407bb5.png)


# TESTING
So far, 45km at 10mw was achieved from a takeoff point which was not ideal. There was no LOS towards the end.
![image](https://user-images.githubusercontent.com/1324144/235009741-40a1a1b1-8efb-4ae1-88ae-fcb74584971a.png)
