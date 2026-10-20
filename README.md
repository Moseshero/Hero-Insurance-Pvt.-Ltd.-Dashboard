# Hero-Insurance-Pvt.-Ltd.-Dashboard
An interactive Excel dashboard analysing premiums, claims and policy status across 10,004 insurance policies.


<img width="744" height="374" alt="Image" src="https://github.com/user-attachments/assets/a29fbcee-ff2f-4476-8b74-f0ad4188ffe9" />

---

## Table of Contents
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Tools and Skills](#tools-and-skills)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Dashboard Components](#dashboard-components)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Challenges and Lessons](#challenges-and-lessons)
- [Repository Structure](#repository-structure)
- [Contact](#contact)

---

## Business Problem
An insurer needs a quick view of how its policy book is performing. This dashboard answers:
- Which policy types generate the most premium?
- How are claims distributed by status and by age group?
- How healthy is the policy book, in terms of active policies and the claim ratio?

---

## Dataset

A sample insurance dataset of 10,004 policies, provided as part of an Excel course on Udemy.

| Field | Description |
|---|---|
| Policy ID | Unique identifier for each policy |
| Policy Type | Auto, Health, Home, Life, Travel |
| Premium Amount | Premium paid on the policy |
| Coverage Amount | Total amount the policy covers |
| Claim Amount | Amount claimed |
| Claim Status | Pending, Rejected, Settled |
| Age / Gender | Customer demographics |
| Policy Start / End Date | Policy period |

> **Note:** The data is synthetic, which explains the unusually high claim ratio.

---

## Tools and Skills

- Microsoft Excel
- Power Query
- PivotTables and slicers
- GETPIVOTDATA
- KPI cards and charts
- Custom number formats
- Data cleaning

---

## Data Cleaning and Preparation

1. **Checked for duplicates** using Policy ID (none found).
2. **Standardised data types:** converted Age from text to number, amounts to decimal, and corrected the date format.
3. **Created an Age Group column:**

   | Age | Group |
   |---|---|
   | 24 and under | Young Adult |
   | 25 to 60 | Adult |
   | Above 60 | Elder |

4. **Created an Active/Inactive column** with a formula comparing each policy's end date to a reference date of **December 31st, 2024**. Policies ending on or after that date are Active, and earlier ones are Inactive.
5. **Built PivotTables** and connected the slicers (Policy Type, Gender, Active/Inactive) to all of them.
6. **Designed the dashboard:** KPI cards, charts and a key insights box.

---

## Dashboard Components

**KPI cards**

| KPI | Value |
|---|---|
| Total Policies | 10,004 |
| Premium Amount | 6.0M |
| Coverage Amount | 600.6M |
| Claim Amount | 16.9M |
| Claim Ratio | 283% |
| Average Claim per Policy | 1,691 |
| Average Premium per Policy | 597 |

**Charts and tables**

- Premium Amount by Policy Type
- Count of Active/Inactive Policies
- Claim Amount by Age Group
- Number of Claims by Status
- Premium Amount by Policy Type and Claim Status (table)

**Slicers:** Policy Type, Active/Inactive, Gender

---

## Key Insights

1. **Travel leads premium.** Travel brings in 2.5M, about 41% of total premium, and together with Health accounts for roughly 61%.
2. **Home and Life are underperforming.** They contribute only 0.6M and 0.7M, about 22% of premium combined, so they may be an opportunity for growth.
3. **Rejected claims are the largest group.** About 44% of claims are rejected, against 34% settled and 23% pending, so the rejection process deserves a closer look.
4. **Claims far exceed premium.** The 16.9M in claims is about 2.8x the 6.0M premium, a ratio that would be unsustainable for a real insurer and likely reflects synthetic data.

---

## Recommendations

- Review the claim rejection process to understand why 44% of claims are rejected.
- Grow Home and Life sales, since they are the smallest premium lines.
- Focus retention efforts on the 25% of policies that are inactive.

---

## Challenges and Lessons

- Ages stored as text and inconsistent date formats had to be fixed before the PivotTables worked.
- Dates in dd-mm-yyyy format caused errors during conversion, which I solved by converting with a day-first locale in Power Query.
- The 283% claim ratio looked wrong at first, so I checked for duplicates and verified the totals before concluding it came from the dataset.
- Revising the dashboard taught me to match chart types to the data (columns for categories, not lines) and to label every table and chart clearly.

---

## Repository Structure

```
hero-insurance-dashboard/
├── README.md
├── Hero_Insurance_Dashboard.xlsx
└── images/
    └── dashboard.png
```

---

## Contact

**Moseshero**
- Email: Mtamusa@gmail.com
