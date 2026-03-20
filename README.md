# 🤖 Cartesian Manipulator Modelling and Control using PID

## 📌 Overview

This project presents the **modelling, simulation, and control** of a 3-DOF Cartesian robot manipulator using MATLAB/Simulink.

The system is first derived using **Lagrangian dynamics**, then implemented in Simulink to simulate its behaviour, and finally controlled using **decentralized PID controllers** to achieve accurate trajectory tracking.

**This project reflects a complete robotics workflow from dynamic modelling to control system implementation.**

---

## ⚙️ System Description

The manipulator consists of three prismatic joints operating along:

* X-axis (linear motion)
* Y-axis (sinusoidal motion)
* Z-axis (step motion)

The system dynamics are derived using a **Lagrangian formulation** to obtain the equations of motion for each joint.

---

## 🧮 Dynamic Modelling

The dynamic behaviour of the Cartesian manipulator is derived using a **Lagrangian formulation**, capturing the relationship between applied forces and joint motion.

* Kinetic energy is based on translational motion of each link
* Potential energy is influenced by gravity along the Z-axis
* Euler–Lagrange equations are used to derive the system dynamics

This results in second-order differential equations describing each joint:

* X-axis: q̈x = Fx / mx
* Y-axis: q̈y = Fy / my
* Z-axis: q̈z = (Fz − mg) / mz

These equations form the foundation of the simulation model and are used to compute acceleration, velocity, and position over time.

![Dynamic Model](results/dynamic_model_simulink.png)

---

## 🧠 Control Strategy

A **decentralized PID control architecture** is used:

* Each joint is treated as an independent system
* Control input is computed using tracking error
* Feedback loop ensures stability and accuracy

The controller minimizes the error between:

* Desired trajectory
* Actual joint position

---

## 🧩 Control System Architecture

The control system is implemented in Simulink using a decentralized PID structure.

Each prismatic joint (X, Y, Z) includes:

* Reference trajectory input
* Error calculation (desired − actual)
* PID controller
* Dynamic system (acceleration → velocity → position)
* Feedback loop

![Control Architecture](results/simulink_control_architecture.png)

---

### 🔹 Example: Single Joint Control Loop

The following diagram shows a zoomed-in view of the control loop for a single prismatic joint.

![Single Joint Control](results/single_joint_control_diagram.png)

---

## 📊 Results

### 🔹 Linear Trajectory (X-axis)

![Linear Error](results/tracking_error_linear.png)

### 🔹 Sinusoidal Trajectory (Y-axis)

![Sine Error](results/tracking_error_sine.png)

### 🔹 Step Trajectory (Z-axis)

![Step Error](results/tracking_error_step.png)

### 🔹 Robustness Test (5% Parameter Variation)

![Robustness](results/robustness_comparison.png)

---

## 📈 Key Observations

* PID controllers successfully reduce tracking error
* System stabilizes quickly after initial transients
* Minor overshoot observed in step response
* Controller remains stable under parameter variation
* Demonstrates strong robustness and reliability

---

## 🧩 Simulink Model

The full system, including both dynamic modelling and control implementation, is developed in Simulink.

The model file is available in the `models/` folder.

---

## ▶️ Tools Used

* MATLAB
* Simulink

---

## 🚧 Future Improvements

* Adaptive or robust control methods
* Model predictive control (MPC)
* Multi-axis coupling effects
* Real-world hardware implementation

---

## 💼 Author

**Jessica Sutherns**
https://github.com/jessysutherns

---

## ⭐ Project Significance

This project demonstrates a complete robotics pipeline including:

* Dynamic modelling of manipulators
* Simulation of physical systems
* Control system design
* Performance evaluation

It highlights how modelling and control work together to enable **precise and stable robotic motion** in real-world applications.
