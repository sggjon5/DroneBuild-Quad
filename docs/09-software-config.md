# 💻 Software Configuration

For this build I am using Ardupilot and mission planner. The setup process is well guided and there is plenty of good documentation online for this. 

The things I would highlight though are:

- You do not need to calibrate the Alpha ESC's from what I can find online
- You need to fix your Flight controller and GPS in place to do the calibrations
- **Do not put the propellors on for any of the testing**
- Check, check and check again that your motors are spinning in the right direction that is expected by the software

## 📶 Connecting Mission Planner

To connect mission planner to your drone, we will use the telemetry setup that we have established. Plug the second (i.e. the one not on the drone) telemetry module (with antenna screwed on) into your PC using the USB cable provided in the bundle. Then, power on your drone. Whilst doing this, you can also turn on your transmitter and allow it to automatically connect to the receiver on the drone (as we have set up the binding and registration earlier) using the model that was setup previously.

>  [!WARNING]
> Do not do this if you have props attached. Remove all props before any power is connected to your drone.

On the successful connection of your telemetry modules (indicated by a solid green and flashing orange light), navigate to the top right corner of mission planner (can be downloaded [here](https://ardupilot.org/planner/docs/mission-planner-installation.html)) and select the first drop down box. There should be a COMX option available. For example, mine is COM6. The Baud rate for my setup is 57600 but it may differ for different arrangements. Click connect in the top right corner.

A "Getting Params" pop up box will then appear and begin to load as it connects to your drone via the telemetry link we have established - this may take a moment.

---

## 🗺️ Mission Planner Setup

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

Once you have completed all of the orientations/calibrations etc you can then get something moving - the motor test!

---

## 🧲 Motor Test

I know I have said it before, but I will say it again just in case.

> [!WARNING]
> Remove all propellors before doing the motor test.

Navigate to the optional hardware dropdown in the sidebar of the setup tab and select motor test. Here you can diligently check that the motors are spinning in the right direction. An easy way to test this is to rip a strip of paper and hold it against the motor as it spins for the 2 seconds at 5% throttle. This gives a clear indication of which way the motor is spinning and you can ensure that it matches the setup shown in the software that is required.

> [!NOTE]
> The stickers that come as a defualt on many frames do not necessarily match the numbering in the mission planner software. Check this carefully to ensure what is happening in the real world is what is expected to happen, governed by the labelling in the software.


If the motors are not spinnning, it could be that the signal cables are not correctly assigned/oriented, it could also be that there is not enough power to spin the motors (if you are still attached to a low amp bench power supply, for example) or it could be that the connection between the ESC and the motor is faulty.

One sign that the connections are correct is that when you power on the drone, you should hear a succession of around 5 beeps, proceeded by one longer beep. This is also dependent on turning off the safety parameter we mentioned in the GPS setup section. The noises made by the ESC can be decoded and often have some meaning. I have not had to go through this but a google of what the beeps mean for your specific ESCs should turn up some results and information to then act on.

 ---
 
## 🦾 Setting a Remote Arm Switch

I know I have said it before, but I will say it again and again just in case.

> [!WARNING]
> Remove all propellors.

Now you have confirmed everything is working as anticipated, we can set the arm switch we assigned to channel 8 on our transmitter to actually mean something to the drone via changing some parameters in mission planner. The video linked below goes through the whole process but I will highlight the key details (I would still reccomend watching the video, it is very short and straight to the point).

- Go to config > full parameter list
- Search for rcX_option, where X is the number of the channel you have assigned to be your arming channel (in this case RC8_OPTION)
- Change the value to 153
- Write the parameter changes back to the flight controller (button on right hand menu)

It is worth noting that you can also do this through the Extended tuning menu by setting the corresponding RC Opt to be ArmDisarm.

[![Watch the video](https://img.youtube.com/vi/wtwehddboB4&t/0.jpg)](https://www.youtube.com/watch?v=wtwehddboB4&t=25s)

---

## 🛸 Fake Flying

Okay, now everything is working as expected, the motors are spinning safely in the correct direction and we have a way to arm the drone for flight.

> [!WARNING]
> Remove all propellors.

We can now pretend to fly the drone and test the responsiveness of the control input and validate that it is making a difference to the actual physical system.

- Ensure the throttle is all the way down, the drone is in stablize mode and the throttle cut is not active
- Arm the drone (flicking SD down in this case)
- The artificial horizon on the data tab of mission planner should change to say ARMED
- The motors will start spinning
- If all sounds good, start to slowly increase the throttle to 50%
- Then, once this has settled, start to move the right stick around and hear the motors change and modulate to what you are doing
- Then, bring the throttle down to idle, disarm the drone and compelte the test

- An alternative is to pick up the drone in stabilise mode and perturb it from its horizontal state, the stabilize mode should react to your actions and you should hear this reflected in the motors movement


[![Watch the video](![drone_portrait_outside](https://github.com/user-attachments/assets/9a051afe-b0c8-467b-bf7a-06b82b5f59e2))](https://www.youtube.com/watch?v=z5--iK6VvRA)




