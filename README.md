# COVID-19 Healthcare Impact & Vaccination Analysis – Australia (2020–2022)

**Domain:** Healthcare Analytics / Public Sector Intelligence
p

**Tools:** Power BI, DAX, Power Query

**Duration:** 2–3 Weeks
**Dataset:** Public Australian COVID-19 reporting data (2020–2022), educational use

---

## Overview

This project analyses the progression of COVID-19 across Australian states between 2020 and 2022, focusing on healthcare strain and vaccination impact.

Rather than reporting raw case counts, the dashboard evaluates:

The dashboard answers:

- When outbreak severity peaked
- Which states experienced the highest healthcare pressure
- How hospitalisations, ICU admissions, and ventilations tracked case growth
- Whether vaccination rollout corresponded with reduced mortality trends

The dashboard transforms epidemiological data into structured, state-level decision intelligence.

---

## Business Problem

During the pandemic, daily case numbers were widely reported, but there was limited structured analysis answering key operational questions:

- Which states faced the greatest strain on healthcare infrastructure?
- How closely did ICU and ventilation demand track case growth?
- When did severity indicators peak?
- Did vaccination rollout reduce mortality impact?

Public health decision-makers required a consolidated analytical view to monitor healthcare capacity and evaluate intervention timing.

The objective of this project was to build an interactive Power BI dashboard that quantifies outbreak severity, healthcare pressure, and vaccination progression across Australian states.

---

## Data & Model Design

### Data

The dataset includes:
- Confirmed cases
- Deaths
- Hospitalisations
- ICU admissions
- Ventilations
- Vaccination doses
- Date and State attributes

Data cleaning and transformation were performed in Power Query:
- Corrected invalid data types
- Standardised column naming
- Replaced missing values where appropriate
- Created calculated date fields (Year, Month Name, Month Number) for time-based analysis

All data used is public and contains no sensitive personal information.

### Model Design

A simplified star schema model was implemented:

- Fact Table: COVID metrics (cases, deaths, hospitalisations, ICU, ventilations, vaccinations)
- Dimension Table: State

The model enables accurate aggregation and interactive filtering across:
- Year
- Month
- State

This structure supports time-series analysis and cross-visual drill-down.

---

## Key Measures (DAX)

```DAX


```

These measures shift the focus from churn percentage to **expected revenue exposure**.

---

## Analysis & Insights

COVID-19 progression in Australia followed a clear structural pattern.

Late 2021 to 2022 marked the most significant outbreak wave, particularly in New South Wales and Victoria. Case growth accelerated sharply compared to earlier containment phases.

Healthcare strain closely tracked case surges. ICU admissions and ventilations moved in parallel with confirmed cases, indicating consistent severity ratios during peak transmission periods.

Despite substantial increases in total cases during 2022, the mortality rate growth was comparatively moderated. This divergence suggests improved clinical management and/or vaccination impact, reducing severe outcomes.

Vaccination rollout accelerated significantly from mid-2021 onward. States with higher vaccination volumes demonstrated stabilisation in mortality trends despite continued transmission.

Overall, the data shows a transition from containment-driven waves to high-transmission but comparatively lower fatality phases.

---

## Business Impact

This dashboard simulates public-sector healthcare intelligence use cases.

If deployed within a government or health department environment, the analysis would support:

- Healthcare capacity monitoring (ICU and ventilation demand forecasting)
- Resource allocation across states
- Early detection of strain escalation
- Vaccination policy evaluation

The project shifts reporting from raw case counts to system pressure monitoring.

Rather than reacting solely to transmission levels, decision-makers can monitor leading severity indicators to trigger timely interventions.

---

## Repository Structure

```
/covid-australia-healthcare-analysis/
│
├── Reports/
│   ├── COVID_Healthcare_Dashboard.pbix
│   └── Dashboard_Screenshots/
│
├── Data/
│   └── Australia_Covid-19.xlsx
│
├── Writeups/
│   └── Project_Case_Study.pdf
│
└── README.md
```

---

## Dashboard Preview  


---

## Assumptions & Limitations

- Missing values were treated as zero where no data was recorded.
- Interstate comparisons are based on absolute values; per-capita normalisation was not included.
- Demographic variables (age, gender) were not available.
- The analysis is descriptive and does not include predictive modelling.
- Correlations observed do not imply causal relationships.

---

## Skills Demonstrated

- Data cleaning and transformation (Power Query)
- Time-series modelling
- Star schema data modelling
- Healthcare KPI design
- DAX measure development
- Interactive dashboard design
- Public sector analytics storytelling

---

## Contact

For questions or discussion regarding this project:

www.linkedin.com/in/ismailarshad  
m.ismailasrhadd@gmail.com
