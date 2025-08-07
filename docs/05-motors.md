# 🧲 Motors

The motors selected for this project were the T-motor MN4014 330KV motors - a member of the navigator series.

![MN414_motor_up_close](https://github.com/user-attachments/assets/82659fea-2a19-43e4-bd82-3c97fe69583a)

According to the manufacturers datasheet, these motors (when paired with the selected propellors) will provide 830g of thrust at 50% throttle, meaning a total thrust of 3320g. 

By making some assumptions[^1] we can ascertain the relationship between % throttle and thrust to be y = 22.517x - 284.79. Which then provides:

- at 40% throttle, 4 x 615g = 2460g
- at 45% throttle, 4 x 728g = 2912g

This provides the confidence that we will be able to hover (where weight=lift) at an appropriate throttle setting (aiming for between 40-50%) to give good control authority (mass of the drone is currently predicted to be 2,839.3g).

The other consideration with motors (beyond their physical size and if they will fit) is the voltage that they operate at. This information can be obtained from their data sheet and can be deciphered with the knowledge that there is nominally 3.7V per cell. So if the motor claims an operating voltage of 22.2V, this means it is suited to a 6S battery (as 6 * 3.7V = 22.2V). As a realted note, LiPo batteries are considered to be fully charged at 4.2V and fully discharged at 3.0V. It is common practive to stop flying between 3.4-3.5V to preserve the battery and store the batteries at a balanced 3.8V per cell.

The numbers within a motors name typically conform to the convention of stator diameter by stator height - so in this case, these motors are 40mm i diameter and 14mm in height, forming the 4014.
)
The KV rating is an indicator of speed potential. It describes the revolutions per minute (RPM) a motor will achieve per Volt that is put into it. Typically, higher Kv motors spin faster and have lower torque and the opposite is true of lower Kv rated motors. There is plenty of literature online about this sort of thing and it is not my area of expertise so I shall defer you to other, readily available resources online if you want to do any further reading around this.

[^1]: the assumptions are that the relationship is _almost_ linear between % throttle and thrust provided by the motor, verified by plotting some of their similar motor data that includes a lower range of throttle percentage data points. Using this info, a simple linear regression can be applied to the motor data on this motors datasheet.

---

## Shortening the cable length 

The one thing that did surprise me is that the length of the cables that came as standard on the motors was 50cm - lending itself to placing the ESC in the main body of the frame; or have a large bundle of cables at the end of the arm. This led me to reconsider whether the setup I had already selected (ESCs under motors) was the optimal architecture. 

![MN4014_motor_full_cable_50cm](https://github.com/user-attachments/assets/27dbdcaf-4917-4fe4-9884-83eda33d4664)

Mainly driven by not wanting bunches of cables strapped to my (already arguably too big) ESCs, I did some reading around shortening the cables of the motor. The internet left me feeling like the answer was yes, but ensure the cables remain the same length otherwise there will be marginal differences going between the phases of the motor caused by differences in length of the cables. I corroborated this finding with someone in the know and confirmed that I would be okay to shorten the cables.

> [!IMPORTANT]
> If you are shortening the length of the motor cables, make sure you keep them the same length, as varying length may imbalance the motor.

I decided to shorten them enough so that there was not a lot of excess cable there, but left them long enough such that I could use a thicker zipclip around the motor mount clamps to both reinforce the clamping and also hold the ESC -> motor cables in place. I also wanted to use the original connectors that came on each motor, rather than retrofitting my own. To make sure all of these criteria were met, I shortened the length from 500mm per cable to a total of 235mm per cable. I did this by first cutting the length from motor to cable end to 175mm, and then cutting off the connector from the end of the stray cable to a length of 60mm. I then soldered these two parts together, effectivley reattaching the male bullet connector at shorter lenth.

> [!TIP]
> Make sure you put the heat shrink tubing on the cable before you reattach the connector!

![motor_cable_shotening_in_progress](https://github.com/user-attachments/assets/f30bedb2-d811-49d5-b0dd-7fe9c78d3b75)
![motor_shotened_cable3](https://github.com/user-attachments/assets/775f780c-e3e1-4e95-ac87-eef6fef4efcc)

---

## Installing the motors onto the motor mounts
The motor mounts have a carbon plate on their top side which fixes to the motors via a selection of holes within it. It is highly likely that some of these will align with the mounting holes on the bottom of your motor. I used four screws per motor to mount them to the carbon plate.

![carbon_motor_mount_plate](https://github.com/user-attachments/assets/838ec77d-c3a9-4d0d-b910-f7c11848fada)

An important observation that was made during this build was that the mounting screws included with the motor were (just!) too long and impeded the movement of the motor by making contact with the coils. This was due to the fact that the mounting plate is a thin carbon fibre element, if it were bulkier then this would not be an issue. To me, there were two options:

- Replace the M3 bolts with shorter versions
- Use washers on the outside of the mount

As I had some shorter bolts (8mm?), I used these.

The screws that came with the motor (I think 12mm)
![old_motor_screws](https://github.com/user-attachments/assets/be5df695-0ecb-411d-a56a-bd04fe998fae)

The photo I took when changing the screws.
![changing_motor_screws](https://github.com/user-attachments/assets/edb32b63-3b1b-4d13-b711-b110bc8841c7)

Once I had changed all of the screws over I then re-mounted all of the motors to the frame. The ordering of the cables from the ESC to the motor was not important at this point as I would determine their spin direction later on when configuring the software. In the interim, I just connected all four motors the same with the cables going to their nearest connector as shown below.

![ESC_connected_to_motor_closeup](https://github.com/user-attachments/assets/c7395ab8-23a3-4e9c-a00c-939e51819535)

(ultimatley you will end up swapping over the 2 of the 3 cables on two of the motors to get them to spion in the correct direction, but as they are now attached via bullet connectors, this is an easy and fast process.)

![drone_assembled_propulsion_installed3](https://github.com/user-attachments/assets/c451654b-8efc-4432-8e68-9fc5b1c1da1d)

---

## Props

The props being used in this build as the Carbon P15x5 props recommended by T-motor to pair with the MN4014 motor being used. It is important to check that the frame you are using/have designed has enough clearance for the size of the props you want to use. Ideally you would not have the props effectivley being tip to tip when they are spinning, there should be a safe amount of cleareance between them at all points of their rotation.

The props should not be installed at this point as you will just have to uninstall them as soon as you connect any power. But it seems appropriate here to discuss the them. 

With the t-motor props, they are sold in pairs, often one being a clockwise (CW) prop and one being a counter clockwise (CCW) prop. This is conventially declared from a top down view of the drone w.r.t. which way they spin.

The coding on the propellors here are the markings L and R. With 

- L meaning clockwise
- R meaning counter-clockwise

You can find this lettering on the topside of each propeller.

![propellors](https://github.com/user-attachments/assets/0401d972-98de-45eb-8070-123368680871)

Both the motors and the props likely came with small discs which sit on top of them and the bolts go through when installed, I used the ones from the motor box but the two sets were the same diameter, shape and thickness. They come with a card that explains the installation. 

> [!NOTE]
> There is also little coloured stickers with the props that can be used to pair a prop with a particular arm/motor. I would advise checking the rotations are correct multiple times before changing your reference point to the stickers!

➡️ [Continue to: Telemetry >>](06-telemetry.md)




