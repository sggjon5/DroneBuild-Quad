# 🧲 Motors

The motors selected for this project were the T-motor MN4014 330KV motors - a member of the navigator series.

![MN414_motor_up_close](https://github.com/user-attachments/assets/82659fea-2a19-43e4-bd82-3c97fe69583a)

According to the manufacturers datasheet, these motors (when paired with the selected propellors) will provide 830g of thrust at 50% throttle, meaning a total thrust of 3320g. 

By making some assumptions[^1] we can ascertain the relationship between % throttle and thrust to be y = 22.517x - 284.79. Which then provides:

- at 40% throttle, 4 x 615g = 2460g
- at 45% throttle, 4 x 728g = 2912g

This provides the confidence that we will be able to hover (where weight=lift) at an appropriate throttle setting (aiming for between 40-50%) to give good control authority (mass of the drone is currently predicted to be 2,839.3g).

The numbers within a motors name typically conform to the convention of stator diameter by stator height - so in this case, these motors are 40mm in diameter and 14mm in height, forming the 4014.

The KV rating is an indicator of speed potential. It describes the revolutions per minute (RPM) a motor will achieve per Volt that is put into it. Typically, higher Kv motors spin faster and have lower torque and the opposite is true of lower Kv rated motors. There is plenty of literature online about this sort of thing and it is not my area of expertise so I shall defer you to other, readily available resources online if you want to do any further reading around this.

[^1]: the assumptions are that the relationship is _almost_ linear between % throttle and thrust provided by the motor, verified by plotting some of their similar motor data that includes a lower range of throttle percentage data points. Using this info, a simple linear regression can be applied to the motor data on this motors datasheet.

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


## Installing the motors onto the motor mounts














