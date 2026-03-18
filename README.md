# Customer Support SLA Automation 📊⚙️

## Project Overview

This mini project automates the **analysis of customer support tickets** and generates **SLA (Service Level Agreement) reports** using Python.

The goal is to simulate a **real-world data analyst task** where support ticket data must be cleaned, analyzed, and transformed into automated reports for monitoring team performance.

---

## Project Structure

```
Customer-Support-SLA-Automation
│
├── python_automation_support_tickets.csv
├── automation_support_report.py
├── README.md
└── support_automation_reports
    ├── kpi_summary.csv
    ├── tickets_by_priority.csv
    ├── tickets_by_agent.csv
    ├── monthly_tickets.csv
    └── tickets_by_issue_type.csv
```

---

## Dataset

**File:** `python_automation_support_tickets.csv`

The dataset contains customer support tickets with fields such as:

* Ticket ID
* Created Date
* Resolved Date
* Priority
* Agent
* Issue Type
* Response Time
* Resolution Time
* Status

---

## Data Processing Steps

### 1️⃣ Load the Dataset

The script loads the support ticket dataset using **Pandas**.

### 2️⃣ Data Exploration

Initial exploration includes:

* `head()` → preview the data
* `info()` → check data types
* `isna().sum()` → identify missing values

### 3️⃣ Data Cleaning

The script performs several cleaning tasks:

* Parse `created_at` and `resolved_at` columns as datetime
* Standardize text fields (priority, agent, issue type)
* Remove duplicate records
* Fill missing values
* Fix invalid response or resolution times

### 4️⃣ Feature Engineering

New calculated columns are created:

* **Month** → extracted from ticket creation date
* **Resolved Flag** → indicates if a ticket is resolved
* **SLA Target Hours** → expected resolution time based on priority
* **SLA Met Flag** → whether the ticket met SLA requirements

---

## Reports Generated

The script automatically generates several analytical reports:

### KPI Summary

High-level support performance metrics.

### Tickets by Priority

Distribution of tickets across priority levels.

### Tickets by Agent

Number of tickets handled by each support agent.

### Monthly Tickets

Ticket volume trend by month.

### Tickets by Issue Type

Breakdown of tickets based on problem category.

### Backlog Tickets

List of unresolved or pending tickets.

---

## Output

All generated reports are automatically saved in:

```
support_automation_reports/
```

Formats include:

* CSV files
* Excel reports

---

## Technologies Used

* Python 🐍
* Pandas
* Excel Export (OpenPyXL)
* Data Cleaning
* Data Analysis Automation

---

## Author

**Abdelrhman Mohammed Aja**

---
