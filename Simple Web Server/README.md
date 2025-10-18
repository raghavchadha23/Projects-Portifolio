💬 For access to this project or other portfolio work, please email me at:  
📩 **raghav.chadha25@gmail.com**

# 🌐 Simple Web Server (SWS)

A **Python-based HTTP server** that supports **multiple concurrent requests**, serves **small and large files**, and correctly handles **repeated connection initiations** following **TCP** and **HTTP/1.0 & HTTP/1.1** semantics (non-persistent and persistent/keep-alive).  
It demonstrates core networking concepts: **socket programming**, **request parsing**, **connection lifecycle management**, **concurrency**, and **observability** via logs and packet captures.

---

## 🧠 Project Overview

The server listens on a configurable port, accepts **multiple client connections**, parses HTTP requests, and responds with content from a configurable **document root**.  
It supports:

- **HTTP/1.0 (non-persistent):** close after each response  
- **HTTP/1.1 keep-alive (persistent):** reuse a TCP connection for multiple requests within a timeout  
- **Concurrent clients:** handle many requests “at once” via threading or evented I/O  
- **Small & large files:** stream responses efficiently to avoid blocking on big payloads  
- **Repeated connection setup:** robustly accepts new connections again and again per TCP rules (3-way handshake, orderly close, timeouts)

> Packet captures (`.cap`) are included to showcase both persistent and non-persistent sessions.

---

## ⚙️ Core Features

| Feature | Description |
|---|---|
| 🔌 **TCP Stream Sockets** | Accepts and serves HTTP over reliable byte streams (listen, accept, read, write, shutdown/close). |
| 🔁 **Persistent & Non-Persistent** | HTTP/1.1 keep-alive with idle timeout; HTTP/1.0 closes after response. |
| 👥 **Concurrency** | Handles **multiple clients simultaneously** (per-connection worker or multiplexing). |
| 🗂️ **Static File Serving** | Safely serves **small and large files** from a configurable `www/` root; streams large files in chunks. |
| 🧪 **Protocol Correctness** | Validates method, target, version; returns `200/400/404/405/500` as appropriate. |
| 🧭 **Connection Lifecycle** | Cleanly handles repeated connect/close, half-closes, and timeouts. |
| 📜 **Access Logging** | Logs method, path, status, bytes, remote addr, and response time for each request. |
| 🛰️ **Packet Traces** | `.cap` captures for **persistent** and **non-persistent** sessions (inspect with Wireshark/tcpdump). |

---

## 🧰 Technologies Used

- **Language:** Python  
- **Stdlib:** `socket`, `threading` (or `selectors`), `os`, `time`, `logging`  
- **Tools (debug):** **Wireshark**, **tcpdump**, `curl`, `ab`/`wrk` (optional)  
- **Concepts:** TCP stream sockets, HTTP/1.0 vs HTTP/1.1, keep-alive, concurrency, streaming I/O, logging

---

## 🧩 Request/Response Behavior

- **Methods:** `GET` for static files (others may return `405 Method Not Allowed`)  
- **Status Codes:**  
  - `200 OK` — file found and served  
  - `404 Not Found` — missing path  
  - `400 Bad Request` — malformed start-line/headers  
  - `405 Method Not Allowed` — unsupported method  
  - `500 Internal Server Error` — unexpected exception  
- **Headers:** minimal set (e.g., `Content-Length`, `Content-Type`, `Connection`)  
- **Connection Reuse:** HTTP/1.1 defaults to persistent; closes on timeout or `Connection: close`

---

## 🧱 Project Structure

sws/<br>
&nbsp;&nbsp;&nbsp;&nbsp;── **sws.py** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Main HTTP server (sockets, handlers, concurrency)<br>
&nbsp;&nbsp;&nbsp;&nbsp;── **www/** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Document root (public files)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;── index.html<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;── bigfile.bin &nbsp;&nbsp;&nbsp;# Example large file (optional)<br>
&nbsp;&nbsp;&nbsp;&nbsp;── **logs/** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Access/error logs<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;── access.log<br>
&nbsp;&nbsp;&nbsp;&nbsp;── **captures/** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Packet captures (demo sessions)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;── sws-persistent.cap &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# HTTP/1.1 keep-alive session<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;── sws-non-persistent.cap &nbsp;# HTTP/1.0 close-after-response<br>
&nbsp;&nbsp;&nbsp;&nbsp;── **README.md** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# This documentation<br>

> Some filenames are placeholders; the actual set may vary. Full source remains **private** for copyright issues.

---

## ⚙️ Configuration

- **Port:** default `8080` (override with `--port 8000`)  
- **Document root:** default `./www` (override with `--root PATH`)  
- **Keep-alive idle timeout:** default `5s` (override with `--keepalive 10`)  
- **Log file:** `logs/access.log` (override with `--log PATH`)

**Example:**
```bash
python3 sws.py --port 8000 --root ./www --keepalive 10 --log ./logs/access.log
```

📚 **Learning Outcomes**

1. Building a TCP stream socket server in Python
2. Understanding HTTP/1.0 vs HTTP/1.1 keep-alive and connection reuse
3. Managing concurrency and streaming I/O for large and small files
4. Observability with access logs and packet captures (Wireshark/tcpdump)
5. Robust connection lifecycle management (repeated connect/close, idle, timeouts)

🔒 **Source Code Access**

The complete source code is private to avoid copyright issues.
If you’d like to review it for evaluation or hiring purposes, please contact:

📩 raghav.chadha25@gmail.com

🪪 **License**

© 2025 Raghav Chadha. All rights reserved.
This project is provided for academic and professional showcase purposes only.
Redistribution, modification, or reuse of the source code without permission is strictly prohibited.



