# student-mental-health-sql-case-study
A SQL case study exploring the relationship between international student status, length of stay, and mental health outcomes using survey data from a Japanese university. Analysis performed in a Jupyter Notebook with PostgreSQL.

# 🧠 Analyzing Mental Health in International Students (SQL + Jupyter Notebook)

**Project Type**: SQL Case Study  
**Source**: [DataCamp - Associate Data Analyst in SQL track]  
**Tools**: PostgreSQL, Jupyter Notebook
**Files Included**: `Notebook.ipynb`, `students.csv`, `mentalhealth.jpg`

---
![Mental Health](mentalhealth.jpg)
## 📌 Project Overview

Does going to university in a different country affect your mental health?

A Japanese international university conducted a student mental health survey in 2018. Their study suggested that:
- International students are at **higher risk of depression** than the general population.
- **Social connectedness** and **acculturative stress** are predictive of depression.

In this project, I use SQL to explore whether the data supports these findings and whether **length of stay** also plays a role.

---

## 🧾 Dataset Summary

The dataset (`students.csv`) includes the following variables:

| Column         | Description                                               |
|----------------|-----------------------------------------------------------|
| `inter_dom`    | Student type: International or Domestic                   |
| `japanese_cate`| Japanese language proficiency                             |
| `english_cate` | English language proficiency                              |
| `academic`     | Academic level (Undergrad / Graduate)                     |
| `age`          | Student age                                               |
| `stay`         | Length of stay in years                                   |
| `todep`        | Total depression score (PHQ-9)                             |
| `tosc`         | Total social connectedness score (SCS)                    |
| `toas`         | Total acculturative stress score (ASISS)                  |

---

## 📘 Notebook Preview

The Jupyter notebook includes:
- SQL queries executed within a Python environment (via `%sql` or similar magic commands)
- Inline visualizations (optional)
- Commentary on observations and conclusions

> 📄 **File:** [`notebook.ipynb`](./notebook.ipynb)

---
## 🧠 Key Analysis

The notebook explores:
- Trends in **depression (PHQ-9)** based on student type and length of stay
- How **social connectedness** and **acculturative stress** relate to mental health
- Whether longer stays reduce stress and improve social bonding

```sql
-- Sample Query:
SELECT 
  stay,
  COUNT(inter_dom) AS count_int,
  ROUND(AVG(todep), 2) AS average_phq, 
  ROUND(AVG(tosc), 2) AS average_scs, 
  ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;

## 📊 Key Findings

- **Higher depression scores** are associated with shorter stays among international students.
- **Acculturative stress** is initially high but decreases as students stay longer.
- **Social connectedness** tends to increase with time, which may help reduce depression levels.

---

## 💡 Reflections

- Jupyter Notebooks are a great way to combine SQL logic with narrative explanation.
- Mental health is a multi-faceted issue — data analysis provides insights, but human factors matter just as much.
- Language proficiency and academic level could also be worth deeper exploration.

---

## 📁 Files

- `mental_health_students_analysis.ipynb` – Jupyter notebook with full SQL analysis and notes
- `README.md` – This documentation

---

## 🔗 Related Projects

- [SQL Case Studies](https://github.com/yourusername/sql-case-studies)
- [Business Analytics Portfolio](https://github.com/yourusername/portfolio)
