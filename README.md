# ELRS-433
Pioneering an end-end ELRS 433 setup as of early 2023. Here you will find STLs to print a case for the TX and RX. The TX case allows for mounting to a standard JR bay and the RX case allows for easy mounting to any flat surface.

![image](https://user-images.githubusercontent.com/1324144/235009558-79952516-3b14-47f2-b9f9-011f956f0802.png)
![image](https://user-images.githubusercontent.com/1324144/235009440-e0f3cc6b-6ad9-4de3-b4aa-b2fab7c1f22f.png)
![image](https://user-images.githubusercontent.com/1324144/235009537-a800d56e-89f2-4df9-a196-2cfdcba78d30.png)


# INITIAL SETUP
First you need to "setup the toolchain" which means install VSCode + PlatformIO extension and download the ELRS source code to your computer (by cloning the repo) so you can compile it and flash the modules. Instructions here: https://www.expresslrs.org/software/toolchain-install/

Change the values in user_defines

# FLASHING
In the PlatformIO menu (left side of VS code) click on the "Unified_ESP32_900_TX_via_UART", then wait a few seconds as it loads, then click "Upload" with the module plugged in. Do the same for the RX ("Unified_ESP32_900_TX_via_UART")

![image](https://user-images.githubusercontent.com/1324144/231937139-5e73e033-5cf1-488c-b9d1-206ac9429ce8.png)

As you flash the TX, you will get a prompt like this. Please choose 4.

![image](https://user-images.githubusercontent.com/1324144/235009215-3ea17c77-f1fc-4ed1-8400-7234bbca62b6.png)


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
