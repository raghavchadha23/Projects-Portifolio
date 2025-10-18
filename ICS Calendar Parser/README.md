💬 For access to this project or other portfolio work, please email me at:  
📩 **raghav.chadha25@gmail.com**

🔒 The **source code access is available to verified reviewers (e.g., recruiters, hiring managers, professors) upon request** to protect integrity. 

# 🗓️ ICS Calendar Parser

This project is a **Python-based parser** for **iCalendar (.ics)** files.  
It converts raw calendar data into **structured, human-readable output**, handling **recurring** and **overlapping** events while keeping ordering and time conflicts clear.

The parser demonstrates principles of **file parsing and data structures**: events are extracted, indexed, and formatted in a readable format.

---

## 🧠 Project Overview

The program reads an `.ics` file (used by Google Calendar, Outlook, Apple Calendar) and outputs a clean list of events with **start/end time, summary, and location**.  
It normalizes recurring rules and resolves overlaps so the final output is chronological and easy to scan.

- Parsing the iCalendar format  
- Detecting overlapping/recurring events  
- Producing readable, de-duplicated summaries

---

## ⚙️ Core Features

| Feature | Description |
|----------|-------------|
| 📄 **ICS Parsing** | Reads and tokenizes standard `.ics` (iCalendar) fields (e.g., `VEVENT`, `DTSTART`, `DTEND`, `RRULE`). |
| 🔁 **Recurrence Handling** | Expands recurring events into concrete instances within a time range. |
| ⏱️ **Overlap Resolution** | Identifies and orders overlapping events for clarity. |
| 🧰 **Custom Indexing** | Efficient in-memory structures for fast sort/filter. |
| 🚀 **Performance-Oriented** | Designed to handle large `.ics` files cleanly. |

---

## 🧩 Input File Format (`input.ics`)
Each event is defined as a `VEVENT` in the `.ics` file.

**Example (snippet):**  
BEGIN:VEVENT<br>
SUMMARY:Team Sync<br>
DTSTART:20251021T100000<br>
DTEND:20251021T103000<br>
LOCATION:Zoom<br>
RRULE:FREQ=WEEKLY;BYDAY=TU<br>
END:VEVENT<br>

- **SUMMARY**: Human title of the event  
- **DTSTART/DTEND**: Start and end timestamp (UTC or with TZ)  
- **LOCATION**: Where the event occurs  
- **RRULE**: Recurrence rule (optional)

---

## 🧰 Technologies Used

- **Language:** Python  
- **Key Modules:** `datetime`, `re` (regex), optional third-party date utils (document in `requirements.txt` if used)  
- **Concepts Demonstrated:**  
  - Text/file parsing  
  - Recurrence expansion & overlap handling  
  - Data structuring and sorting

---

## 🧱 Project Structure

ics-parser/<br>
&nbsp;&nbsp;&nbsp;&nbsp;├── ics_parser.py &nbsp;&nbsp;# Core parser source code<br>
&nbsp;&nbsp;&nbsp;&nbsp;├── input.ics &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Sample calendar input<br>
&nbsp;&nbsp;&nbsp;&nbsp;├── output.txt &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Example parsed output<br>
&nbsp;&nbsp;&nbsp;&nbsp;├── requirements.txt &nbsp;# Dependencies (if any)<br>
&nbsp;&nbsp;&nbsp;&nbsp;└── README.md &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# This documentation<br>

---

## ⚙️ Setup and Execution Guide

### Prerequisites and HOW TO RUN: 
**Ensure you have:*
- Python 3.8+:
  ```bash
  pip install -r requirements.txt

  python3 ics_parser.py input.ics
  ```

🪪 License

© 2025 Raghav Chadha. All rights reserved.
This project is provided for academic and professional showcase purposes only.
Redistribution, modification, or reuse of the source code without permission is strictly prohibited.

💬 For access to this project or other portfolio work, please email me at:
📩 raghav.chadha25@gmail.com```
