# Adaptive Resource Allocation Simulator

A real-time Python simulator demonstrating adaptive CPU and memory allocation in multiprogramming systems. The system dynamically schedules processes based on requested resources, assigns states (Ready, Running, Waiting, Completed), and visualizes execution using a Tkinter GUI.

---

## 🧠 Project Overview

This project simulates a multiprogramming environment where multiple processes request CPU time and memory. The scheduler continuously monitors available resources and allocates them based on system constraints. The GUI provides real-time visualization of:

- CPU usage percentage
- Memory usage percentage
- Dynamic process states
- Execution progress bars

The simulation prevents resource bottlenecks by automatically controlling which processes get CPU time and which must wait.

---

## 🧩 Problem Statement

In multiprogramming systems, multiple programs execute concurrently and share limited resources. Without proper scheduling:

- CPU might stay underutilized
- Memory can overflow
- Some processes may starve
- System performance decreases

This project demonstrates how **adaptive resource allocation** can improve stability, performance, and fairness.

---

## 🎯 Objectives

- Monitor real-time CPU and memory usage
- Simulate multiple processes with different resource requirements
- Dynamically assign process states:
  - **Running**
  - **Ready**
  - **Waiting**
  - **Completed**
- Prevent overload by limiting CPU to 100% and memory to 2048 MB
- Provide visual representation for understanding OS scheduling concepts

---

## 🏗️ System Architecture

**Frontend:**  
- Tkinter GUI  
- Treeview table for process list  
- Progress bars for execution visualization  

**Backend:**  
- `Python`
- `threading` for concurrent scheduling and GUI updates  
- `psutil` for system usage monitoring  

**Process States Highlighting:**  
- 🟩 Green → Running  
- 🟨 Yellow → Ready  
- 🟧 Orange → Waiting  
- ⚪ Gray → Completed  

---

## ⚙️ Core Algorithms

### CPU Allocation
- Total CPU is capped at **100%**
- Processes get CPU time only if available CPU remains

### Memory Allocation
- Total memory limited to **2048 MB**
- If memory limit is reached → extra processes become *Waiting*

### Scheduling Loop
- Runs continuously in a background thread
- Updates progress based on allocated CPU

### Termination
- When progress reaches 100% → state changes to *Completed*


---

## 🛠️ Technologies Used

| Component | Technology |
|---------|------------|
| Programming Language | Python |
| GUI | Tkinter |
| Monitoring | psutil |
| Concurrency | threading |
| Visualization | ttk Progress Bars |

---

## 📁 File Structure

```
project.py                 # Main simulator application

screenshots/              # GUI output demonstration images
├── screenshot_01_initial_view.png
├── screenshot_02_running_ready.png
├── screenshot_03_waiting_state.png
└── screenshot_04_all_states.png

README.md                 # Documentation and project explanation
LICENSE                   # MIT open source license
.gitignore                # Git ignore rules
```

---

## ▶️ How to Run

### 1. Install Dependencies
> (Only required if `psutil` is not already installed)

```bash
pip install psutil
```
### 2. Run the Simulator

```bash
python project.py
```
---

## 📸 Screenshots

### Initial View
![Initial GUI](screenshots/screenshot_01_initial_view.png)

### Running & Ready
![Running & Ready](screenshots/screenshot_02_running_ready.png)

### Waiting State
![Waiting State](screenshots/screenshot_03_waiting_state.png)

### All Process States
![All States](screenshots/screenshot_04_all_states.png)

---
