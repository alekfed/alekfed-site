+++
title = "Control Systems Engineering"
subtitle = "Experience: 6 years"
tags = ['Other']
date = 2020-02-25

# For description meta tag
description = "Linear algebra, complex analysis and groups."

# Comment next line and the default banner wil be used.
banner = 'img/math_control.svg'

+++

I have an experience in control systems engineering for aircrafts (UAVs) and testing devices for spacecraft power supply systems.

# Publications

While studying in graduate school, I published [twenty articles](https://www.elibrary.ru/author_items.asp?pubrole=100&authorid=872738&show_refs=1&show_option=0) (only in [English](https://www.researchgate.net/scientific-contributions/A-S-Fedchenko-2111061948)) and three patents:

- https://patents.google.com/patent/RU153595U1
- https://patents.google.com/patent/RU154432U1
- https://patents.google.com/patent/RU159208U1

All of them are related to spacecraft power supply testing.

# Tools

[MATLAB](https://www.mathworks.com/products/matlab.html) is often the primary (and most mature) choice for the control systems development. Since at some point I started using [pandas](https://pandas.pydata.org/), I decided to move my control systems environment to Python as well and used [python-control](https://python-control.readthedocs.io/en/0.9.0/) for this.

Today, I would work on control systems using [Julia](https://julialang.org/), because it has quite mature packages for the [control systems](http://juliacontrol.github.io/ControlSystems.jl/latest/) themselves, for analysis with [uncertainties](https://github.com/baggepinnen/MonteCarloMeasurements.jl), and it has a very impressive [integrator collection](https://diffeq.sciml.ai/stable/).

# Testing devices

I was involved in the development of electronic loads with power recovery and programmable charging/discharging devices. I researched the issues of control systems coordination between individual load cells (that consisted of switched-mode converters and wide-band linear regulators) in order to obtain the required input admittance characteristics, in particular, for the possibility to induct current interference with an amplitude of tens of amperes.

In general, my work looked like this: first, simple control systems were made using IIR filters or broadband analog PID controllers for the initial mathematical models, then stable systems were identified (using the [N4SID and MOESP](https://en.wikipedia.org/wiki/Subspace_identification_method) algorithms), then MIMO H∞-controllers for several converters were synthesized and then mutual influence of the cells was balanced.

# Rotorcraft UAV

For helicopters, I developed both the control system itself with the necessary processing circuits and a simulation mathematical model of the helicopter, since without closed control loops the helicopter is an unstable system, which greatly complicates the synthesis of the control systems.

The mathematical model was largely based on the work of [Padfield](https://www.amazon.com/Helicopter-Flight-Dynamics-Including-Treatment/dp/1119401054/) and [Johnson](https://www.amazon.com/Rotorcraft-Aeromechanics-Cambridge-Aerospace-Johnson/dp/1107028078/) and was developed in C++ (for more details see [C++](/skills/cpp) section).

The control system was developed as a set of MIMO controllers due to the strong mutual influence of control loops (especially in swashplate cyclic pitch). In addition to the classical versions (H∞, PID), several experimental controllers were investigated, in particular:

- nonlinear controllers (obtained by [backstepping](https://en.wikipedia.org/wiki/Backstepping)): unfortunately, they turned out to be highly dependent on the elaboration of the mathematical model and gave too conservative results (which, generally speaking, is logical for Lyapunov controllers);

- neural networks-based controllers ([Keras](https://keras.io/), see [Python](/skills/python)): they were made by the reinforcement learning method with gradient search for the optimum. They spent a lot of computational resourses, stability was not always ensured even in the simplest flight modes, and the reliability of such a control system in extreme modes was not guaranteed in any way.

# Filters

Various digital filters have also been developed for control systems (see [C++](/skills/cpp)). In particular, when developing the module for determining the wind direction from indirect data, I built various types of estimators ([UKF](https://en.wikipedia.org/wiki/Kalman_filter#Unscented_Kalman_filter), [multiparticle](https://en.wikipedia.org/wiki/Particle_filter)), but in the end the simple [extended Kalman filter](https://en.wikipedia.org/wiki/Extended_Kalman_filter) did a great job.

___
# Illustration

- Composition: cover of the [excellent book](https://www.amazon.com/Nonlinear-Systems-3rd-Hassan-Khalil/dp/0130673897/) by Hassan Khalil on Nonlinear Systems.


- Equations: [extended Kalman filter](https://en.wikipedia.org/wiki/Extended_Kalman_filter).

- Block diagram: [LTI system](https://en.wikipedia.org/wiki/Linear_time-invariant_system) with uncertainties, transformed using [LFT](https://en.wikipedia.org/wiki/Linear_fractional_transformation) to a form convenient for the analysis and synthesis of robust controllers ([the article](https://core.ac.uk/download/pdf/84317308.pdf), which introduced the fashion for such things).

- Helicopter in the background: [Commanche](https://en.wikipedia.org/wiki/Boeing%E2%80%93Sikorsky_RAH-66_Comanche), I liked its appearance since childhood.
