Download full dataset: [Google Drive Link](https://drive.google.com/file/d/1-8__VqSb3LLxAvBNhpuja_eDNCzNIOnC/view?usp=drive_link)

# Task 1: Telemetry Data Dashboard (Tableau)

## 🧾 Objective
Analyze telemetry data collected from Daikibo’s 4 factories and identify:
1. Which factory had the most machine downtime?
2. Which machine types broke most often in that factory?

## 🧰 Tools Used
- Tableau (Desktop Trial)
- JSON data import
- Calculated Field, Bar Charts, Dashboard

## 🧠 Steps Performed
1. Imported `daikibo-telemetry-data.json` into Tableau.
2. Created a **calculated field** named `Unhealthy`:
   ```tableau
   IF [status] = "unhealthy" THEN 10 ELSE 0 END
