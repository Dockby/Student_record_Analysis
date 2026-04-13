# Student Performance Analysis

Intermediate-level data analysis on student academic performance, attendance, and extracurricular participation using Python.

## Tools Used
- Python, pandas, numpy, matplotlib, seaborn

## Dataset
Two CSVs — `student_performance.csv` (30 students, 9 columns) and `student_extracurricular.csv` (21 records) — merged on `student_id`. Data included missing values across attendance and score columns.

## What I Did

**Data Cleaning**
- Imputed missing values in `attendance_pct`, `math_score`, `english_score`, and `science_score` using column means
- Used correct pandas syntax to avoid chained assignment warnings

**Feature Engineering**
- Computed `avg_score` as mean of math, english, and science scores
- Created `pass_fail` column using `np.where()` (pass if avg_score ≥ 60)
- Created `performance_tier` (High / Mid / Low) using `np.select()`

**Merging**
- Left joined performance data with extracurricular data to retain all students
- Filled missing `hours_per_week` with 0 for students with no activity

**Analysis**
- Average score by gender (bar chart)
- Attendance percentage by grade level (bar chart)
- Performance tier distribution (count plot)
- Attendance vs avg score relationship (scatter plot)
- Top performer per grade level

## Key Findings
- **Grade 12** had the highest average attendance
- **Meera** (Grade 12) was the top performer with an avg score of 97.3
- **Ananya** (Grade 11) and **Aarav** (Grade 10) were top performers in their grades
- Students in Grade 9 showed the lowest scores and attendance overall
- A positive relationship was observed between attendance and average score

## Top Performers by Grade
| Grade | Student | Avg Score |
|-------|---------|-----------|
| 9 | Rohit | 58.3 |
| 10 | Aarav | 81.7 |
| 11 | Ananya | 86.7 |
| 12 | Meera | 97.3 |

## Skills Demonstrated
`fillna` · `np.where` · `np.select` · `pd.merge` · `groupby` · `idxmax` · `pivot_table` · `seaborn barplot/countplot/scatterplot`
