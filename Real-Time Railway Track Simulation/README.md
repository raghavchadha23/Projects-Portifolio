💬 For access to this project or other portfolio work, please email me at:

📩 raghav.chadha25@gmail.com

# 🚉 Railway Track Simulation (MTS)

This project is a **multithreaded train traffic simulator** built in **C**.  
It models trains traveling from East and West directions on a **single shared railway track**, ensuring synchronization, fairness, and safety through the use of **POSIX threads**, **mutexes**, and **condition variables**.

The simulation demonstrates principles of **operating systems concurrency control**:  multiple threads (representing trains) must coordinate access to a critical shared resource (the track) without conflicts.

---

## 🧠 Project Overview

The program reads a list of trains and their parameters (direction, loading time, crossing time) from `input.txt`.  
Each train runs as a separate thread and simulates:

- Loading before departure  
- Waiting for track availability  
- Crossing the track safely  

A **controller thread** manages the order of crossings, applies direction and priority rules, and ensures that trains from both directions get fair access to the track.

---

## ⚙️ Core Features

| Feature | Description |
|----------|-------------|
| 🧵 **Multithreading** | Each train runs as its own thread using `pthread_create`. |
| 🔒 **Synchronization** | Uses mutexes and condition variables to control access to shared queues and track. |
| 🚦 **Priority Management** | Four queues are maintained: `E`, `W` (priority), and `e`, `w` (regular),  each with their own mutex. |
| 🚉 **Track Controller** | A separate controller thread enforces the “one train at a time” rule and alternates direction after three consecutive trains. |
| 🕒 **Timing Simulation** | Real-time loading and crossing are simulated with `usleep()` delays and timestamped logs. |

---

## 🧩 Input File Format (`input.txt`)
Each line in `input.txt` defines a train:

### Example:

E 2 3<br>
e 4 3<br>
W 3 4<br>

- **Direction:**
  - `E` → Eastbound (priority)
  - `e` → Eastbound (normal)
  - `W` → Westbound (priority)
  - `w` → Westbound (normal)
- **Loading time:** Time (in seconds) before a train is ready to depart.
- **Crossing time:** Time (in seconds) it takes for the train to cross the track.

---

## 🧰 Technologies Used

- **Language:** C  
- **Concurrency Library:** `pthread`  
- **Key Headers:** `pthread.h`, `unistd.h`, `time.h`, `stdio.h`, `stdlib.h`  
- **Concepts Demonstrated:**  
  - Thread creation and joining  
  - Mutex locks and condition variables  
  - Shared resource synchronization  
  - Fairness and priority scheduling  

---

## 🧱 Project Structure

mts/<br>
&nbsp;&nbsp;&nbsp;&nbsp;├── mts.c <br>
&nbsp;&nbsp;&nbsp;&nbsp;├── Makefile<br>
&nbsp;&nbsp;&nbsp;&nbsp;├── input.txt <br>
&nbsp;&nbsp;&nbsp;&nbsp;├── readme.txt <br>
&nbsp;&nbsp;&nbsp;&nbsp;└── README.md<br>



---

## ⚙️ Setup and Execution Guide

### Prerequisites
Ensure you have:
- GCC compiler (`gcc`)
- POSIX threads support (installed by default on Linux/macOS)
- Terminal or shell access

---

### 🧰 How to Run

1. **Clone or navigate to the project folder**
   ```bash
   cd "portfolio/Real-Time Railway Track Simulation"
  

2. **Verify input line**
   ```bash
   cat input.txt
   

3. **Build the project**
  ```bash
   make
```

4. **Run the simulation**
  ```bash
  ./mts
```
🪪 License
© 2025 Raghav Chadha. All rights reserved.
This project is provided for academic and professional showcase purposes only.
Redistribution, modification, or reuse of the source code without permission is strictly prohibited.
💬 For access to this project or other portfolio work, please email me at:

📩 raghav.chadha25@gmail.com
