# PROJECTS PORTIFOLIO
# 💼 Raghav Chadha: Software Project Portfolio

Welcome! This repository showcases my main academic and personal software projects.  
Each project includes a README with the objective, technologies used, architecture overview, and demo screenshots.

> 🔒 The **source code access is available to verified reviewers (e.g., recruiters, hiring managers, professors) upon request** to protect integrity.  
> To review a specific project, please email me at [raghav.chadha25@gmail.com] 
> Include your GitHub username and the project name, and I’ll grant you access for review.

---

## 📘 Projects Overview

### 🚉 [Railway Track Simulator](projects/railway-simulator)

A **real-time multithreaded train traffic simulator** built in **C**, modeling trains traveling from East and West on a **shared single-track system**.  
The program ensures safety, fairness, and concurrency through **mutex locks**, **condition variables**, and precise **thread scheduling**, accurately simulating real-world train operations and control flow.

---

## ⚙️ Key Features

- 🚄 **Real-time railway system simulation**, including dynamic signal and track state management to ensure safe train passage.  
- 🧩 **Implements a multithreaded architecture**, where each train runs as an independent thread using POSIX `pthread_create`.  
- 🔒 **Employs mutex locks and condition variables** to manage shared resource access and prevent race conditions.  
- 🕒 **Simulates realistic scheduling and timing**, with load and crossing delays controlled via sleep intervals and precise time tracking.  
- 🔁 **Maintains directional fairness**: limits consecutive trains in one direction before switching flow.  
- 🧠 **Focuses on performance optimization**, achieving efficient thread-safe synchronization and scalable design.  
- 🚦 **Includes controller thread logic** that prioritizes trains and enforces proper sequencing based on direction and priority queues.  
- ⚙️ **Demonstrates operating system concurrency concepts**, including inter-thread communication and critical section handling.  
- 🧮 **Accurate event logging** for every train: loading, waiting, crossing, and exit times.  
- **Tech:** C • POSIX Threads • Mutexes • Condition Variables • Synchronization  
- **Status:** Completed  

---

### 🗓️ [ICS Calendar Parser](projects/ics-parser)
A **Python-based calendar parser** that reads and converts `.ics` (iCalendar) files into structured, **human-readable output**, efficiently handling **recurring** and **overlapping events**.  
It uses **custom data structures** for event indexing, optimized memory management, and fast parsing of large calendar files, producing organized, chronological summaries for users or automated systems.

---

## ⚙️ Key Features

- **Parses `.ics` calendar files** and converts raw calendar data into readable, structured summaries.  
- **Handles recurring and overlapping events**, expanding recurrence rules and avoiding duplication.  
- **Processes large calendar files efficiently** through custom event indexing and optimized memory handling.  
- **Detects and corrects malformed entries**, ensuring parser resilience across real-world iCalendar formats.  
- **Implements efficient time and date parsing** using Python’s built-in libraries for accurate sorting and filtering.  
- **Supports flexible output formats** (text or structured data) for potential extensions like JSON or CSV export.  
- **Error-tolerant and scalable**, suitable for real-world data from Google, Outlook, or Apple Calendar exports.  
- **Tested on multiple calendar datasets** to ensure consistent behavior under complex recurrence scenarios.  
- **Tech:** Python • File I/O • Data Structures • Date/Time Parsing • Algorithm Design  
- **Status:** Completed  

---

### 🌐 [Simple Web Server (SWS)](projects/simple-web-server)
A fully functional **TCP-based web server** built in **Python**, supporting both **persistent (HTTP/1.1)** and **non-persistent (HTTP/1.0)** connections.  
It serves **multiple concurrent clients**, handles diverse file types and malformed requests, and demonstrates complete **TCP lifecycle compliance** — from connection establishment to teardown — verified through **Wireshark** and **tcpdump** captures.

---

## ⚙️ Key Features

- **Implements a TCP-based web server** supporting both **HTTP/1.0** (non-persistent) and **HTTP/1.1** (persistent/keep-alive) protocols.  
- **Serves multiple concurrent clients** simultaneously without blocking, ensuring smooth parallel communication.  
- **Handles various file types and sizes:** efficiently serves large files (streamed in chunks), small files, and empty files.  
- **Manages malformed or invalid requests**, returning appropriate HTTP status codes (400, 404, 405, 500).  
- **Supports concurrent file transfers** and sustained load through optimized socket handling and thread-safe design.  
- **Follows complete TCP connection lifecycle**, including repeated connect–close cycles and persistent session reuse.  
- **Gracefully handles edge cases**, such as broken connections, missing headers, or corrupted requests.  
- **Fully tested with Wireshark and tcpdump** to validate TCP packet flow, persistence behavior, and data integrity.  
- **Tech:** Python • Sockets • TCP • HTTP/1.0 • HTTP/1.1 • Wireshark • tcpdump  
- **Status:** Completed  
---

## 📬 Contact
📧 [raghavchadha2323@gmail.com](mailto:raghav.chadha25@gmail.com)  
🌐 [LinkedIn](https://www.linkedin.com/in/raghav-chadha-uvic)


🔗 Access to private code available upon request.

