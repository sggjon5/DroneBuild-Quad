# 📻 Telemetry
The telemetry selected for this build was the RFDesigns 868x-EU radio bundle. 

> [!NOTE]
> You will likely have to buy the cable that goes from the telemetry unit to the telemetry port on the flight controller seperatley.


The setting up of these components was actually very simple. As I had purchased a pair as a bundle, they had already been programmed to have the same settings and find eachother. I did find a brilliant video that spoke all about them and was worth the watch in its entirety to understand. I will link it below.

[![Watch the video](https://img.youtube.com/vi/lN28v68aL_Y/0.jpg)](https://www.youtube.com/watch?v=lN28v68aL_Y)

This video talks you through everything I would type here and is much easier to scrub through and find the parts you need/want. Most notably, the checking that all the parameters are aligned on both your radios and how to actually plug them in and check it is all working.

I will however mention how you actually orientate the connector onto the pins (it is also convered in the video). Your connector will have a little arrow in the top corner above the (most likely) black cable.

![telemetry_cable](https://github.com/user-attachments/assets/7c76d9c1-8b74-414f-a247-03822e803434)

This arrow goes onto the far left, bottom rail of the RFD868x-EU pins (there is likely a plastic blocker stopping you from using the top rail).

![telemetry_nearly_plugged_in](https://github.com/user-attachments/assets/114ac63d-f156-4cf9-99d8-894b9290fd90)

![telemetry_plugged_in](https://github.com/user-attachments/assets/2e7c4964-dbf0-48ac-a7a1-bf0ee9da5cf3)

To state the obvious, one of the telemetry modules goes onto the drone and one goes into your computer (via the USB cable provided in the bundle).

I attached the one on the drone to the underside of the main body, using a piece of 3M foam tape and threaded the cables through the holes in the lower and top plate to plug it into my telem1 port on the cube pilot.

![telem_on_drone](https://github.com/user-attachments/assets/dd0b87a7-73c8-4b77-982b-5bfd5819f13f)

It is reccomended online that you make a seperate power source for the radio but given the fact that the RFD868x-EU operates at 5V and has a "~800mA max peak (at maximum transmit power)", it can quite comfortably be powered by the telem1 port on the cube orange plus as this also operates at 5V and can provide up to 1.5A [link](https://discuss.cubepilot.org/t/serial-port-problems/5654/5).
