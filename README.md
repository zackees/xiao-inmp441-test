# SongStone

# Guides

https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started

# Install

  * Install VSCode
    * with the platform io plugin
  * `git clone https://github.com/zackees/xiao-inmp441-test`
  * Use VSCode to open `xiao-inmp441-test`

# Programming a board

  * Connect to XIAO board with USBC cable.
    * Make sure the cable is designed for data
    * Click build/upload in the platform io toolpanel
      * (show picture)
  * The test software should now be installed and the board should be running a test program

# Test routine

  Prior to test please SOLDER ON AN LED to EXTERNAL LED on board. Add a 120 ohm resistor in series with the LED.


https://github.com/zackees/xiao-inmp441-test/assets/6856673/368250d2-1b81-4c72-8af0-213dab47555c



  * Software Test
    * Fade on-off blink test (1 second): Led should fade on/off
      * If LED does not come on then FAIL
    * 5 seconds: ambient sound level check
      * Clap your hands
        * if led does not come on THEN FAIL
    * Click button, lights go on always
      * if no LED on then FAIL
    * SUCCESS

Prior to the battery test please solder on a lipo pouch cell >= 150 mA to the battery connections on the board.

  * Battery Test
    * Plug in power USBC
      * If no RED CHARGE LIGHT then FAIL
    * Unplug power USBC
      * If device turns off then FAIL
    * Desolder battery
    * If not failure then SUCCESS

# Owner's design:

![image](https://github.com/zackees/xiao-inmp441-test/assets/6856673/7017fa5a-ff1d-4d03-8c54-105cfbb52e59)


# XIAO Pins

  * Datasheet
    * https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf

  * I2S
    * According to the datasheet, any pin can be used for I2S
    * Pins (All pins as marked on the board) MIC -> XIAO:
      * WS -> D1
      * L/R -> VDD
      * SD -> D0
      * SCK -> D2
      * VDD -> VDD
      * GND -> D3


# Pinouts

  * XIAO:
    * ![image](https://github.com/zackees/noodz-soundreactive/assets/6856673/b1114268-d4b9-4eeb-9ecf-c81d819812d9)
  * Generic ESP32-C3
    * ![image](https://github.com/zackees/noodz-soundreactive/assets/6856673/4beef3b1-20db-4457-be57-3be4b7ca0fc7)
