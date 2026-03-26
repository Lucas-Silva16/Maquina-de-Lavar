# Washing Machine FSM Controller in Verilog

![Language](https://img.shields.io/badge/Language-Verilog-blue)
![Tools](https://img.shields.io/badge/Tools-Xilinx_ISE-orange)
![Domain](https://img.shields.io/badge/Domain-Finite_State_Machine-lightgrey)

## Introduction
This project simulates the control logic of a fully automated washing machine using **Verilog**. Developed and simulated in the **Xilinx ISE** environment, it relies on a robust Finite State Machine (FSM) to manage the strict sequence of operations required in a standard washing cycle

---

## Objectives
To design and implement a hardware-level **Finite State Machine (FSM)** capable of safely executing a complete washing cycle. The modeled sequence includes:
* Water Fill
* Heating
* Detergent Dispensing
* Active Wash
* Rinse Cycle
* Spin Cycle
* Door Release

---

## Core Features
* **Deterministic State Management:** A well-defined FSM architecture strictly controlled by synchronous `start`, `pause`, and `reset` signals.
* **Power Failure Protection (State Retention):** Capable of retaining its current state and resuming the cycle precisely where it left off in the event of an interruption.
* **Scheduled Execution:** Includes logic for a delayed start, allowing the machine to begin its cycle based on scheduled timing.

---

## System Architecture
* **State Memory:** Sequential logic block driven by the system clock (`clk`) and control signals to update current states.
* **Next State Logic:** Combinational block defining the strict transition conditions between different washing phases.
* **Output Decoder:** Combinational logic that drives the machine's simulated actuators (water valves, heater, drum motor, door lock) based strictly on the current active state.

---

## Validation & Testing
The digital logic was verified using Xilinx ISE testbenches, covering the following critical scenarios:
* **Standard Cycle:** Triggering the `start` signal and monitoring the correct sequential transition through all states (Wash -> Rinse -> Spin).
* **Interrupt Handling:** Asserting the `pause` signal mid-cycle and verifying that the FSM properly holds its state until resumed.
* **System Reset:** Ensuring the system safely abort
