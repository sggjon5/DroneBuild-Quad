# 📻 🎮  Receiver and Transmitter 

- **Receiver** - FrSky ARCHER PLUS RS
- **Transmitter** - FrSky Tandem X18

I will provide info about the receiver, then transmitter, and then the binding process.

## 📻 Receiver
The receiver used for this build is the FrSky Archer Plus RS 2.4 GHz. This is an incredibly small and lightweight reciever weighing just over a gram. The datasheets spec it to be able to operate at >2km in good conditions and I found the whole registering and binding process very straight forward. [The datasheet](https://www.frsky-rc.com/wp-content/uploads/Downloads/Amanual/ARCHER%20PLUS%20RS%20RS%20Mini%20Manual.pdf) explains how to set up this receiever in a set of relativley short and easy steps.

The 'work' you have to do to get it ready for use is three solder joints. I used a servo cable (22 AWG) and soldered directly to the plated through holes on the board.

> [!TIP]
> Change your soldering iron tip from the gigantic one you probably used to do the ESC/PDB/Power, to a fine point one, these connections are very small.

The three connections you have to solder are as follows (colouring as a guideline only, but conforms to convention):

- Black - GND
- Red - VIN
- White - SBUS_OUT

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


I felt a little overwhelmed with setting this up at first but after watching the above, the menus of the ETHOS system are intuitive and pretty easy to navigate. I will add my personal selection of buttons etc below but first I will go through the binding process with the receiver.

With the reciever powered off, turn on the transmitter and follow the instructions to set up a model - it should match the configuration that you are building, in this case, a quadcopter (I think it says "multi" on the ETHOS system).

It will then suggest some channels, typically a set-up would have

- **CH1** - Roll
- **CH2** - Pitch
- **CH3** - Throttle
- **CH4** - Yaw


