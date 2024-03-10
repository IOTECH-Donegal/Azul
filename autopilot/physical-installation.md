# Physical Installation

1. Place the Cube on its carrier board. Ensure the Cube has an SDCard installed, mine came with a 16GB card preinstalled.
2. Install Mission Planner (MP) on a new Windows 10 VM, I am using VMWare Workstation, it works fine.
3. Plug the USB cable into the host laptop.
4. In VMWare, link the device to the VM.
5. Update firmware with ROVER latest version. If you need to do a fresh wipe, upload PLANE and then reupload ROVER.
6. Take a copy of the config as DATE TIME, e.g. 22JUN22 1215
7. Go to SETUP->MANDATORY HARDWARE->ACCELEROMETER CALIBRATION and calibrate.
8. Take a copy of the config as After Calibration.
9. Disable GPS\_AUTO\_CONFIG, otherwise the Autopilot will overwrite the GPS configurations.

```
GPS_AUTO_CONFIG = 0
```

10. Connect GPS1, reboot and make sure it shows on the HUD. Set the GPS type.

```
   GPS_TYPE = 1
```

11. Set GPS2 type and connect, reboot and make sure it shows on the HUD.

```
  GPS_TYPE2 = 1
```

12. This is a ROVER, set the FRAME\_CLASS to make it a boat.

```
   FRAME_CLASS = 2
```

This verifies physical connectivity and the ability to navigate.
