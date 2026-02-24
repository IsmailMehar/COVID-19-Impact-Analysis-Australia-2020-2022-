COVID-19 Impact & Healthcare Strain Analysis – Australia (2020–2022)

Domain: Healthcare Analytics / Public Sector Intelligence
Tools: Power BI, DAX, Power Query
Duration: 2 Weeks
Dataset: Public Australian COVID-19 reporting data (educational use)

Overview

This project analyses the progression of COVID-19 across Australian states between 2020 and 2022, focusing on healthcare system strain and vaccination impact.

Rather than reporting case counts in isolation, the analysis links:

Case growth

Hospitalisations

ICU admissions

Ventilation demand

Mortality rate

Vaccination rollout

The dashboard answers:

When did outbreak severity peak across states?

How closely did ICU and ventilation demand track case surges?

Which states experienced the highest healthcare pressure?

Did vaccination rollout correspond with reduced mortality trends?

Business Problem

During the pandemic, daily case numbers were widely available, but operational healthcare insights were fragmented.

Decision-makers required clarity on:

The timing and magnitude of healthcare system strain

Interstate comparisons of outbreak severity

The relationship between transmission growth and ICU demand

Whether vaccination rollout correlated with reduced fatality impact

The objective of this project was to consolidate multi-metric COVID data into a structured, interactive dashboard that supports healthcare capacity monitoring and state-level comparison.

Data & Model Design
Data

The dataset included daily state-level metrics:

Confirmed cases

Deaths

Hospitalisations

ICU admissions

Ventilations

Vaccination doses

Data preparation steps included:

Handling missing values

Correcting invalid data types

Standardising column names

Creating time intelligence fields (Year, Month, Month Name)

All transformations were completed in Power Query.

Model Design

A simplified star schema was implemented:

Fact Table: COVID daily metrics

Dimension Table: State reference table

Time-based filtering was enabled through calculated date attributes.

Interactive slicers allow filtering by:

State

Year

Month

This structure ensures correct aggregation and filter propagation across visuals.

Key Measures (DAX)
-- Total Cases
Total Cases =
SUM ( Covid[Cases] )

-- Total Deaths
Total Deaths =
SUM ( Covid[Deaths] )

-- Mortality Rate
Mortality Rate =
DIVIDE ( [Total Deaths], [Total Cases] )

-- Total Hospitalisations
Total Hospitalisations =
SUM ( Covid[Hospitalisations] )

-- Total ICU Admissions
Total ICU Admissions =
SUM ( Covid[ICU] )

-- Total Ventilations
Total Ventilations =
SUM ( Covid[Ventilations] )

-- Total Vaccinations
Total Vaccinations =
SUM ( Covid[Vaccinations] )

-- Average Daily Cases
Average Daily Cases =
AVERAGE ( Covid[Cases] )

-- Peak Daily Cases
Peak Daily Cases =
MAX ( Covid[Cases] )

These measures shift the focus from raw reporting to healthcare strain and severity analysis.

Analysis & Insights

COVID progression in Australia followed clear structural phases.

Outbreak severity accelerated sharply in late 2021 and into 2022, particularly in New South Wales and Victoria. Earlier waves showed lower sustained transmission levels.

Healthcare strain closely tracked case growth. ICU admissions and ventilation demand moved in near parallel with case surges, indicating consistent severity proportions during peak transmission periods.

Despite significant case increases in 2022, mortality rate growth did not rise proportionally. This divergence suggests improved treatment protocols and/or vaccination impact mitigating fatality outcomes.

Vaccination rollout accelerated from mid-2021 onwards. States with higher vaccination volumes showed stabilised mortality patterns despite ongoing transmission waves.

The analysis demonstrates that monitoring case growth alone is insufficient — healthcare capacity indicators provide earlier and more operationally meaningful signals of system pressure.

Business Impact

This project transforms epidemiological data into healthcare system intelligence.

If deployed in a public health setting, it would support:

ICU and ventilation capacity planning

Early detection of healthcare strain escalation

Interstate performance comparison

Vaccination impact evaluation

Policy trigger monitoring

Rather than reacting to case counts alone, decision-makers can monitor leading indicators such as hospitalisation growth and ICU utilisation to initiate earlier interventions.

The dashboard shifts reporting from descriptive case tracking to operational capacity insight.

Repository Structure
/covid-australia-healthcare-analysis/
│
├── Reports/
│   ├── COVID_Healthcare_Dashboard.pbix
│   └── Dashboard_Screenshots/
│
├── Data/
│   └── Cleaned_Sample_Data.xlsx
│
├── Writeups/
│   └── Project_Case_Study.pdf
│
└── README.md
Dashboard Preview

Add dashboard screenshots here

Recommended screenshots:

Executive Overview page

State comparison view

ICU vs Ventilation trend chart

Vaccination rollout analysis

Assumptions & Limitations

Missing values were treated as zero where data was not recorded.

Absolute values were used; per-capita normalisation was not applied.

Demographic variables (age, risk groups) were not included.

Analysis is descriptive and does not include predictive modelling.

External policy variables (lockdowns, variant type) were not incorporated.

Skills Demonstrated

Public sector KPI modelling

Time-series analysis in Power BI

Star schema design

Healthcare capacity analytics

DAX measure design

Multi-metric correlation analysis

Executive-level dashboard storytelling

Interactive filtering & drill-down design

Contact

For discussion or questions regarding this project:

www.linkedin.com/in/ismailarshad

m.ismailasrhadd@gmail.com
