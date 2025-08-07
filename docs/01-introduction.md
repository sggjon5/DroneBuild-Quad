# 🛠️ Introduction

For a bit of context, I completed an MEng in Aerospace Engineering in 2021 and have since pursued a PhD with a more computer science–oriented focus, primarily exploring decision-making under uncertainty for applications in multi-target tracking. As PhDs often are, it has been heavily simulation-based, and I’ve found myself missing the hands-on challenges that come with developing physical systems, the kind that operate in the real world, not just the virtual one.

To address the above, I decided to build a quadcopter drone capable of carrying a companion computer and some onboard sensing capability (tbd), with the aim of testing some of the algorithms I’ve developed during my PhD in real-world conditions. This repository is intended to document the full lifecycle of building the quadcopter, culminating in a functional testbed for the aforementioned sensor management algorithms.

The drone itself has been designed to be general purpose, with enough payload capacity to support a variety of small, but meaningful, components - making it a flexible platform for future development projects as well.

To put some numbers to it, I was aiming for a takeoff weight (without any payload) of about 2.5-3kg, with some payload capacity left over so that I could build things into/onto it in the future.

I was starting from basically no tools (other than general household things like pliers, screwdrivers, allan keys, zip-ties, etc) and have therefore included the cost of obtainign all 'new' tools in total running cost of this project to keep it transparent. As I have written this, I realised I also have a 3D printer that I used to print a GPS stand that would have likely cost ~£10 if I had not have designed and printed one.

None of this work has been sponsored by any of the vendors that I have used and therefore I am happy to provide an impartial review that they have all been excellent w.r.t. their correspondence and delivery times.

---

## 🎯 Project Goals

- Learn the full drone build process: from frame selection to first flight
- Create a modular and maintainable quadcopter that can be modified for other purposes
- Share a detailed, beginner friendly guide that is open and accessible

---

## 🔍 What You'll Find in This Guide

This repo contains:

- A full parts & tools list, with links and costs
- A step-by-step recollection of the process, including mistakes and things that added costs...
- A wiring diagram
- Software setup and parameters
- Demo videos and photos (from when I remembered to take them...)

Whether it is just curiosity, you are planning your own custom build, or stuck halfway through it, I hope this guide is helpful.

---

## 🧠 Skills Developed (or at least had to refresh!)

- Basic electronics & soldering
- Engineering design
- CAD (Fusion360)
- 3D printing (also had to replace the hot end on the printer)
- Firmware flashing and configuration
- Mechanical assembly
- ETHOS (transmitter OS)
- Ground control software (Mission Planner)
- Autopilot software (ArduPilot)
- Latte Art

![latte art](https://github.com/user-attachments/assets/a7c2b577-58bf-41e5-9ea3-50af2a89e9c6)


➡️ [Continue to: Parts List >>](02-parts-list.md)
