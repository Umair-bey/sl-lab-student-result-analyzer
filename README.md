# 🎓 Student Result Analyzer

**SL Lab Assignment — Group Project**

**Ramdeobaba University**  
Department of Computer Science and Engineering  
Software Laboratory – I (24CS01PR0303)

---

## 👥 Team Members

| # | Name | Roll Number | Batch |
|---|------|-------------|-------|
| 1 | Umair Khan | A12-B3-50 | B-3 |
| 2 | Utkarsh Vijay Kumbhare | A12-B3-37 | B-3 |
| 3 | Mohammad Afham | A12-B4-60 | B-4 |

**Submission Date:** 15th October  
**Project Topic:** Student Result Analyzer

---

## 📖 About the Project

The **Student Result Analyzer** is a Python-based application that reads student
marks from a text file, performs statistical analysis using **NumPy**, assigns
grades based on averages, and generates a formatted report — all automatically.

Manual result processing is slow, error-prone, and does not scale. This project
demonstrates how core Python data structures (nested dictionaries, tuples, sets)
and NumPy can be combined to build a clean, modular analysis pipeline.

---

## 🎯 Objectives

- Read student records from an external `.txt` file
- Store data using **nested dictionaries** and **tuples**
- Compute total marks, averages, and identify the class topper
- Perform **subject-wise statistics** (mean, max, min, 75th percentile)
- Assign grades (A+, A, B, C, D, F) based on averages
- Identify **unique grades** across the class using sets
- Generate and save a formatted report to `result_report.txt`

---

## 🧠 Concepts Covered (Mapped to Labs 1–5)

| Lab | Concept | Where Used |
|-----|---------|------------|
| Lab 1 | Loops, `if-elif-else` | Grade logic, iterating records |
| Lab 2 | Strings, Lists, Tuples | `split()`, `strip()`, marks stored as tuple |
| Lab 3 | Sets, Nested Dictionaries | `unique_grades()`, `students{}` |
| Lab 4 | Functions, File Handling, `os` | Modular functions, `open()`, `os.path.exists()` |
| Lab 5 | NumPy — mean, max, percentile, boolean masks | `subject_wise_statistics()` |

---

## 📂 Project Files

```
StudentResultAnalyzer/
├── Student_Result_Analyzer.ipynb   ← Main notebook (all code)
├── student_data.txt                ← Input dataset (20 students)
├── result_report.txt               ← Generated output report
└── README.md                       ← This file
```

---

## 🚀 How to Run

### In Jupyter:
1. Open `Student_Result_Analyzer.ipynb`
2. Click **Cell → Run All**
3. Check `result_report.txt` for the output

### As a Python script (optional):
```bash
pip install numpy
python Student_Result_Analyzer.py
```

---

## 📥 Input Format — `student_data.txt`

Each line follows the format:

```
roll_no, name, physics, chemistry, maths
```

**Sample (first 3 records):**

```
101, Amit, 85, 90, 88
102, Riya, 92, 95, 91
103, Rahul, 75, 80, 78
```

Total records: **20 students**

---

## 📤 Output Format — `result_report.txt`

The generated report contains:

1. **Student-wise results table** — Roll | Name | Physics | Chemistry | Maths | Total | Average | Grade
2. **Class topper** — highest total marks
3. **Subject-wise statistics** — mean, max, min, 75th percentile, count above 90
4. **Grade distribution** — count per grade with bar chart
5. **Unique grades present** — set of distinct grades

---

## 📊 Actual Output (From Our Run)

### Result Summary:
```
=======================================================
            RESULT SUMMARY
=======================================================
Class Topper : Meera (Roll 114, Total 288)

Subject-wise Mean:
  Physics   : 80.3
  Chemistry : 82.75
  Maths     : 82.1

Grade Distribution:
  A   : 6 student(s)
  A+  : 6 student(s)
  B   : 5 student(s)
  C   : 2 student(s)
  D   : 1 student(s)

Unique Grades : ['A', 'A+', 'B', 'C', 'D']
=======================================================
```

### Subject-wise Statistics:
| Subject | Mean | Max | Min | 75th %ile | Above 90 |
|---------|------|-----|-----|-----------|----------|
| Physics | 80.3 | 96 | 55 | 90.25 | 5 |
| Chemistry | 82.75 | 95 | 60 | 90.25 | 5 |
| Maths | 82.1 | 98 | 58 | 91.25 | 6 |

### Top Scorers:
| Rank | Roll | Name | Total | Average | Grade |
|------|------|------|-------|---------|-------|
| 1 | 114 | Meera | 288 | 96.0 | A+ |
| 2 | 106 | Priya | 285 | 95.0 | A+ |
| 3 | 120 | Ishita | 279 | 93.0 | A+ |
| 4 | 102 | Riya | 278 | 92.67 | A+ |

---

## 🔧 Requirements

- **Python** 3.10 or higher (tested on 3.13.9)
- **NumPy** — install with `pip install numpy` (tested on 2.3.5)
- **Environment** (Choose one):
  - **Jupyter Notebook** (optional — for running the .ipynb locally)
  - **Google Colab** (optional — for running the .ipynb in the cloud without local setup)


---

## 📌 Notes

- The program uses a **nested dictionary** `{roll: {name, marks}}` for storage
- All statistical operations use **NumPy** for efficiency
- The report is regenerated every time `main()` is run
- The `above_90` count uses a **boolean mask**: `col[col > 90].size`

---
