# 🧩 Parts List

Below is a complete list of the components used to build the quadcopter, including the prices at the time of purchase and links to suppliers where available. I have also included some notes on why certain components were selected and any alternatives that were (more seriously) considered.


| Category        | Component                       | Supplier / Link                                                                 | Price (£) | Notes |
|-----------------|----------------------------------|----------------------------------------------------------------------------------|-----------|-------|
| **Frame**       | [Tarot 650 Sport]            | [FlyingTech](https://www.flyingtech.co.uk/product/tarot-650-sport-carbon-fibre-foldable-quadcopter-frame/)                           | £149.90    | 600mm wheelbase, carbon fibre, top plate is the Power Distribution Board (PDB), ideal size for carrying the payloads anticipated.  |
| **Motors**      | [T-Motor MN 4014 330KV]      | [3DXR](https://www.3dxr.co.uk/multirotor-c3/multirotor-motors-c35/t-motor-mn4014-p3510)                                        | £96.90    | Provide sufficient thrust for anticipated mass of quad, slightly overspecified but this will allow slightly larger battery and also more opportunity for alternative payload. Provide 830g of thrust with recommended props (selected below) at 50% throttle. Also operate on 6S battery voltage. |
| **ESCs**        | [T-Motor Alpha 60A ESC - 6S]                 | [3DXR](https://www.3dxr.co.uk/multirotor-c3/multirotor-escs-c48/t-motor-alpha-60a-6s-lv-p2888)                                           | £69.99    | Slight mistake made here, recommended alpha esc for the selected motor is the 40A version of this esc, also did not tell 3DXR as they were in seperate orders and had to buy the datalink v2 to flash the firmware myself. |


| **Flight Controller** | [Betaflight F7 FC]         | [Unmanned Tech UK](https://www.unmannedtechshop.co.uk/)                         | £XX.XX    | F7 for more UARTs and future expansion |
| **Propellers**  | [5x4.3" Tri-blade Props]         | [Amazon](https://www.amazon.co.uk/)                                             | £XX.XX    | Pack of spares; tune for thrust & stability |
| **Receiver**    | [TBS Crossfire Nano RX]          | [Team BlackSheep](https://www.team-blacksheep.com/)                             | £XX.XX    | Long-range capability |
| **Transmitter** | [RadioMaster TX16S]              | [Banggood](https://www.banggood.com/)                                           | £XX.XX    | Versatile and well-supported |
| **Battery**     | [4S 1500mAh LiPo]                | [DroneBitz](https://www.dronebitz.com/)                                         | £XX.XX    | 4S gives a good balance of power and endurance |
| **VTX**         | [Analog VTX or DJI FPV Unit]     | [FPV Drone Store](https://example.com/)                                         | £XX.XX    | Depends on video system; I used [analog/DJI] |
| **Camera**      | [RunCam Phoenix 2 / DJI Cam]     |                                                                                 | £XX.XX    | Depends on video system |
| **Onboard Computer** | [Raspberry Pi 4 / Jetson Nano] | [Pimoroni](https://shop.pimoroni.com/)                                        | £XX.XX    | Used for running onboard algorithms |
| **GPS**         | [Ublox M8N Module]               |                                                                                 | £XX.XX    | Needed for position hold and RTK capability |
| **3D Prints**   | Custom Mounts, Camera Plates     | [STL files](../cad/)                                                            | ~£0 (if you have a printer) | Used for sensor mounting and frame adaptations |
