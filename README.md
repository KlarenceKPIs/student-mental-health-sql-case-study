# student-mental-health-sql-case-study
A SQL case study exploring the relationship between international student status, length of stay, and mental health outcomes using survey data from a Japanese university. Analysis performed in a Jupyter Notebook with PostgreSQL.

# 🧠 Analyzing Mental Health in International Students (SQL + Jupyter Notebook)

**Project Type**: SQL Case Study  
**Source**: [DataCamp - Associate Data Analyst in SQL track]  
**Tools**: PostgreSQL, Jupyter Notebook

---

## 📌 Project Overview

Does going to university in a different country affect your mental health?

A Japanese international university conducted a student mental health survey in 2018. Their study suggested that:
- International students are at **higher risk of depression** than the general population.
- **Social connectedness** and **acculturative stress** are predictive of depression.

In this project, I use SQL to explore whether the data supports these findings and whether **length of stay** also plays a role.

---

## 🧾 Dataset Information

The `students` table includes:

| Column         | Description                                               |
|----------------|-----------------------------------------------------------|
| `inter_dom`    | Type of student: International or Domestic                |
| `japanese_cate`| Japanese language proficiency                             |
| `english_cate` | English language proficiency                              |
| `academic`     | Academic level (Undergrad / Graduate)                     |
| `age`          | Age of the student                                        |
| `stay`         | Length of stay in years                                   |
| `todep`        | Total score of depression (PHQ-9 test)                    |
| `tosc`         | Total score of social connectedness (SCS test)           |
| `toas`         | Total score of acculturative stress (ASISS test)         |

---

## 📘 Notebook Preview

The Jupyter notebook includes:
- SQL queries executed within a Python environment (via `%sql` or similar magic commands)
- Inline visualizations (optional)
- Commentary on observations and conclusions

> 📄 **File:** [`mental_health_students_analysis.ipynb`](./mental_health_students_analysis.ipynb)

---

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
