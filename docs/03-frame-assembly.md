# 🏗️ Frame Assembly

The frame selected was the Tarot 650 sport. The primary reasons were the size and weight and the fact that the top plate is actually a power distribution board (which I think is pretty cool). The retractable landing gear is a nice feature that is included but this was not really a major factor in the decision. Maybe I will come to love this if I install a camera onto it...

The frame comes neatly packaged in a Tarot box and is quite easy to put together. The screws are pretty small so my advice (as with pretty much all of this process) would be to set up the area you are working in so that it is difficult to drop and lose them. With that said, there were spares in the box should you lose any.

![frame_box_closed](https://github.com/user-attachments/assets/cd70d033-0c08-4bcf-9be2-d52523bc90a6)

I will scan and upload the instructions that come in the box as after a quick Google, I cannot immediatley find them online.

I found this helpful video online (see below), which I used in conjunction with the instructions that came in the box. Flicking back and forth between the two seemed to serve me well and it did not take too long to assemble the core components.

[![Watch the video](https://img.youtube.com/vi/4H4Mjw7wpys/0.jpg)](https://www.youtube.com/watch?v=4H4Mjw7wpys)

I think given the veracity of the instructions I have pointed you to (and my lack of taking photos throughout) there is not much need in me writing a comprehensive instruction set for this part of the process.

My only notes would be:

- Be extra careful of overtightening the motor mounts and stripping the holes
- Do not tighten any screws that you will be loosening very shortly to install other components
- The grub screws in the landing gear are particularly fiddly

One thing that I do not recall the video showing is the connection of the power connector to the PDB. This requires you to solder two relativley big solder joints.

![XT60_pigtail_soldered](https://github.com/user-attachments/assets/a47fdcf4-d29d-49ea-ba40-f7f03b8cce74)

As you can see, red goes to the positive (+) and black goes to the negative (-).

> [!TIP]
> You can use the multimeter to check for continutity through your soldered joints. Make contact with one probe to the end of the XT60 connector and the other to the corresponding points on the PDB.

## CubePilot PowerBrick

This may or may not be the correct place for this information but as we currently do not have a power/battery section, this feel the most fitting. With the cube orange+, you get a power brick in the box which sits between the battery and PDB that is designed to tap off the power required to maintain the flight controller and its peripherals (i.e. things connected to the flight controler). There is a cable in the box that connects directly into the bottom of the power brick and goes into the power port on the cube orange+. As I am writing this ater the fact, the cable has already been threaded through the complteted drone but I will add some photos so it is clearer about where it sits in the architecture. This will also be made clear in the [wiring diragramn](wiring_diagram.pdf).

![power_converters](https://github.com/user-attachments/assets/cc5a00aa-4aa1-41a2-bf6e-a1ccd9817071)


Some pictures I did take through the process that I have not used in the above descriptions...

![frame_box_open](https://github.com/user-attachments/assets/3889645b-6901-43d9-97db-806f2b0a3d38)
![frame_box_component_bags2](https://github.com/user-attachments/assets/1ccdccf4-58ba-4fec-a7a4-ef21a4009383)
![frame_top_plate_and_arms](https://github.com/user-attachments/assets/d8479b57-179b-46dc-82ab-5b9a9d62f733)
![drone_on_desk_no_electronics](https://github.com/user-attachments/assets/258a9c49-ec6e-48dc-98de-d168879d30ec)
