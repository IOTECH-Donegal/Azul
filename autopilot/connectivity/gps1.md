# GPS1

The cable which came with the Cube did not have a JST-GH connector. Serial3/UART3 is for GPS1 and direction is from the perspective of the Cube.

| Pin | Name        | Direction | Voltage | Color |
| --- | ----------- | --------- | ------- | ----- |
| 1   | VCC 5VDC    | IN        | 5V      | Red   |
| 2   | Serial 3 RX | IN        | 3.3-5V  | Black |
| 3   | Serial 3 TX | OUT       | 3.3-5V  | Black |
| 4   | I2C SCL     | IN        | 3.3     | Black |
| 5   | I2C SDA     | IN/OUT    | 3.3     | Black |
| 6   | Button      |           | GND     | Black |
| 7   | LED         |           | GND     | Black |
| 8   | GND         |           | GND     | Black |

On the Ardusimple, there is a 6 pin JST-GH connector. I took a generic JST-GH 6 to 6 and cut off one end. I then connected the four wires required using solder & heatshrink. This table is from the perspective of the Ardusimple ZED F9P.

| Pin | Name             | Direction | Voltage |
| --- | ---------------- | --------- | ------- |
| 1   | VCC 5VDC         | IN        | 5V      |
| 2   | ZED-F9P UART1 RX | IN        | 3.3     |
| 3   | ZED-F9P UART1 TX | OUT       | 3.3     |
| 4   | Not connected    |           | GND     |
| 5   | Not connected    |           | GND     |
| 6   | GND              | IN        | GND     |
