# 💻 Software Configuration

For this build I am using Ardupilot and mission planner. The setup process is well guided and there is plenty of good documentation online for this. 

The things I would highlight though are:

- You do not need to calibrate the Alpha ESC's from what I can find online
- You need to fix your Flight controller and GPS in place to do the calibrations
- **Do not put the propellors on for any of the testing**
- Check, check and check again that your motors are spinning in the right direction that is expected by the software

## 🗺️ Connecting Mission Planner

To connect mission planner to your drone, we will use the telemetry setup that we have established. Plug the second (i.e. the one not on the drone) telemetry module (with antenna screwed on) into your PC using the USB cable provided in the bundle. Then, power on your drone. Whilst doing this, you can also turn on your transmitter and allow it to automatically connect to the receiver on the drone (as we have set up the binding and registration earlier) using the model that was setup previously.

> ![WARNING]
> Do not do this if you have props attached. Remove all props before any power is connected to your drone.

On the successful connection of your telemetry modules (indicated by a solid green and flashing orange light), navigate to the top right corner of mission planner (can be downloaded [here](https://ardupilot.org/planner/docs/mission-planner-installation.html)) and select the first drop down box. There should be a COMX option available. For example, mine is COM6. The Baud rate for my setup is 57600 but it may differ for different arrangements. Click connect in the top right corner.

A "Getting Params" pop up box will then appear and begin to load as it connects to your drone via the telemetry link we have established - this may take a moment.

---

## Mission Planner Setup

The main steps you want to take are under the setup cog on the top navigation bar. Working your way through the side panel on this tab is a good starting point. The documentation and community surrounding ardupilot and mission planner is very strong and usually any errors can be resolved by googling them and navigating to one of the easy to find forums. Most of the errors you will encounter have likely been seen before.

The other things to remember here are:

- The setup of the GPS through the CAN port, if you skipped this step earlier, now is the time to do it
- The above GPS setup includes the disabling of the safety parameter, as there is no safety switch installed onto this aircraft (yet!)
- On Initial tune parameters, the screw siize relates to the size of the prop in inches, in this case it is 15. The battery cell count is 6 and it is a LiPo Battery. You will need to change these according to your setup.
- I found on a blog reply that under ESC calibration (or via the full parameters list) the PWM min for these ESCs should be set to 1100, and the PWM max should be set to 1940. You also (according to the same blog) do not need to calibrate the Alpha series of ESCs.

---

## ✈️ Flight Modes

Under the flight modes tab you will see 6 flight modes available. The way to check which of the flight modes are mapped to your CH5 3-position switch (that we setup in the transmitter mixes), is to simply change the position of that switch (in this case SC) and see the highlighted flight mode change. The three modes I have selected are stabilize (SC up), Alt Hold (SC centre) and Return to Land (RTL) (SC Down).

<img width="604" height="254" alt="image" src="https://github.com/user-attachments/assets/a9b7b5ae-dee4-4c1c-afa0-d335169ec03a" />
<img width="611" height="267" alt="image" src="https://github.com/user-attachments/assets/15af1f9b-7a58-40e6-bf9b-cb963e529731" />
<img width="618" height="261" alt="image" src="https://github.com/user-attachments/assets/d3bf0836-ca12-42c5-b76c-e1cf4f850799" />

