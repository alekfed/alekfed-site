+++
title = "C/C++"
subtitle = "Experience: 4 years"
tags = ['Languages']
date = 2020-03-21

# For description meta tag
description = "Chasing the minimal overhead."

# Comment next line and the default banner wil be used.
banner = 'img/cpp.svg'

+++

Since I started programming with microcontrollers, C became my first "serious" language. But at some point I became interested in writing native desktop GUIs, and started to learn, how classes and templates can help me at large...

*Note:* I'm **not interested** in C/C++ jobs at the moment.

# RTOS

In C++, I developed an in-house [Hard RTOS](https://en.wikipedia.org/wiki/Real-time_operating_system) which is used in the control system of the rotorcraft [UAV](https://en.wikipedia.org/wiki/Unmanned_aerial_vehicle). Despite the widespread belief that "C++ has too big overhead for microcontrollers, especially for providing hard real-time capabilities", everything somehow fitted in memory, and hard real-time was provided on microcontrollers with one CPU without a floating point coprocessor.

Before that, already in C, I worked with [FreeRTOS](https://freertos.org/), which I used to develop control systems for switched-mode power converters and for the firmware of a radio modems that worked with an [Iridium] (https: //www.iridium. com /) satellite constellation and was used in then-developed UAV.

# DSP

Since the embedded operating systems I worked with were written in C and C ++, [DSP](https://en.wikipedia.org/wiki/Digital_signal_processing) modules were also written in the corresponding languages for the needs of control systems. Basically, it was highly simplified libraries for linear algebra and mathematical analysis for the implementation of various filters: [Kalman](https://en.wikipedia.org/wiki/Kalman_filter), [elliptic](https://en.wikipedia.org/wiki/Elliptic_filter), [FIR](https://en.wikipedia.org/wiki/Finite_impulse_response), [IIR](https://en.wikipedia.org/wiki/Infinite_impulse_response).

# Simulation model

In the course of work on the UAV control system, I also developed a simulation model of the helicopter, which, among other things, had to work with full-fledged hardware versions of control units ([HIL](https://en.wikipedia.org/wiki/Hardware- in-the-loop_simulation)). This work was done using [adevs](https://web.ornl.gov/~nutarojj/adevs/), ODE solvers from [SUNDIALS](https://computing.llnl.gov/projects/sundials) and linear algebra routines from [Blaze](https://bitbucket.org/blaze-lib/blaze/src/master/).

# Qt

Before switching to web-based solutions (see [Python](/skills/python)), I spent some time developing interfaces for testing equipment in Qt. Too much boilerplate for a simple set of buttons, switches and graphs...

___
# Illustration

- Composition: covers of the cult C++ books from Addison-Wesley by Scott Myers and The "Gang of Four": [Design Patterns](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/), [Effective C++](https://www.amazon.com/Effective-Specific-Improve-Programs-Designs/dp/0321334876/), [More Effective C++](https://www.amazon.com/More-Effective-Improve-Programs-Designs/dp/020163371X/), [Effective STL](https://www.amazon.com/Effective-STL-Specific-Standard-Template/dp/0201749629/).

- It's dangerous to go alone! Take [this](https://zelda.fandom.com/wiki/Triforce).

- Perhaps, everyone who was in [the C++ lands](http://goldns.ru/cppmap-2012.png) had visited [the C++ standards committee secretary's mill](https://herbsutter.com/).

- "Elements of Overcomplicated Designs" — it's personal 😄

- Magic square: since the cover of "Design Patterns" features [Escher's "Swans"](https://arthive.com/escher/works/200315~Swans), I wanted to put something like that on my quasi-cover. "Swans" somehow reminded me of the magic square from [Dürer's "Melencolia I"](https://en.wikipedia.org/wiki/Melencolia_I)—perhaps, the same mathematical charm and engraving style...
