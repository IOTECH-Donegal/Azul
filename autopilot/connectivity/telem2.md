# Telem2

A generic JST-GH 6 pin cable was cut at one end and connected to header pins for a Raspberry Pi, generally following [this](https://ardupilot.org/dev/docs/raspberry-pi-via-mavlink.html).

<table><thead><tr><th width="76">Pin</th><th>Name</th><th>Direction</th><th>Voltage</th><th>Color</th><th>Use</th></tr></thead><tbody><tr><td>1</td><td>VCC 5VDC</td><td>IN</td><td>5V</td><td>Red</td><td>Not used</td></tr><tr><td>2</td><td>Serial 2 TX</td><td>OUT</td><td>3.3-5V</td><td>Black - Green</td><td>TX RPi 09</td></tr><tr><td>3</td><td>Serial 2 RX</td><td>IN</td><td>3.3-5V</td><td>Black - Yellow</td><td>RX RPi 07</td></tr><tr><td>4</td><td>CTS</td><td>IN</td><td>3.3</td><td>Black</td><td></td></tr><tr><td>5</td><td>RTS</td><td>OUT</td><td>3.3</td><td>Black</td><td></td></tr><tr><td>6</td><td>GND</td><td></td><td>GND</td><td>Black</td><td>GND RPi 05</td></tr></tbody></table>

The RPi is [azul-sonar](../../rpi/azul-sonar.md), a RPi Zero 2W.
