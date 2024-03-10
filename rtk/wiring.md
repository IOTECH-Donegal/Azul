# Wiring

## Sparkfun boards

The Mission Planner menus do mention UBX ZED-9P but do not mention the ZED-9R. The ZED-9R was not treated as a compass, leaving the device without a working yaw sensor.

An option using OpenINS is also to be tested ++later.

The cables which come out-of-the-box with the cube are JST-GH type, 4 and 6 pin for the GNSS. Unfortunately, the Sparkfun boards only have a QWIK connector output, and I have not found a conversion cable. For the moment, I have not tested any cable-kludging.

## Ardusimple boards

These have a JST-GH connector, the mating aerial connector is JST GHR-06V.

1. 5V\_IN
2. ZED-F9P UART1 RX (3.3V level)
3. ZED-F9P UART1 TX (3.3V level)
4. Not connected
5. Not connected
6. GND

## Mini Carrier board

These have JST-GH connectors

The matching GPS1 connector is:

1. 5V\_IN
2. SERIAL 3 RX
3. SERIAL 3 TX
4. I2C SCL
5. I2C SDA
6. BUTTON
7. SAFETY LED
8. GND

The matching GPS2 connector is:

1. 5V\_IN
2. SERIAL 4 TX
3. SERIAL 4 RX
4. I2C SCL
5. I2C SDA
6. GND

Unfortunately, the Ardusimple side does not match any of the cables supplied in the mini carrier kit. A cable from 3DXR (JST-GH 6pin to 6pin 25cm, Code: HB-25CM-JST-GH-6to6) is suitable. This worked out of the box as GPS2 and also powered the Ardusimple board.
