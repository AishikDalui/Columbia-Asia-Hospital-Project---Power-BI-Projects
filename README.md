# Columbia Asia Hospital — Power BI & SQL Analytics

Interactive Power BI dashboard and SQL analysis of 9,200+ hospital patient records, built to help Columbia Asia Hospital make data-driven decisions on **revenue, staffing, and patient discount strategy**.

## 📊 Project Overview

Acting as a consultant data analyst, this project turns raw hospital operations data into decision-ready insights across three business objectives:

- **Revenue Generation** — where does the hospital make its money, and which departments drive it?
- **Hiring Priorities** — which departments are most in need of additional doctors?
- **Patient Discount Strategy** — where and how should discounts be offered without hurting margins?

## 🗂️ Dataset

One operational table (`hospital_er`) of patient visit records — 9,216 rows, 14 fields.

| Column | Description |
|---|---|
| Date | Visit date & time (DD-MM-YYYY HH:MM) |
| Patient ID | Unique identifier (e.g. `124-62-3289`) |
| Patient Gender | M / F |
| Patient Age | Age in years |
| Patient Sat Score | Single-digit patient satisfaction score |
| Patient First Initial | First initial of patient's first name |
| Patient Last Name | Patient's surname |
| Patient Race | White, African American, Asian, Native American/Alaska Native, Two or More Races, etc. |
| Patient Admin Flag | Boolean (TRUE/FALSE) administrative indicator |
| Patient Wait Time | Minutes waited before being seen |
| Department Referral | Department assigned, or "None" |
| Doctor Name | Attending doctor |
| Appointment Fees | Consultation cost |
| Total Bill | Full amount billed, including all charges |

## 🛠️ Tools & Skills

- **Power BI** — data modeling, DAX measures, interactive dashboards
- **SQL** — rule-based, multi-condition analysis (rankings, ratios, diversity checks)
- **Power Query (M)** — data cleaning and transformation
- **DAX** — CALCULATE, aggregation, and row-iteration functions

## 🧹 Data Preparation

- Verified column data types against schema
- Handled nulls in `patient sat score` (replaced with 0 to avoid skewing the average)
- Split combined date-time field into separate Date and Time columns
- Merged first/last name initials into a readable `Patient Name` column
- Built a custom `Age Group` column (0-18, 19-35, 36-50, 51-65, 66+) via Power Query M

## 🔍 Key Insights

**Revenue**
- Orthopaedics (173M) and General Practice (156M) generate ~65% of total revenue
- Neurology has the highest average bill per visit (0.38M) and the highest appointment fee (₹1,500)
- Younger patients (0-18, 19-35) generate the most revenue overall

**Staffing**
- General Practice handles 75%+ of all patient visits (7.2K of ~9.2K) but runs on just 3 doctors — the clearest staffing mismatch in the data
- Neurology and Physiotherapy have the longest average waits (37 min)
- Within General Practice, the morning shift sees 2x the patient load of the evening shift (4.8K vs 2.4K)

**Patient Discounts**
- Satisfaction drops sharply once wait time passes ~35–40 minutes
- 0–18 and 19–35 age groups make up the largest share of visits (44%+)
- Patients aged 66+ report the lowest satisfaction score (5.14 / 10)
- No meaningful gender or racial bias found in wait times or visit counts

## 💡 Recommendations

1. Protect and grow Neurology and Cardiology — the hospital's highest-margin departments
2. Hire additional doctors into General Practice first, prioritizing second-shift coverage
3. Offer a wait-time goodwill discount past the ~35-minute mark
4. Run discount campaigns targeting the 0–18 and 19–35 segments for maximum reach, and a loyalty discount for 66+ patients to improve retention

## 📸 Dashboard Preview

**Overview** — KPIs, revenue by department/age group, waiting time, gender split
![Dashboard Overview](images/dashboard-overview.png)

**Doctors' Tab** — drill-down into individual doctor performance
![Doctors' Tab](images/doctors-tab.png)

**Patients' Tab** — drill-down into individual patient profiles
![Patients' Tab](images/patients-tab.png)

**Financial & Demographic Overview** — billing, gender split, and wait time by department
![Financial & Demographic Overview](images/financial-demographic-overview.png)

**Departments & Shift Analysis** — doctor allocation, patient load, and shift patterns
![Departments & Shift Analysis](images/departments-shift-analysis.png)

**Trends & Demographics** — wait time vs. satisfaction, age/race distribution, yearly visit trends
![Trends & Demographics](images/trends-demographics.png)

## 📁 Repository Contents

| File | Description |
|---|---|
| `POWER_BI_REPORT.pbix` | Power BI report file (dashboard + data model) |
| `Objective_and_Subjective_Questions.docx` | Full Q&A write-up of the analysis |
| `Columbia_Asia_Consulting_Report_AishikDalui.pptx` | Consulting-style presentation deck |
| `images/` | Dashboard screenshots used in this README |

## 👤 Author

**Aishik Dalui**
Data Analyst | Power BI • SQL • DAX
[Portfolio](https://aishikdalui-dataanalyst.tech) · [GitHub](https://github.com/AishikDalui)
