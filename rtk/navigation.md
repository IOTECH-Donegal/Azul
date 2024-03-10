---
description: Using 2 x UBLOX ZED F9P for heading and position
---

# Navigation

## Configure the GNSS assembly

1. Configure an Ardusimple heading basic starter kit using the configuration files [here](https://www.ardusimple.com/ardupilot-simplertk2bheading-configuration-external-corrections/).
2. Assemble the units and test with patch antennas. I connected to the BLite in U-Centre and confirmed heading, distance between antennas, etc.

## Configure the Autopilot

1. Confirm by measuring the distance between the two GNSS antenna in final mount position. Mine was 1.3 meters, this must be accurate +/- 20%.

```
GPS_POS1_X = 1.3
```

2. Set the units up as base and rover.

```
GPS_TYPE = 17
GPS_TYPE2 = 18
```

3. Do not use the auto config, or pass RTCM through the Autopilot.

```
GPS_AUTO_CONFIG = 0
GPS_DRV_OPTIONS = 0
```

4. The Autopilot gets yaw from the GNSS.

```
EK3_SRC1_YAW = 2
```

5. Switch off magnetic compasses.

```
COMPASS_USE = 0 
COMPASS_USE2 = 0 
COMPASS_USE3 = 0
```

6. Restart the Autopilot.
7. Check in messages, both UBlox boards should be connecting at 460800.
