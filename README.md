# Data Career Journey 🚀

Rohit's 6-month roadmap to get hired as **Data Analyst / Analytics Engineer / Data Engineer**.

**Target:** Get first job by Dec 2026  
**Current:** B.Tech CSE (AI) — 2025 Passout, Fresher  
**Strategy:** Learn skills common to all 3 roles, apply to all simultaneously

---

## 📁 Repository Structure

```
rohit-career-plan/
├── README.md
├── ROHIT_CAREER_PLAN.md
├── month-1-sql-python/
│   ├── week-1-sql-basics/
│   ├── week-2-sql-advanced/
│   ├── week-3-pandas/
│   └── week-4-stats-excel/
├── month-2-tools/
│   ├── week-5-powerbi/
│   ├── week-6-dbt/
│   ├── week-7-spark-warehouse/
│   └── week-8-airflow-cloud/
├── month-3-projects/
│   ├── week-9-project-1-eda/
│   ├── week-10-project-2-3/
│   ├── week-11-project-4-pipeline/
│   └── week-12-project-5-ml/
├── month-4-apply/
│   ├── week-13-resume-linkedin/
│   ├── week-14-interview-prep/
│   ├── week-15-mock-interviews/
│   └── week-16-aggressive-apply/
├── month-5-interviews/
│   ├── week-17-18-interview-rounds/
│   └── week-19-20-iterate/
├── month-6-close-deal/
│   └── week-21-26-final/
├── projects/
│   ├── project-1-eda-insights/
│   ├── project-2-powerbi-dashboard/
│   ├── project-3-dbt-pipeline/
│   ├── project-4-data-pipeline/
│   └── project-5-ml-analysis/
├── practice/
│   ├── sql/
│   ├── pyspark/
│   ├── pandas/
│   └── datapathsala/
├── interview-prep/
│   ├── star-stories/
│   ├── sql-questions/
│   └── system-design-notes/
├── notes/
└── resume/
```

---

## 📅 Progress Tracking

### Month 1: SQL + Python Foundation
- [ ] Week 1: SQL basics (SELECT, JOINs, GROUP BY)
- [ ] Week 2: SQL advanced (Window Functions, CTEs, Subqueries)
- [ ] Week 3: Python Pandas + NumPy + Data Cleaning
- [ ] Week 4: Statistics + Excel + Visualization

### Month 2: Tools for All 3 Roles
- [ ] Week 5: Power BI (dashboards, DAX)
- [ ] Week 6: dbt (models, tests, docs)
- [ ] Week 7: Spark basics + Data Warehousing
- [ ] Week 8: Airflow + Cloud (AWS) + Docker

### Month 3: Projects
- [ ] Week 9: **PROJECT 1** — EDA + Business Insights
- [ ] Week 10: **PROJECT 2** — Power BI Dashboard + **PROJECT 3** — dbt Pipeline
- [ ] Week 11: **PROJECT 4** — End-to-End Data Pipeline
- [ ] Week 12: **PROJECT 5** — ML Prediction + Analysis

### Month 4: Resume + Interview Prep + Apply
- [ ] Week 13: Resume + LinkedIn + Start applying
- [ ] Week 14: Interview prep (SQL + Python + Stats + dbt + Spark questions)
- [ ] Week 15: Mock interviews
- [ ] Week 16: Aggressive applying (10-15/day)

### Month 5: Interviews
- [ ] Week 17-18: Interview rounds
- [ ] Week 19-20: Iterate and improve

### Month 6: Close the Deal
- [ ] Week 21-26: Negotiate + accept offer

---

## 🛠️ Tech Stack

| Already Know | Learning |
|-------------|----------|
| Python (basic) | Pandas, NumPy, Seaborn |
| SQL (basic) | Window Functions, CTEs, Optimization |
| AI/ML theory | scikit-learn (hands-on) |
| | Power BI, DAX |
| | dbt, Data Modeling |
| | PySpark, Spark SQL |
| | Airflow, Docker |
| | AWS (S3, Glue, Athena) |

---

## 🎯 Target Roles (Applying to ALL simultaneously)

| Role | Companies Hiring | Salary Range |
|------|-----------------|--------------|
| Data Analyst | Mu Sigma, Fractal, Swiggy, Meesho, Deloitte | ₹4-7 LPA |
| Analytics Engineer | Razorpay, CRED, PhonePe, Freshworks | ₹6-10 LPA |
| Data Engineer | Flipkart, Walmart, Delhivery, Groww | ₹5-10 LPA |

---

---

## 📖 HOW TO USE THIS PLAN (Usage Guide)

### 🗓️ Daily Routine — What To Do Every Day

1. **Open `ROHIT_CAREER_PLAN.md`** — check what's planned for this week
2. **Do the tasks** — follow the exact order given for the day
3. **Save your work** in the correct week folder (e.g., `month-1-sql-python/week-1-sql-basics/`)
4. **At end of day** — update progress (see tracking section below)

---

### ✅ How To Track Your Learning (Daily/Weekly)

