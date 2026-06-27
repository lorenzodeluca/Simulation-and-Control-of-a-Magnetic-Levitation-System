### Simulation and Control of a Magnetic Levitation System

This repository contains the project for the modeling, simulation, and control of a Single-Input Single-Output (SISO) magnetic levitation system. The project focuses on linearizing a highly non-linear physical system around its equilibrium point and designing a feedback control strategy to ensure stability.

### System Overview

The system consists of a levitating magnet actuated by controlling the currents of surrounding solenoids. Due to the lack of friction, the uncontrolled open-loop system is **not BIBO stable** (Bounded-Input Bounded-Output).

### Key Characteristics & Assumptions

*   **Mass (m):** Approximated with a point mass moving exclusively in the vertical direction (z).
*   **Rotations & Inertia:** Negligible moment of inertia; rotations are disregarded.
*   **Permanent Magnets:** Upward push force, inversely proportional to the distance (z).
*   **Solenoids:** Push/pull force, inversely proportional to the distance (z) and proportional to the input current (i(t)).

* * *

### Mathematical Model

### Non-linear SISO Model

The dynamic equation governing the system is:  𝑚𝑧̈\=−𝐹𝑝+𝐹𝑚(𝑧)+𝐹𝑠(𝑧,𝑖)−𝑑𝑧̇

Where:

*   𝐹𝑝 Gravity force
*   𝐹𝑚 Permanent magnet force
*   𝐹𝑠 Solenoid force
*   dż Damping/friction factor

### Equilibrium and Linearization

To obtain a Linear Time-Invariant (LTI) model, the system is linearized around the equilibrium point (z₀, i₀) where i₀ = 0:  

𝑧\=𝑧0+𝑧̃,𝑖\=𝑖0+𝑖̃

The resulting linear equation in the state-space form or transfer function via Laplace transform yields:  

𝑍(𝑠)\=𝑀(𝑠)+𝐺(𝑠)𝐼(𝑠)

Where the plant transfer function G(s) is:  

𝐺(𝑠)\=𝑏𝑠𝑧0𝑚𝑠2+𝑑𝑠+𝑏𝑚𝑧20

* * *

### Requirements and Tools

*   **MATLAB & Simulink** (For numerical simulation and control design)
*   **LaTeX Compiler** 

If you are new to these tools, you can explore the following introductory resources:

*   [MATLAB Onramp](https://matlabacademy.mathworks.com/details/matlab-onramp/gettingstarted)
*   [Simulink Onramp](https://matlabacademy.mathworks.com/details/simulink-onramp/simulink)
*   [LaTeX Video Introduction](https://www.youtube.com/watch?v=zqQM66uAig0)

* * *



*Project developed based on the course materials provided by Niccolò Turcato (niccolo.turcato@phd.unipd.it) - Università degli Studi di Padova.*
