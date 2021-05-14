## 1.1. Last news Marlin 2 Bugfix Branch
  Update Marlin-BugFix 20210404
  - New bootscreen ;-)
  - New **Special Menu** to set its Delta and leveling.
  - Update ReadMe.
  - Last fix by Marlin.
  - New release (binaries and source) v1.2.0
  - Support QQSP/Q5 Stock, TMC and UART mode.
  - **All QQSP features on Q5 and SKR**

## 1.2. Validate and Actived parts
### Validate:
  - Firmware for QQS-Pro with A4988/TMC220x_Standalone/TMC220x_UART/TMC2209_UART one-wire.

 With activate parts: ![Capabilities](../../docs/images/Marlin-QQS-Pro_Foxies.png)

  * [PID_EDIT_MENU]
  * [NATIVE LANGUAGE]
  * [PROBE_OFFSET_WIZARD]
  * [DELTA_CALIBRATION_MENU]
  * [AUTO_BED_LEVELING_UBL]
  * [MULTI_BUILD_MESH]
  * [UBL_HILBERT_CURVE]
  * [PREHEAT LEVELING]
  * [POWER_LOSS_RECOVERY]
  * [FILAMENT_RUNOUT_SENSOR]
  * [XY_FREQUENCY_LIMIT]
  * [BABYSTEPPING]
  * [PAUSE_BEFORE_DEPLOY_STOW]
  * [LIN_ADVANCE]
  * [ARC_SUPPORT]
  * [BINARY_FILE_TRANSFER]
  * [UART_MODE_for_TMC/RPI/ESP]

## 1.3. **Hardware for the FLSunQ printers**
  
  * MotherBoards QQS(P): 
    [HiSpeedv1_&_RobinMini](./HISPEED)
    
    With integrated stepper drivers(A4988)=>(**Sxxx-Robin_mini.bin**)

    ![First Version-A4988](../../docs/images/HiSpeed.jpg)
    
    With removable stepper drivers.
    2&3_A4988(Green/Red)=>(**Sxxx-Robin_mini.bin**)
    
    ![Second Version-A4988](../../docs/images/HiSpeedv1-A4988.jpg) ![Seconds Version-A4988](../../docs/images/HiSpeedv1-A4988red.jpg)
    
    4xTMC2208 MKS =>(**8xxx-Robin_mini.bin**)
    
    ![Last Version-TMC2208](../../docs/images/HiSpeedv1-TMC.jpg)
  
  * Others Micro Steppinp Drivers
  
    ![Drivers](../../docs/images/MicroSteppinpDrivers.jpg)

  * Other MotherBoards for Q5 and QQS:

    [NANOv1.2](./Q5)=>(**Q5_Header_robin_nano.bin**)

    ![Board_Nanov1.2](../../docs/images/Fam_Nano.png)
    
    [SKR](./SKR)=>(**Header-firmware.bin**)
    
    ![Board_SKRs](../../docs/images/Fam_SKR.png) 
    ![Cnx_SKRs](../../docs/images/SKR_EndStop.png)

  Typically the probe for the QQS-Pro printers.
  
  * Z Probe Offset (-16.2mm)        * TFT screen color Marlin

    ![Version Probe](../../docs/images/VersionProbe.jpg)        ![TFT_COLOR_UI](../../docs/images/UI_Color.png)
  

###  Optionals:

  * Modules Wifi
  
    ![ESP12](../../docs/images/esp12.jpg)
    ![ESP8266](../../docs/images/WemosD1.jpg)

  * Led Strip with additional converter 24v/12-5v
  
    ![Neopixels](../../docs/images/LedsStip.jpg)

  No validate:
  -TMC5121
  -TMC2224/5

## 1.4. CAPTION Firmwares

  **Exemple:** 
  8CWBL-Name_Of_Firmware.bin =>  (8)TMC2208 standalone - (C)UI Marlin - (W)Module Wifi - (B)Extruder BMG - (L)LinearAdvance  

  **Note**: After choosing your binary, remove the "8CWBL-" header or rename the file to "Robin_mini.bin" for QQS or "Robin_nano.bin" for Q5,
  place it on your SD card, insert your SD card into the printer and power on your printer.

  **Caption:**

  **/*------Drivers--------*/**
  - (S) A4988 (green/red)
  - (8) TMC2208 Standalone
  - (9) TMC2209 Standalone
  - (U8) 4xTMC2208_UART with no module ESP12.
  - (U9) 4xTMC2209_UART with no module ESP12.
  - (U8+) 3xTMC2208 (XYZ) + Choice for E0 (A4988,TMC220x) 
  - (U9+) 3xTMC2209 (XYZ) + Choice for E0 (A4988,TMC220x)
  - **(UH) 4xTMC2209_UART with one wire (option modules Wifi/Rpi/Neopixel)**

  **/*-------Options UI TFT--------*/**
  - (F) UI STANDARD (Emulation LCD screen on TFT)
  - (C) UI MARLIN (TFT Color screen)
  - (r) UI STANDARD (Marlin Mode on TFT FOR SKR/NANOv2-3)

  **/*------Modules--------*/**
  - (N) NeoPixel (management of led strips)
  - (W) Module ESP8266/ESP12 (infos at the middle of the page)
  - (w) Module ESP8266/ESP12 with ESP3Dv3.0 Firmware.
  - (T) Extruder Titan
  - (B) Extruder BMG
  - (b) Extruder BMG mini
  
  **/*-------Others options in firmware----*/**
  - (A) BED_LEVELING_BILINEAR
  - (U) BED_LEVELING_UBL
  - (P) PreHeat bed before leveling
  - (R) ARC_SUPPORT
  - (L) Linear Advance (Possible Bug with BabyStep and TMC2208)
  
  **/*-------Others options for advanced users who build their firmware----*/**
  - HOST_ACTION_COMMANDS (Action Command Prompt support Message on OctoPrint) 
  - (M) MEATPACK (Improve dialogue/communication with OctoPrint)
  - BINARY_FILE_TRANSFER
  - TEMP_SENSOR_0 (After changed the thermitor nozzle)
  - LCD_LANGUAGE (Change to the native language)
  - etc 
  
  **/*-------Others Firmwares for Q5 nanov1.2 or QQS with SKR family or Mks_Nano Family----*/**
  - (Q5_8+SCTPULR-Robin_nano)   Q5 Stock(3xTMC2208+1xA4988) with TITAN extruder. 
  - (Q5_9CBPULR-Robin_nano)     Q5 with 4xTMC2209 with BMG extruder.
  - (QQS)U9rTPULR16-SKR14_firmware QQS with SKRv1.4 Board with emulation LCD (Marlin Mode)
***