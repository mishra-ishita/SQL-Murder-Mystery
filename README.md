# 🕵️‍♂️ **SQL Murder Mystery — Case Closed (Capstone Project)**

## 📌 **Project Overview**

This project is part of the **21-Day SQL Challenge by Indian Data Club**, where I investigated a fictional crime titled **“Who Killed the CEO?”** using SQL queries, log analysis, and analytical reasoning.

The objective was to determine:
* **Where** the crime happened
* **When** it occurred
* **Who** accessed the crime scene
* **Who lied in their alibi**
* **What evidence matched the movement logs**
* **Who committed the murder**

The project required analyzing five tables:
**employees**, **keycard_logs**, **calls**, **alibis**, and **evidence**.

## 🗂 **Dataset Description**
### **1. employees**
| Column      | Type    | Description         |
| ----------- | ------- | ------------------- |
| employee_id | INT     | Unique employee ID  |
| name        | VARCHAR | Employee name       |
| department  | VARCHAR | Employee department |
| role        | VARCHAR | Role/Designation    |

### **2. keycard_logs**
| Column      | Type     | Description                    |
| ----------- | -------- | ------------------------------ |
| log_id      | INT      | Keycard log entry              |
| employee_id | INT      | Employee who accessed the room |
| room        | VARCHAR  | Room accessed                  |
| entry_time  | DATETIME | Time of entry                  |
| exit_time   | DATETIME | Time of exit                   |

### **3. calls**
| Column       | Type     | Description          |
| ------------ | -------- | -------------------- |
| call_id      | INT      | Unique call entry    |
| caller_id    | INT      | Caller employee ID   |
| receiver_id  | INT      | Receiver employee ID |
| call_time    | DATETIME | Time of call         |
| duration_sec | INT      | Duration in seconds  |

### **4. alibis**
| Column           | Type     | Description                      |
| ---------------- | -------- | -------------------------------- |
| alibi_id         | INT      | Alibi entry                      |
| employee_id      | INT      | Employee ID                      |
| claimed_location | VARCHAR  | Where the employee claimed to be |
| claim_time       | DATETIME | Time of the claim                |

### **5. evidence**
| Column      | Type     | Description             |
| ----------- | -------- | ----------------------- |
| evidence_id | INT      | Evidence item ID        |
| room        | VARCHAR  | Location found          |
| description | TEXT     | Description of evidence |
| found_time  | DATETIME | Time evidence was found |


## 🔍 **Investigation Steps**

### **1️⃣ Identifying Crime Location & Time**
* Analyzed evidence timestamps
* Checked keycard logs around the same period

### **2️⃣ Who Accessed the CEO’s Office?**
* Filtered logs between 8:50 PM and 9:10 PM

### **3️⃣ Alibi Verification**
* Compared claimed locations with actual movement logs
* Highlighted mismatches

### **4️⃣ Suspicious Calls**
* Checked calls around the crime window (20:50–21:00)

### **5️⃣ Evidence Matching**
* Cross-checked evidence timestamps with room access

### **6️⃣ Final Correlation**
* Combined logs, alibis, calls, and evidence
* Identified the killer

## 🟥 **Final Verdict**
### 🔪 **Killer Identified: *David Kumar***
### 📍 **Crime Location: CEO’s Office**
### ⏰ **Time of Crime: Around 9:00 PM**

### **Why David Kumar?*
* Entered the **CEO’s Office** during the crime window
* Provided a **false alibi** (claimed to be in Server Room)
* Made **suspicious calls** around crime time
* Evidence found in the room correlated with his presence
* Multiple **alibi mismatches** flagged by SQL checks

## 🛠 **Skills Demonstrated**
* **Advanced SQL Joins**
* **Time-based filtering**
* **Cross-table validation**
* **CTEs & Subqueries**
* **Pattern detection in logs**
* **Analytical reasoning**
* **Data storytelling**
