# 📻 🎮  Receiver and Transmitter 

- **Receiver** - FrSky ARCHER PLUS RS
- **Transmitter** - FrSky Tandem X18

I will provide info about the receiver, then transmitter, then the binding process and finally my configuration of mixes.

## 📻 Receiver
The receiver used for this build is the FrSky Archer Plus RS 2.4 GHz. This is an incredibly small and lightweight reciever weighing just over a gram. The datasheets spec it to be able to operate at >2km in good conditions and I found the whole registering and binding process very straight forward. [The datasheet](https://www.frsky-rc.com/wp-content/uploads/Downloads/Amanual/ARCHER%20PLUS%20RS%20RS%20Mini%20Manual.pdf) explains how to set up this receiever in a set of relativley short and easy steps.

The 'work' you have to do to get it ready for use is three solder joints. I used a servo cable (22 AWG) and soldered directly to the plated through holes on the board.

> [!TIP]
> Change your soldering iron tip from the gigantic one you probably used to do the ESC/PDB/Power, to a fine point one, these connections are very small.

The three connections you have to solder are as follows (colouring as a guideline only, but conforms to convention):

- Black - GND
- Red - VIN
- White - SBUS_OUT

  <img width="475" height="381" alt="archer_plus_rs_pinout" src="https://github.com/user-attachments/assets/99b246d7-5661-4257-b2c6-c5ec59e69a10" />

 These three cables then go into a Servo connector and is connected to the "RC IN" pins on the flight controller (along the bottom edge of the orange+), with black corresponding to - and white corresponding to s.

![reciever_soldered](https://github.com/user-attachments/assets/fd48d23a-7e68-48d3-b165-bca9f1a40a55)

> [!WARNING]
> **Do not stick this receiver to the frame using foam tape attached to the side with the button**. I did this and it literally pulled the button off so I had to spend 10 minutes reconstructing it with a pair of very fine tweezers to be able to bind the transmitter.

As can be seen in the above photo, the button is not actually attached anymore, this is because it was stuck to the foam tape I had used to mount it to the frame. I attached it to the top of the bottom plate when affixing it to the frame, on the back right hand side, with the antennas hanging out the side of the central body of the drone. As you can also (just about) see in the below image, the servo connector that is attached to the three cables that were soldered to the receiver, are connected to the RC IN port on the cube (furthest left rail on the bottom of the flight controller).

![receiver_onboard](https://github.com/user-attachments/assets/065384a2-1af9-4703-9a6b-8b6338f07f67)






## 🎮 Transmitter

The transmitter used for this project was the FrSky Tandem X18 Dual Band transmitter. 

![x18_transmitter](https://github.com/user-attachments/assets/04077540-5ebc-422b-8f45-79d357f510f8)

![x18_transmitter_case](https://github.com/user-attachments/assets/f2b5dc64-3e4e-4742-a701-c562b071ca1f)


There is again, a great comprehensive video about this series of transmitters that I found useful to watch most of. I can corroborate what is said there that it does have a real quality feling to it, even if mine is the cheapest version available.

[![Watch the video](https://img.youtube.com/vi/sJ-LwGSo7k8/0.jpg)](https://www.youtube.com/watch?v=sJ-LwGSo7k8)

### Registration and binding process
I felt a little overwhelmed with setting this up at first but after watching the above, the menus of the ETHOS system are intuitive and pretty easy to navigate. I will add my personal selection of buttons etc below but first I will go through the binding process with the receiver.

With the reciever powered off, turn on the transmitter and follow the instructions to set up a model - it should match the configuration that you are building, in this case, a quadcopter (I think it says "multi" on the ETHOS system).

It will then suggest some channels, typically a set-up would have

- **CH1** - Roll
- **CH2** - Pitch
- **CH3** - Throttle
- **CH4** - Yaw

Once you have made this model, it should become the active model. Using the nav bar at the bottom of the screen, click on the second from the left (the plane icon) and navigate to RF system.

You then want to expand the internal module drop down and turn it on.

You should then select the protocol to be the one that matches with your receiver, in this case ACCESS.

You then need to turn on either 2.4GHz or 900M depending on what frequency your receiever operates on. As spoken through in the video, this transmitter can do both. In this case, I have turned on the 2.4GHz and left 900M turned off.

Select the Register button on the transmitter and head back over to your drone/receiver.

> [!NOTE]
> You should check your electronics for shorts before going all out with the battery for the next step. In this case, I actually used the bench power supply with 22.2V and a lower ampage (3.0A?) to safeguard against frying anything done incorrectly. I would advise to do this before plugging in a battery straight away. Check for shorts using the multi-meter etc. The battery I have came with an XT90 connector, and the pigtail I soldered onto the board was female (whereas male would have been better). Due to this, I have a succession of converters (including the powerbrick that comes with the flight controller.

Hold the button down on the reciever (you should feel it click when pressed) and plug the battery (or bench power advised) in to power on the system. The lights on the receiver should be green and red, indicating (as per the data sheet) that it is in "reg" mode.

On the screen of your transmitter, you should then see it change and the register button at the bottom of the screen should be able to be selected - click it to register the device.

After you have had a registration successful/ok message, power down the drone so the receiever is powered off.

Then, on the transmitter, click one of the three options on the same line as the regiser button (mine was RX1, RX2 and RX3) but I have seen slighly different layouts of menu's on some youtube videos.

Power the drone/receiever back on

You may have to select it on the screen of the transmitter again, but it is intutive to do and you should then recieve a bind successful message. The light on the receiver should be green and you should see the name of it (or some truncated form) in the box on the menu of the transmitter.

The above is basically a poorly worded version of the advice on the manual provided by FrSky (see the datasheet linked previously, or the image below).

<img width="1171" height="501" alt="image" src="https://github.com/user-attachments/assets/edd27356-092a-4244-aea2-a7d27dd7c508" />

### My Setup

This is the part I feel the most uncertain about in the entire process to be honest. I could not really find a "this is how you configure your transmitter" advice easily online, so I am going off the assumption that there are some standards but it is otherwise personal preference what the different switches etc are assigned. In anycase, here is my current mixes configuration for this quad copter setup.

| Name | Channels | Source | Notes |
|------|----------|---------|-------|
|  Roll | CH1 | Aileron  | Default setting, what is recognised by default in Ardupilot |
| Pitch | CH2 | Elevator | " |
| Yaw | CH4 | Rudder | " |
| Throttle | CH3 | Throttle | ". Added throttle cut setting assgined to SG (3 position switch converted to a 2 position switch in hardware settings) |
| Flight Modes | CH5 | SC | Free mix - Kept as 3 position switch, will likely assign to stabilized, ATTI and RTH?. |
| RTH | CH7 | SF | Free mix - 2 position switch |
| Arm | CH8 | SD | Free mix - changed 3 pos switch to a 2 pos switch in hardware settings. Set so drone can be armed remotely |

To change the setup of a particular switch (i.e. name, whether it is 2pos, 3pos etc), you can navigate to the settings cog along the bottom nav bar of ETHOS on the transmitter. Here you will find hardware settings > switches settings. Within this drop-down you can change the features of the switches and see what is available to you. If you are permanently renaming things, I would reccomend keeping the assigned letters in the name somwehere as it is then easy to rember which one you have assigned as arm, or kill_motors etc.

There are some things to be configured within the software setup to make some of this work but we will go through that in the next section.




