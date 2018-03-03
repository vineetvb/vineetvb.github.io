---
title: Introducing the Micromouse Simulator
resume: 
---


## What is a Micromouse ?

A Micromouse is a maze solving robot that conforms to the rules of design- e.g. those specified by [IEEE here]( http://sites.ieee.org/r1/files/2013/03/2013-Region-1-Micromouse-Competition-Rules.pdf). Micromouse contests are held worldwide where robot enthusiasts build robots that compete to win the prize of the fastest robot to solve the maze.

Back in 2007, I made my first foray into building micromouse robots, and now in 2018, I am reviving that project with the aim of competing in a US contest in 2018. Here is the mouse I made in 2007:

![My mouse 2007](https://raw.githubusercontent.com/vineetvb/vineetvb.github.io/master/images/micromouse3.jpg =250x)


## Why a simulator ?

The algorithmic challenges of building a maze solving robot are many fold. There are different combinations exploration and fast-run algorithms that can affect the scoring [see the rule book above for scoring]. Moreover, the dynamics of the robot also affects the manner of maze exploration and fast-runs and which algorithm might be suitable.

The problem of testing your algorithms and simultaneously building optimal hardware is somewhat circularly dependent. Hardware is expensive and the cost of crashing and damaging hardware is quite high. It would be great if we could somehow know before hand what a certain hardware capability would buy us and how would the algorithms change to maximize this new hardware feature. Thus, the simulator was born.

Another problem testing your algorithms on hardware directly is the iteration time to download new code on your system, collect data and debug the situation is extremely high. One way to counter this that I have tried in the past is to do a controlled data collection run, where the mouse is manually controlled while logging sensor data. This logged data can then be streamed to your coding environment when you are testing your algorithms without downloading new code to the system. In the long run my goal is to be able to simulate sensor data as well. This will shorten the iteration cycle and enable high development velocity.


The simulator is a work-in-progress and I plan to add more simulation capabilities as my hardware matures as well. Currently, the focus is discrete exploration algorithms and as the simulator is somewhat limited beyond that.

## Micromuse simulator

The simulator is under active develpment at github.com:vineetvb/micromouse. As much as possible, I am attempting to keep the Simulation layer as similar as possible to the Hardware Abstraction layer that runs on my actual robot. The code is written to be as simple and high-level as possible without resorting to premature optimization- prioritizing readability and maintanability above all else. I also wanted people to download and be able to run the simulator on their machines as easily as possible, so I have minimized the dependencies needed to run it.

Here is an example run from the simulator:
![MouseRun](https://raw.githubusercontent.com/vineetvb/micromouse/floodfill/artwork/anim.gif)


