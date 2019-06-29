# Get Started

## How the Z Probe Determines a Successful Print

![probes-positions](assets/probes-positions.jpg)

When you print, it is imperative that the model - the object you're printing - is **stuck to the build plate**; only to be peeled off once the print is finished.

For this, the printer needs to be able to repeatedly and precisely **position the nozzle very close to the build plate** so that the filament gets stuck to it as it's being extruded.

> In short, a badly set-up Z probe guarantees a bad first layer and a print failure.

The Z Probe is an inductive proximity sensor which senses metal objects using electromagnetic field. In JellyBOX, the probe senses the aluminum build plate and thus determines the z home position - just like simple mechanical switches determine the x and y home positions. Therefore, **by adjusting the z probe, we can change the z home position and thus also the first layer height.**

![first-layer-poster.png](assets/first-layer-poster.png ':size=400%')

## The Plan

1. First, we need to **move the Z probe itself** into the right position. (* Only if you use the _adjustable Z probe mount_.)
2. Then, we will use the LCD controller (aka rotary encoder) to **calibrate the 1st layer height** to perfection via live adjustment.

<details>
<summary><b>* Adjustable vs. Fixed Z probe mount (click to expand)</b></summary>

![zprobe-mount.png](assets/zprobe-mount.png)

**Adjustable Z probe mount** is
- 👍 Perfect for power users who want to use hotends of different lengths (like full metal E3D v6 hotend).
- 👍 Compatible with jb JellyBOX Original and 2.
- 👎 Under certain conditions can move if disturbed.

**Fixed Z probe mount** is
- 👍 Easier to use
- 👍 Can never move once set-up
- 👎 Is only compatible with JellyBOX 2 in the moment
</details>


## What about Different JellyBOX Versions?

There are differences between how the Z probe looks for different JellyBOXes, but the techniques and principles in this guide are the same for all. Proceed without fear.