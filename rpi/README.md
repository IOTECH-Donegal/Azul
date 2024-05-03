# RPi

## MavProxy

Some work requires MavProxy

```
sudo apt-get install python3-dev python3-opencv python3-wxgtk4.0 python3-pip python3-matplotlib python3-lxml python3-pygame
pip3 install PyYAML mavproxy --user
 echo 'export PATH="$PATH:$HOME/.local/bin"' >> ~/.bashrc
```

To listen to a link, type

```
mavproxy.py --master=/dev/serial
```

To test simple Python, use the following script (link.sh)

```
#!/usr/bin/env python3

# Get the mavutil library
from pymavlink import mavutil

# Start a connection listening on a UDP port
connection = mavutil.mavlink_connection('/dev/serial0' , baud=57600)

# Wait for the first heartbeat
#   This sets the system and component ID of remote system for the link
connection.wait_heartbeat()
print("Heartbeat from system (system %u component %u)" % (connection.target_system, connection.target_component))
```

Add the following code to read a single parameter.

```
while True:
    msg = connection.recv_match(type='ATTITUDE', blocking=True)
    print(msg)
```

Add the following code to send an ARM command and get the ACK

```
# Arm the system
connection.mav.command_long_send(cts, ctc, mavutil.mavlink.MAV_CMD_COMPONENT_ARM_DISARM, 0, 1, 0, 0, 0, 0, 0, 0)
msg = connection.recv_match(type='COMMAND_ACK', blocking=True)
print(msg)

```
