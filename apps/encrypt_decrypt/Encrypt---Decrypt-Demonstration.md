# Introduction
Demonstration of the encrypt/decrypt functionality of the crypto module.
# Description
This demonstration exercises several cryptographic functions, including MD5, TDES, DES, AES, RSA, ECC, and Random
Number Generation, to verify that the software or hardware is performing correctly.

# Building the Application
To build this project, the project corresponding to the functionality desired must be opened in MPLAB X IDE or the IAR IDE. The following tables list and describe the project and supported configurations. The parent folder for these files is crypto/apps/encrypt_decrypt/firmware.

## MPLAB X IDE Projects
This table lists the name and location of the MPLAB X IDE project folder for the demonstration.

| Project Name | BSP Used | Description |
| --- | --- | ---|
| sam_e70_xplained_ultra.X | sam_e70_xplained_ultra | Encrypt/Decrypt project using the SAME70 and hardware accelerated cryptography|
| sam_e70_xplained_ultra_rtos.X | sam_e70_xplained_ultra | Encrypt/Decrypt project using the SAME70 and hardware accelerated cryptography. The software has been enabled to use freeRTOS.|
| sam_e70_xplained_ultra_sw.X | sam_e70_xplained_ultra | Encrypt/Decrypt project using the SAME70 and software cryptography|
| sam_e54_xplained_pro_sw.X | sam_e54_xplained_pro | Encrypt/Decrypt project using the SAME54 and software cryptography|
| sam_e54_xplained_pro.X | sam_e54_xplained_pro | Encrypt/Decrypt project using the SAME54 and hardware cryptography|
| sam_e54_xplained_pro_rtos.X | sam_e54_xplained_pro | Encrypt/Decrypt project using the SAME54 and hardware cryptography. The software has been enabled to use freeRTOS.|
| pic32mz_ef_sk_sw.X | pic32mz_ef_sk | Encrypt/Decrypt project using the PIC32MZ-EF and software cryptography|
| pic32mz_ef_sk.X | pic32mz_ef_sk | Encrypt/Decrypt project using the PIC32MZ-EF and hardware cryptography|
| pic32mz_ef_sk_rtos.X | pic32mz_ef_sk | Encrypt/Decrypt project using the PIC32MZ-EF and hardware cryptography. The software has been enabled to use freeRTOS.|
| pic32mz_w1_curiosity_sw.X | pic32mz_w1_curiosity | Encrypt/Decrypt project using the PIC32MZ-W1 and software cryptography|
| pic32mz_w1_curiosity.X | pic32mz_w1_curiosity | Encrypt/Decrypt project using the PIC32MZ-W1 and hardware cryptography|
| pic32mz_w1_curiosity_rtos.X | pic32mz_w1_curiosity | Encrypt/Decrypt project using the PIC32MZ-W1 and hardware cryptography. The software has been enabled to use freeRTOS.|
| sam_l21_xpro_sw.X | sam_l21_xpro | Encrypt/Decrypt project using the SAML21 and software cryptography|
| sam_l21_xpro.X | sam_l21_xpro | Encrypt/Decrypt project using the SAML21 and hardware cryptography|
| sam_l21_xpro_rtos.X | sam_l21_xpro | Encrypt/Decrypt project using the SAML21 and software cryptography.  The software has been enabled to use freeRTOS.|
| sam_l11_xplained_pro_sw.X | sam_l11_xplained_pro | Encrypt/Decrypt project using the SAML11 and software cryptography|
| sam_l11_xplained_pro_hw.X | sam_l11_xplained_pro | Encrypt/Decrypt project using the SAML11 and Hardware cryptography|

The application is built by using the standard MPLAB X IDE buttons.

## IAR IDE Projects
| Project Name | BSP Used | Description |
| --- | --- | ---|
| sam_a5d2_xplained_ultra_sw.IAR | SAM A5D2 Xplained Ultra | Encrypt/Decrypt project using the SAMA5D2 and software cryptography |
| sam_a5d2_xplained_ultra.IAR | SAM A5D2 Xplained Ultra | Encrypt/Decrypt project using the SAMA5D2 and hardware cryptography |
| sam_a5d2_xplained_ultra_rtos.IAR | SAM A5D2 Xplained Ultra | Encrypt/Decrypt project using the SAMA5D2 and software cryptography. The software has been enabled to use freeRTOS. |
| sam_9x60_ek_sw.IAR | SAM 9x60 EK | Encrypt/Decrypt project using the SAM9X60 and software cryptography |
| sam_9x60_ek.IAR | SAM 9x60 EK | Encrypt/Decrypt project using the SAM9X60 and hardware cryptography |
| sam_9x6_ek_rtos.IAR | SAM 9x60 EK | Encrypt/Decrypt project using the SAM9X60 and software cryptography. The software has been enabled to use freeRTOS. |
| sam_e70_xplained_ultra_sw.IAR | SAM E70 Xplained Ultra | Encrypt/Decrypt project using the SAME70 and software cryptography|
| sam_e70_xplained_ultra.IAR | SAM E70 Xplained Ultra | Encrypt/Decrypt project using the SAME70 and hardware cryptography|

1. Once the project is loaded, click on Project in the Main Toolbar.
2. Click on Make under the Project menu to build the demo. 

# Configuring the Hardware
Refer to the following pages to configure the hardware:
* [SAM E70 Xplained Ultra](https://github.com/Microchip-MPLAB-Harmony/crypto/wiki/Configuring-the-SAM-E70-Xplained-Ultra-Board)
* [SAM E54 Xplained Pro](https://github.com/Microchip-MPLAB-Harmony/crypto/wiki/Configuring-the-SAM-E54-Xplained-Pro-Board)
* [SAM A5D2 Xplained Ultra](https://github.com/Microchip-MPLAB-Harmony/crypto/wiki/Configuring-the-SAM-A5D2-Xplained-Ultra-Board)
* [PIC32MZ EF Starter Kit](https://github.com/Microchip-MPLAB-Harmony/crypto/wiki/Configuring-the-PIC32MZ-EF-Starter-Kit)
* [SAM L21 Xplained Pro](https://github.com/Microchip-MPLAB-Harmony/crypto/wiki/Configuring-the-SAM-L21-Xplained-Pro-Board)
* [SAM 9x60 EK](https://github.com/Microchip-MPLAB-Harmony/crypto/wiki/Configuring-the-SAM-9X60-EK-Board)



# Running the Demostration
1. First connect the board to the PC as described in the 'Configuring the Hardware' section.
2. Configure a terminal application (ex. Tera Term) to access the newly attached serial port. The parameters to use:
	* 115,200 bps
	* 8 data bits
	* no parity
	* 1 stop bit
	* no flow control
3. Compile the demostration
	* For MPLAB X
		1. Use the standard MPLAB X IDE Buttons
	* For IAR
		1. Once the build is completed, in an explorer window, go to ...\crypto\apps\encrypt_decrypt\firmware\sam_a5d2_xplained_ultra_sw.IAR\Debug\Exe
		2. Copy the harmony.bin file onto an SD card
		3. Copy the boot.bin file onto the SD card from [here](https://github.com/Microchip-MPLAB-Harmony/at91bootstrap/blob/master/boot.bin)
		4. Insert the SD card into the card connector on the SAMA5D2 board.
		5. Press the reset button on the board
4. Observe the output from the serial console. An example is shown in the following figure.  Each project will have different timing results.

![Results](../docs/images/EncryptDecryptResults.png)


