### 💡 Project Overview & Idea 📖

This simulation sets up a **CAN network** with two nodes, each managed by CAPL scripts:

- **Node 1** (`AccelerationPedal`): Responsible for controlling the **pedal accelerator** with two commands—`ACCELERATION_COMMAND` to increase speed gradually and `DECELERATION_COMMAND` to decrease speed gradually. It sends these commands to **Node 2** (`EngineControl`).

- **Node 2** (`EngineControl`): Adjusts the **vehicle’s speed** based on the command received from `AccelerationPedal`. After updating the speed, it sends the new speed back to `AccelerationPedal`, maintaining continuous feedback within the network.

🌟 What We’ve Built
CAN Network Setup: Two nodes simulate engine and pedal behavior.
Database: Manages messages and signals for node communication.
CAPL Scripts: Handle both event-driven and timer-based actions.
🧩 Key Components
Network Setup 🌐

Built in CANoe with two nodes: EngineControl and AccelerationPedal.
Communication simulates real-world control for acceleration and speed limits.
CAPL Scripting 📜

System Variables: Trigger event-driven actions (like changing acceleration).
Timers: Perform periodic actions (e.g., read pedal input every 200 ms).
Database 🗄️

Contains message and signal definitions specific to each node.
🚀 Getting Started
Prerequisites
CANoe (for simulation and CAPL scripting)
Basic knowledge of CAN protocol and CAPL scripting
Running the Simulation
Open the CANoe project.
Load the configuration for EngineControl and AccelerationPedal nodes.
Start the simulation to see real-time message exchanges in action!
Project Structure
/scripts: CAPL scripts for EngineControl and AccelerationPedal nodes.
/database: Message and signal definitions.
README.md: Project details and setup guide.
📂 Example Script Highlights
Engine Control Script 🛑🚀

Handles acceleration/deceleration commands and limits speed between defined thresholds.
Sends current speed messages back to the CAN network.
Acceleration Pedal Script 🦶

Periodically reads pedal position and transmits acceleration commands to EngineControl.
⚡ Features and Usage
System Variable Events: Trigger acceleration and deceleration actions based on pedal position.
Timer Events: Pedal values update every 200 ms, simulating real input timing.
📜 License
This project is licensed under the free trial canoe demo version provided by VECTOR INFORMATIK GmbH.
