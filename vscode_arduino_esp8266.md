<<<<<<< HEAD
# Use VSCode developing esp8266 under Arduino Toolchain

1. Download arduino ide at [arduino software](https://www.arduino.cc/en/software), select windows platform [arduino-*-windows.exe](https://downloads.arduino.cc/arduino-1.8.19-windows.exe)
2. Setting up bord tools 文件-首选项-附加开发板管理地址[esp8266.json](http://arduino.esp8266.com/stable/package_esp8266com_index.json)
3. Setting up bord manager 工具-Arduino avr boards-开发板管理-搜索esp8266-选择ESP8266-安装, if the toolchain download speed so slow, you could able to install packages manual at [esp-quick-toolchain](https://github.com/earlephilhower/esp-quick-toolchain/releases) slect which version you need, below was the example to install toolchain ver 3.0.2 on windows.
    > esp8266-3.0.2.zip</br>
    > i686-w64-mingw32.esptool-f80ae31.210717.zip</br>
    > i686-w64-mingw32.mklittlefs-943d2f7.210717.zip</br>
    > i686-w64-mingw32.mkspiffs-7fefeac.210717.zip</br>
    > i686-w64-mingw32.xtensa-lx106-elf-1757bed.210717.zip</br>
    > python-3.7.2.post1-embed-win32v2.zip</br>
    > python3-3.7.2.post1-embed-win32v2a.zip</br>
4. When you downloaded successful, please move/copy to Arduino IDE packages path: (C:\Users\\<user_name>\\AppData\Local\Arduino15\packages)
5. Download and install vscode installer at download page [VSCode Download](https://code.visualstudio.com/), select your platform below download button.
6. Run vscode press plugin button type arduino in input, and press install to install the adruino plugin.
7. In files explorer, select <c_cpp_properties.json> file and append below content in includePath block.
    ```Json
        "includePath": [
                "D:\\Applications\\Arduino\\tools\\**",
                "D:\\Applications\\Arduino\\hardware\\arduino\\avr\\**",
                "D:\\Documents and Settings\\Documents\\Arduino\\**",
                "C:\\Users\\<user_name>\\AppData\\Local\\Arduino15\\**",
                "C:\\Users\\<user_name>\\AppData\\Local\\Arduino15\\packages\\esp8266\\hardware\\esp8266\\3.0.2\\**",
                "C:\\Users\\<user_name>\\AppData\\Local\\Arduino15\\packages\\esp8266\\tools\\**",
                "${workspaceFolder}/**"
            ],
    ```
8. At statusbar press Arduino Board Configuration at "Select Board" choise the "Generic ESP8266 Module" , when you use ESP-01 or ESP-01s keep the config as default.
9. At statusbar press the path which you opened EXP: "ESP8266\testfirst\test.ino", it will notify you type the path in input. This setting influence the binary file compile.
=======
# Use VSCode developing esp8266 under Arduino Toolchain

1. Download arduino ide at [arduino software](https://www.arduino.cc/en/software), select windows platform [arduino-*-windows.exe](https://downloads.arduino.cc/arduino-1.8.19-windows.exe)
2. Setting up bord tools 文件-首选项-附加开发板管理地址[esp8266.json](http://arduino.esp8266.com/stable/package_esp8266com_index.json)
3. Setting up bord manager 工具-Arduino avr boards-开发板管理-搜索esp8266-选择ESP8266-安装, if the toolchain download speed so slow, you could able to install packages manual at [esp-quick-toolchain](https://github.com/earlephilhower/esp-quick-toolchain/releases) slect which version you need, below was the example to install toolchain ver 3.0.2 on windows.
    > esp8266-3.0.2.zip</br>
    > i686-w64-mingw32.esptool-f80ae31.210717.zip</br>
    > i686-w64-mingw32.mklittlefs-943d2f7.210717.zip</br>
    > i686-w64-mingw32.mkspiffs-7fefeac.210717.zip</br>
    > i686-w64-mingw32.xtensa-lx106-elf-1757bed.210717.zip</br>
    > python-3.7.2.post1-embed-win32v2.zip</br>
    > python3-3.7.2.post1-embed-win32v2a.zip</br>
4. When you downloaded successful, please move/copy to Arduino IDE packages path: (C:\Users\\<user_name>\\AppData\Local\Arduino15\packages)
5. Download and install vscode installer at download page [VSCode Download](https://code.visualstudio.com/), select your platform below download button.
6. Run vscode press plugin button type arduino in input, and press install to install the adruino plugin.
7. In files explorer, select <c_cpp_properties.json> file and append below content in includePath block.
    ```Json
        "includePath": [
                "D:\\Applications\\Arduino\\tools\\**",
                "D:\\Applications\\Arduino\\hardware\\arduino\\avr\\**",
                "D:\\Documents and Settings\\Documents\\Arduino\\**",
                "C:\\Users\\<user_name>\\AppData\\Local\\Arduino15\\**",
                "C:\\Users\\<user_name>\\AppData\\Local\\Arduino15\\packages\\esp8266\\hardware\\esp8266\\3.0.2\\**",
                "C:\\Users\\<user_name>\\AppData\\Local\\Arduino15\\packages\\esp8266\\tools\\**",
                "${workspaceFolder}/**"
            ],
    ```
8. At statusbar press Arduino Board Configuration at "Select Board" choise the "Generic ESP8266 Module" , when you use ESP-01 or ESP-01s keep the config as default.
9. At statusbar press the path which you opened EXP: "ESP8266\testfirst\test.ino", it will notify you type the path in input. This setting influence the binary file compile.
>>>>>>> d13f4ba4c4f8d01dcb9e311d920960610e90bf13
10. Press F1 type "arduino:upload" to compile and upload the firmware into your chip.