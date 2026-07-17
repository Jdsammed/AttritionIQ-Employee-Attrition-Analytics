# AttritionIQ — EDA Snapshot (Pre-Analysis Checkpoint)

**Dataset:** IBM HR Analytics Employee Attrition Dataset
**File:** HR_Attrition_Cleaned.xlsx
**Tool used:** ChatGPT (free tier) — Python/Pandas script generation

## 1. Data Cleaning Summary
- Original dataset: 1,470 rows × 35 columns
- Checked for missing values → none found
- Checked for duplicate rows → none found
- Dropped 3 constant columns (no analytical value, same value in all rows):
  - `EmployeeCount` (always 1)
  - `Over18` (always "Y")
  - `StandardHours` (always 80)
- **Cleaned dataset: 1,470 rows × 32 columns**

## 2. Data Types
All columns confirmed correctly typed after cleaning:
- Numeric (`int64`): Age, DailyRate, DistanceFromHome, Education, MonthlyIncome, TotalWorkingYears, YearsAtCompany, etc.
- Categorical (`object`): Attrition, BusinessTravel, Department, EducationField, Gender, JobRole, MaritalStatus, OverTime

## 3. Key Headline Stat
**Overall Attrition Rate: 16.12%** (Yes) vs **83.88%** (No)
→ Roughly 1 in every 6 employees left the company.

## 4. Summary Statistics

| Statistic | MonthlyIncome | Age |
|-----------|--------------:|----:|
| Mean      | 6,502.93      | 36.92 |
| Min       | 1,009         | 18 |
| Max       | 19,999        | 60 |

## 5. Next Steps
- Explore attrition drivers using Julius AI (natural-language queries)
- Cross-check Julius AI's answers manually in Excel PivotTables
- Build Power BI dashboard: attrition by department, overtime, tenure, salary band
- Write business recommendations
- Publish cleaned dataset, scripts, dashboard, and this note to GitHub with a README
