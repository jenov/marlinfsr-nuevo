 # For the Wifi Module ESP8266 or Mks Wifi:

![UI ESP3D with Module Wifi MKS](../../../docs/images/QQSPro_ESP3D.png)![UI ESP3D2](../../../docs/images/ESP_UI2.png)

Put the firmware (MksWifi.bin) on the scard with the firmware FLSUN (Robin_mini.bin)
 - 1) Flash original firmware + original mkswifi 
 - 2) Flash original firmware + Custum mkswifi 
 - 3) Inspect the Wifi Access Point and if you see: AP-FLSUN => Flash ok 
 - 4) Flash Marlin 
 - 5) After that, you can connect to the hotspot AP-FLSUN with password "makerbase"

to run the update of Mks_Wifi or You also can do by web page of the AP (192.168.4.1).

 ### Initial Configuration after the flash.

1. Open device web page on the AP connected device (ap:AP-FLSUN/pwd:makerbase)
2. Accept Captive portal redirect or Open a web browser and navigate to http://192.168.4.1
3. Upload 4 files in the directory "FilesToUpload' and configure the device to your choosing.
4. I recommend changing to Station mode and connecting to your home/office Wifi instead of staying in AP mode
5. You may want to change the Baud rate to accord with your printer.
6. You can change to DHCP, or at the very least setup a Static IP you are familiar with.

![UI ESP3D](../../../docs/images/ESP-UI.png)

Once reconnected to the module's web page, you can update it through the interface with:
- New files "index.html.gz", "preferences.json" or "macros"
- A new ESP firmware "MksWifi.bin or" ESP_firmware.bin "

Enjoy....🙃

More information: [ESP3Dv2.1](https://github.com/luc-github/ESP3D/wiki/Install-Instructions)
