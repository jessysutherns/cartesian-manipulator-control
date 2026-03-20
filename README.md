# 🤖 Cartesian Manipulator Control using PID

## 📌 Overview

This project implements a **decentralized control system** for a 3-DOF Cartesian robot manipulator using MATLAB/Simulink.

Each joint is independently controlled using **PID controllers**, enabling accurate trajectory tracking and robust performance under parameter variations.

---

## ⚙️ System Description

The manipulator consists of three prismatic joints operating along:

* X-axis (linear motion)
* Y-axis (sinusoidal motion)
* Z-axis (step motion)

The system is modelled using a **Lagrangian approach**, resulting in dynamic equations of motion for each joint.

---

## 🧠 Control Strategy

A **decentralized PID control architecture** is used:

* Each joint is treated as an independent system
* Control input is computed using tracking error
* Feedback loop ensures stability and accuracy

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

---

## ▶️ Tools Used

* MATLAB
* Simulink

---

## 🚧 Future Improvements

* Adaptive control methods
* Model predictive control (MPC)
* Real-world hardware implementation

---

## 💼 Author

**Jessica Sutherns**
https://github.com/jessysutherns
