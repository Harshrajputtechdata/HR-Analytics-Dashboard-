# HR Analytics Dashboard | Power BI

## Overview

An interactive Power BI report for exploring employee attrition, workforce demographics, department-level patterns, and employee tenure. The dashboard brings workforce KPIs and detailed breakdowns together on a single report page to support exploratory HR analysis.

## Business Objectives

- Monitor workforce size, active employees, attrition count, and attrition rate.
- Compare attrition counts across departments and experience levels.
- Explore employee distributions by age group and salary slab.
- Examine attrition counts by job role and job satisfaction.
- Use department and age-group filters to focus on specific employee segments.

> This project supports descriptive analysis. Patterns in the report do not establish the causes of employee attrition.

## Tools and Technologies

- **Microsoft Power BI Desktop** — report development and visualization.
- **DAX** — the report references an `Attrition rate %` measure.
- **PBIX** — packaged Power BI report and embedded data model.

## Dashboard Features

### KPI Cards

| Dashboard label | Report configuration / interpretation |
|---|---|
| Total Employee | Count of employee IDs. |
| Active Employee | Count of employee IDs; confirm the visual filter restricts this to active employees. |
| Attrition Count | Sum of the `Attrition count` field. |
| Attrition rate | Uses the `Attrition rate %` measure; validate its definition in the model. |
| Average Age | Average of `Age`. |
| Avg Experience | Average of `YearsatCompany`; represents company tenure, not total career experience. |

### Charts and Detailed Analysis

| Analysis | Visualization | Fields / aggregation |
|---|---|---|
| Attrition by department | Donut chart | Department and sum of attrition count. |
| Attrition by gender | Pie chart | Gender and count of nonblank attrition values; verify attrition-status filtering. |
| Age-group distribution | Column chart | Age group and count of nonblank age values. |
| Department workforce distribution | Funnel chart | Department and sum of employee count. |
| Attrition by experience | Line chart with area fill | Total experience in years and sum of attrition count. |
| Attrition by job role and satisfaction | Matrix | Job role, job satisfaction, and sum of attrition count. |
| Salary-slab comparison | Clustered bar chart | Employee ID count by salary slab, split by attrition status. |

### Interactive Filters

- **Department** slicer.
- **Age Group** slicer.

## Data Fields Referenced

The report visuals reference the table `HR_Analytics-4` and the following fields:

| Category | Fields |
|---|---|
| Employee identifiers and counts | `EmpID`, `EmployeeCount` |
| Demographics | `Age`, `AgeGroup`, `Gender` |
| Organization and role | `Department`, `JobRole` |
| Attrition | `Attrition`, `Attrition count`, `Attrition rate %` |
| Compensation grouping | `SalarySlab` |
| Tenure and experience | `YearsatCompany`, `TotalExperience(Years)` |
| Employee sentiment | `JobSatisfaction` |

**Data provenance:** The original dataset source, collection period, licensing terms, and preparation steps are not documented here. Confirm these details before redistributing the underlying data.

## Repository Structure

```text
hr-analytics-dashboard/
├── README.md
└── HR Analitics Dashboard.pbix
```

*
