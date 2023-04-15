# ELRS-433
Pioneering an end-end ELRS 433 setup as of early 2023. Here you will find STLs to print a case for the TX and RX. The TX case allows for mounting to a standard JR bay and the RX case allows for easy mounting to any flat surface.

# INITIAL SETUP
First you need to "setup the toolchain" which means install a bunch of cool stuff and download the ELRS source code to your computer so you can compile it and flash the modules. Instructions here: https://www.expresslrs.org/software/toolchain-install/

Change the values in user_defines

# FLASHING
In the PlatformIO menu (left side of VS code) click on the "Unified_ESP32_900_TX_via_UART", then wait a few seconds as it loads, then click "Upload" with the module plugged in. Do the same for the RX ("Unified_ESP32_900_TX_via_UART")
![image](https://user-images.githubusercontent.com/1324144/231937139-5e73e033-5cf1-488c-b9d1-206ac9429ce8.png)


# PRINTING
Print tx1/2/3 and glue 2 -> 3. User threaded inserts (m3) to screw on 1 -> 2 with the TTGO screwed to 2.
Print rx1/2 and use threaded inserts + m3 bolts to secure.
