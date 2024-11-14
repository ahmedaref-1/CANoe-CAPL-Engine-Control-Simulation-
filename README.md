### 💡 Project Overview & Key Features 📖

This project simulates a **CAN network** with two nodes managed by CAPL scripts, representing the behavior of an acceleration pedal and vehicle speed control. The simulation uses **event-driven** and **timer-based** actions to model real-world automotive control within CANoe’s demo environment.

### 🌟 Simulation Highlights

- **Node 1** (`AccelerationPedal`): Controls the pedal with commands to gradually adjust speed, using `ACCELERATION_COMMAND` to increase and `DECELERATION_COMMAND` to decrease speed. The command is then sent to **Node 2** (`EngineControl`).
  
- **Node 2** (`EngineControl`): Receives speed commands from `AccelerationPedal`, adjusts the vehicle’s speed accordingly, and sends the updated speed back, maintaining a continuous data exchange.

### 🧩 Key Components

1. **CAN Network Setup** 🌐  
   - Configured in CANoe with two nodes: `EngineControl` and `AccelerationPedal`.
   - The setup enables simulated control over vehicle acceleration and speed limit monitoring.

2. **CAPL Scripting** 📜  
   - **System Variables**: Manage event-driven actions, like toggling acceleration and deceleration.
   - **Timers**: Enable periodic actions, such as reading pedal input every 200 ms.

3. **Database** 🗄️  
   - Contains detailed message and signal definitions for each node, ensuring precise data flow.

4. **Panel View** 🎛️  
   - **Pedal Simulation Button**: Simulate pedal press events to trigger acceleration and deceleration.
   - **Analog Speed Gauge**: Visualizes the vehicle’s speed, acting as a virtual speedometer.
   - **Digital Speed Counter**: Displays the real-time numerical speed value.
   - **Red LED Threshold Alarm**: Lights up when the speed crosses the set threshold, alerting the user to potential overspeeding.

5. **CAN Trace View** 🔍  
   - Offers comprehensive monitoring of all messages on the CAN bus, showing each message's **ID**, **value**, and **timing**.
   - Allows for real-time analysis and verification of the communication between nodes, ensuring accurate message flow and timing across the network.

These components work together to create a detailed and interactive CAN network simulation that accurately reflects vehicle dynamics and control mechanisms in a virtual environment.

---

### 🚀 Getting Started

**Prerequisites**  
- **CANoe** (for simulation and CAPL scripting)
- Basic knowledge of CAN protocol and CAPL scripting

**Running the Simulation**  
1. Open the CANoe project.
2. Load the configuration for the `EngineControl` and `AccelerationPedal` nodes.
3. Start the simulation to observe real-time message exchanges.

**Project Structure**  
- **/scripts**: CAPL scripts for the `EngineControl` and `AccelerationPedal` nodes.
- **/database**: Database file containing messages and signal definitions.
- **README.md**: This guide, detailing project setup and structure.

---

### 📂 Example Script Highlights

- **Engine Control Script** 🛑🚀  
  - Processes acceleration and deceleration commands.
  - Limits speed according to predefined thresholds and sends the current speed to the CAN network.

- **Acceleration Pedal Script** 🦶  
  - Periodically reads pedal values and transmits acceleration commands to `EngineControl`.

---

### ⚡ Features and Usage

- **System Variable Events**: Trigger acceleration or deceleration actions based on pedal position.
- **Timer Events**: Pedal values update every 200 ms, simulating realistic input timing.

---

### 📜 License

This project uses the free trial CANoe demo version provided by VECTOR INFORMATIK GmbH.
