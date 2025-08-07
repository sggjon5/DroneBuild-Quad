# 💻 Software Configuration

For this build I am using Ardupilot and mission planner. The setup process is well guided and there is plenty of good documentation online for this. 

The things I would highlight though are:

- You do not need to calibrate the Alpha ESC's from what I can find online
- You need to fix your Flight controller and GPS in place to do the calibrations
- **Do not put the propellors on for any of the testing**
- Check, check and check again that your motors are spinning in the right direction that is expected by the software

## Connecting Mission Planner

To connect mission planner to your drone, we will use the telemetry setup that we have established. Plug the second (i.e. the one not on the drone) telemetry module (with antenna screwed on) into your PC using the USB cable provided in the bundle. Then, power on your drone. Whilst doing this, you can also turn on your transmitter and allow it to automatically connect to the receiver on the drone (as we have set up the binding and registration earlier).

> ![WARNING]
> Do not do this if you have props attached. Remove all props before any power is connected to your drone.

On the successful connection of your telemetry modules (indicated by a solid green and flashing orange light), navigate to the top right corner of mission planner (can be downloaded [here](https://ardupilot.org/planner/docs/mission-planner-installation.html)) and select the first drop down box. There should be a COMX option available. For example, mine is COM6. The Baud rate for my setup is 57600 but it may differ for different arrangements. Click connect in the top right corner.

A "Getting Params" pop up box will then appear and begin to load as it connects to your drone via the telemetry link we have established.
