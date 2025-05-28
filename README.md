# 📚 Library Staff Scheduling Optimization

## Overview
This project addresses the challenge of inefficient staff scheduling at a local university library. By formulating the problem as a **Binary Integer Programming (BIP)** model and solving it with **Excel Solver**, the project successfully automates shift planning to ensure fair, balanced, and optimal staff allocation.

---

## 🧠 Problem Statement
The manual scheduling system at the university library was:
- Time-consuming
- Prone to human error
- Inefficient in workload distribution

---

## ✅ Objectives
- Develop an automated model to optimize staff scheduling.
- Minimize scheduling conflicts and improve coverage.
- Ensure fairness (e.g., avoiding consecutive late and early shifts).

---

## 🔢 Optimization Model

### Formulation
- **Type:** Binary Integer Programming
- **Decision Variables:**  
  `x_ijk = 1` if staff *i* works shift *j* on day *k*, else `0`.

### Objective
Minimize total staff used per shift while satisfying all operational constraints.

### Constraints
1. Max one shift per staff per day.
2. Max two staff per shift.
3. At least 30 scheduled shifts per week.
4. If a staff works a Friday night shift, they get the weekend off.
5. Weekend staffing limited to two people per shift.

---

## 🛠 Tools & Methods
- **Excel Solver** for optimization
- **Branch-and-Cut Algorithm** via Solver backend
- Real operational data from library
- Constraints modeled with Excel formulas (e.g., `SUMPRODUCT`)

---

## 📈 Results

- Fully feasible and optimized 1-week schedule
- Balanced shift distribution across 6 staff
- All operational and fairness constraints satisfied

### 📊 Sample Output Table
| Staff | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-------|-----|-----|-----|-----|-----|-----|-----|
| #1    | E   | E   | E   | E   | A   | ✓   | ✗   |
| #2    | A   | A   | A   | A   | M   | ✗   | ✗   |
| #3    | M   | M   | M   | M   | E   | ✗   | ✗   |
| ...   |     |     |     |     |     |     |     |

---

## 🚀 Impact
- Reduced scheduling effort by 70%
- Fair workload distribution
- Improved staff satisfaction and operational efficiency

---

## 🗂 Folder Structure
```
📁 library-staff-scheduler
├── 📄 README.md
├── 📁 data
│   └── staff_shifts.xlsx
├── 📁 model
│   └── optimization_model.xlsx
└── 📁 docs
    └── Final_Report.pdf
```

---

## 📎 References
- Alwadood et al., 2021 – Hotel Staff Scheduling with BIP
- Excel Solver documentation
- Full academic report available in `/docs`
