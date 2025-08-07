# 🛰️ GPS

The GPS unit being used in this build us the Here 4 that is part of the flight controller bundle purchased.

![GPS](https://github.com/user-attachments/assets/9ea9e310-beca-4e0c-9016-85bd1e212da0)

---

## Mission Planner Setup
It is pretty easy to install and use and there is plenty of documentation online. Their official documentation is [here](https://docs.cubepilot.org/user-guides/here-4/here-4-manual) and I also used this video in how to configure it within mission planner (you may want to defer this until the next step when you are doing all of the software configuration). With that said, at this point, the drone build in terms of electronics is complete and you can therefore connect to mission planner via the telemetry link and update the parameters to make it function as you desire.

[![Watch the video](https://img.youtube.com/vi/L6gyeE3Q22A/0.jpg)](https://www.youtube.com/watch?v=L6gyeE3Q22A)

---

## Install onto the drone
It is customary (at least historically) to place the GPS on a stand above the rest of the electronics to prevent any electromagnetic interference. I am honestly unsure how much of a requirement this is with these modern devices. Nonetheless, I thought it would give me a great excuse to get the 3D printer out and dust of my CAD skills.

> [!NOTE]
> You can buy pretty good looking, removable GPS stands from a variety of trusted vendors and they are inexpensive (~£10ish), this is not something you have to bodge yourself.

I ended up loading up Fusion360 and designing a simple stand that (due to my infrequent and lacking CAD abilities) ended up being a single piece of print, rather than as I initially intended, a modular design which I could refine and print the different elements to make better. It did however _more or less_ line up with the fixing holes available on the tarot 650 frame. 

If you do want the .stl file for it, is is [here](files/GPS_stand_v1.stl). I will note that without reinforcing the central stick, it is quite springy, and could almost certaintly do with being thicker, or being replaced with a more appropriate material at a minimum (PLA+ be flexin). To remedy this, I quite lazily reinforced it with a wooden dowell, using two trusty zipties at the top and bottom to secure it.

<img width="292" height="430" alt="image" src="https://github.com/user-attachments/assets/777d9a51-122a-432d-8e28-7710f227cbb7" />

I then applied some double sided sticky tape to the bottom of it and secured it in place using the two holes designed to sit over those in the top plate of the drone. Using a nut and bolt to hold the stand in place. The GPS comes with a small circle of double sided foam tape for affixing it.

![GPS_installed](https://github.com/user-attachments/assets/954ebaae-c75f-4410-b93e-c0ed501316bc)

➡️ [Continue to: Software Setup >>](09-software-config.md)