**Option 1: Checkboxes in README.md (Recommended)**
- Open this file → go to "Progress Tracking" section above
- Mark `[x]` for tasks you complete:
  ```
  Before: - [ ] Week 1: SQL basics
  After:  - [x] Week 1: SQL basics
  ```

**Option 2: Week README files**
- Each week folder has a `README.md` with checkboxes
- Example: `month-1-sql-python/week-1-sql-basics/README.md`
- Mark tasks done as you complete them

**Option 3: Tell Kiro (AI assistant)**
- Just say: *"I completed Week 1 SQL basics, moving to Week 2"*
- Or: *"I solved 15 SQL problems today on HackerRank"*
- Kiro will update your progress tracking

---

### 📝 How To Add Notes

When you learn something, save notes in the `notes/` folder:

```
notes/
├── sql-notes.md          ← SQL tricks, patterns, interview shortcuts
├── pandas-notes.md       ← Pandas operations you keep forgetting
├── dbt-notes.md          ← dbt commands, concepts
├── spark-notes.md        ← PySpark syntax, transformations
├── powerbi-notes.md      ← DAX formulas, Power Query tips
├── airflow-notes.md      ← DAG patterns, operators
└── statistics-notes.md   ← Formulas, concepts for interviews
```

**Format:** Write in your own words. Use examples. Keep it short.

Example note:
```markdown
# SQL Window Functions

## ROW_NUMBER vs RANK vs DENSE_RANK
- ROW_NUMBER: Always unique (1,2,3,4...)
- RANK: Ties get same rank, skips next (1,1,3,4...)
- DENSE_RANK: Ties get same rank, no skip (1,1,2,3...)

## Example:
SELECT name, salary,
  ROW_NUMBER() OVER (ORDER BY salary DESC) as rn,
  RANK() OVER (ORDER BY salary DESC) as rnk
FROM employees;
```

---

### 📊 How To Track Practice Problems

Go to `practice/datapathsala/README.md` — update the table daily:

```markdown
| Date       | SQL | PySpark | Topic              | Notes            |
|------------|-----|---------|--------------------|------------------|
| 2026-06-16 | 5   | 0       | JOINs              | LEFT JOIN tricky |
| 2026-06-17 | 5   | 0       | GROUP BY + HAVING  | Easy today       |
```

Same for `practice/sql/`, `practice/pandas/` — save solution files there:
```
practice/sql/
├── day-01-joins.sql
├── day-02-window-functions.sql
├── day-03-ctes.sql
```

---

### 🚨 What To Do When Something Is Missing / Confusing

| Situation | What To Do |
|-----------|------------|
| Topic not clear after watching video | Search YouTube for another explanation (try Hindi channels: Krish Naik, Codebasics) |
| Stuck on a problem for >30 min | Skip it, mark it, come back tomorrow with fresh mind |
| Week's tasks too easy | Move faster — finish early and start next week |
| Week's tasks too hard | Spend 1 extra day. Don't skip — understanding > speed |
| Need a resource not in the plan | Ask Kiro: *"I need a good resource for [topic]"* |
| Want to add a topic | Create a new `.md` file in `notes/` and study it in spare time |
| Behind schedule | Don't panic. Adjust by 1-2 days. Never quit. |

---

### 💬 How To Update Kiro (AI Assistant)

Just tell me naturally. Examples:

- *"Week 1 done, I solved 25 SQL problems"*
- *"I'm stuck on window functions, explain PARTITION BY"*
- *"I finished Project 1, review my approach"*
- *"I have an interview next week for Data Analyst at Fractal, help me prepare"*
- *"Add a note about dbt snapshots to my notes"*
- *"I'm behind by 3 days, should I skip anything?"*
- *"What should I study today?"*

I'll track your progress, answer questions, create notes, and adjust the plan as needed.

---

### 📁 Where To Put Your Work

| What you created | Where to save it |
|-----------------|------------------|
| SQL practice solutions | `practice/sql/day-XX-topic.sql` |
| Pandas practice | `practice/pandas/day-XX-topic.py` |
| PySpark practice | `practice/pyspark/day-XX-topic.py` |
| DataPathSala solutions | `practice/datapathsala/` |
| Study notes | `notes/topic-name.md` |
| Project 1 code | `projects/project-1-eda-insights/` |
| Project 2 files | `projects/project-2-powerbi-dashboard/` |
| Project 3 code | `projects/project-3-dbt-pipeline/` |
| Project 4 code | `projects/project-4-data-pipeline/` |
| Project 5 code | `projects/project-5-ml-analysis/` |
| Resume drafts | `resume/` |
| Interview answers | `interview-prep/star-stories.md` |
| Mock interview notes | `interview-prep/sql-questions/` |

---

### 🔄 Weekly Review (Every Sunday Night — 15 min)

Ask yourself:
1. ✅ Did I complete this week's tasks?
2. 📊 How many problems did I solve? (target: 35/week minimum)
3. ❌ What did I struggle with? (note it down, revisit Monday)
4. 📅 Am I on track with the plan timeline?
5. 🔜 What's the focus for next week?

Update the checkboxes in this README, then move on.

---

*Started: June 16, 2026*
