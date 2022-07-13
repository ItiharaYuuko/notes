# ESP8266 TCP Server Function

## Decelered the command for TCP information functions, and ESP8266 modules behavior
</br>
1. "STD" means shutdown tcp connection.</br>
2. "SETTINGSCLEAR" format flash storage space.</br>
3. "SETUP+\<SSID\>#\<PASSWD\>" to configure next times connection after reboot.</br>
4. "REBOOT" restart esp8266 module to load flash config files for wifi connecting.</br>
5. "RELAYON" set the GPIO16 voltage HIGH, and return GPIO16HIGH message to client.</br>
6. "RELAYOFF" set the GPIO16 voltage LOW, and return GPIO16LOW message to client.</br>