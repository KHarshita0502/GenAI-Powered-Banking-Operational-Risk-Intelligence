# GenAI-Powered Banking Operational Risk Intelligence

A 3-page Power BI dashboard that identifies, analyzes, and explains operational-risk exposure in banking, combining Python and Oracle SQL analysis with a controlled GenAI explanation layer.

> **Python finds it → SQL proves it → Power BI shows it → GenAI explains it.**



##  1. Project Overview

This project analyzes 2,147 banking operational-risk events to identify where financial exposure is concentrated, which event types and process areas contribute most to losses, and which individual events require further investigation.

The project combines Python, Oracle SQL, Power BI, and a controlled GenAI explanation layer.

Python and SQL establish the analytical evidence, Power BI presents the verified findings, and GenAI explains those findings in business language and supports investigation planning.

GenAI is used as an explanation layer, not as the source of truth for numerical calculations.



##  2. Business Problem & Objectives

### Business Problem

Banking operational-risk data can contain events across systems, technology, payments, digital services, fraud, and security-related areas.
Risk teams need to understand where financial exposure is concentrated, which event types contribute the most total loss, which process areas have higher financial exposure, which events have higher financial impact per occurrence, and what areas require further investigation.

### Objectives

* Quantify total and average financial exposure across event types and process areas.
* Analyze event frequency, severity, and OpVar.
* Identify major operational-risk patterns.
* Identify high-loss individual events.
* Validate important analytical findings using Oracle SQL.
* Build an interactive Power BI dashboard.
* Use GenAI to explain verified analytical findings.
* Generate investigation recommendations based on verified evidence.
* Demonstrate validation and correction of an incorrect AI-generated finding.
* Maintain human review over AI-generated recommendations.



##  3. Dataset & Data Quality

**Dataset:** Operational Risk Events Dataset

**Source:** Kaggle — Operational Risk Events Dataset by Ziya

The dataset contains 2,147 records and 12 columns covering event details, process areas, financial loss, frequency, severity, OpVar, and additional economic variables.

The main event types are System Failure, Data Breach, Tech Failure, Cyber-Fraud, and Phishing.

The main process areas are Retail Banking, ATM Network, E-Banking, Payments, and Online Services.

Data-quality checks were performed before analysis.

Missing values: 0

Duplicate rows: 0

The Date field contains both standard date values and `Synth-2022` entries. The parseable dates range from 2022-01-01 to 2023-12-31.

The dataset does not contain a free-text incident-description field, so the project does not use NLP or text-extraction analysis.

The dataset contains both observed and synthetically generated operational-risk events, which is considered when interpreting the results.



## 4. Analytical & Technical Workflow

The project follows an end-to-end analytical workflow:

Raw Data → Python Analysis → Oracle SQL Validation → Power BI → Verified Findings → GenAI Explanation → Analyst Review

Python was used for dataset inspection, data-quality checks, missing-value analysis, duplicate checks, date parsing, descriptive statistics, event-type analysis, process-area analysis, financial-loss analysis, frequency analysis, severity analysis, OpVar analysis, correlation analysis, high-loss event identification, and validation of key analytical findings.

Oracle SQL was used as an independent validation layer to cross-check important aggregations and analytical findings.

Power BI was used to create interactive dashboards for operational-risk monitoring, risk-driver analysis, financial-loss analysis, and verified findings.

DAX was used for KPI calculations, analytical measures, ranking logic, filtering behavior, and the controlled explanation content used on the GenAI page.

Excel was used for quick validation during development and was not treated as a separate project deliverable.



##  5. GenAI Layer & Responsible AI Design

### Why GenAI Was Used

The project does not use GenAI to replace the analytics.

Python and Oracle SQL establish the verified numerical findings, while Power BI presents the evidence.

GenAI is then used to bridge the gap between verified analytical findings and business interpretation.

It provides business explanations, explains why a finding matters, and suggests areas for further investigation.

For example, the analysis identifies that Phishing has an average loss per event of 161.86 kUSD. The GenAI layer can explain that Phishing has fewer incidents but a higher financial impact per event, making individual incidents important for focused risk review.

### Responsible AI Design

GenAI does not calculate authoritative dashboard metrics, access the raw database directly, modify the database, or make final risk decisions.

AI-generated recommendations are treated as investigation support and require analyst review.

### AI Validation & Correction

During development, an AI-generated statement incorrectly claimed that Phishing had the second-highest total financial loss among event types.

The statement was checked against the verified analytical results.

The corrected finding was that Phishing has the lowest total financial loss, at 40,789.80 kUSD, but the highest average loss per event, at 161.86 kUSD.

This demonstrates that AI-generated output must be validated against verified analytical evidence before presentation.



## 6. Dashboard Overview

The Power BI solution contains three pages.

### Page 1 — Operational Risk Command Center

The first page provides an overview of the operational-risk exposure.

KPIs include Total Risk Events, Total Financial Loss, Average Loss per Event, Average Severity, and Average OpVar.

The page includes Events by Event Type, Financial Loss by Event Type, Financial Loss by Process Area, Severity Distribution, and Financial Loss by Process Area × Event Type.

### Page 2 — Risk Driver & Loss Analysis

The second page focuses on identifying the major drivers of financial exposure.

KPIs include Largest Single Loss, Highest-Loss Process, Highest-Loss Event Type, and Most Frequent Event Type.

The page includes Frequency vs Financial Loss, Average Loss by Event Type, Loss Contribution by Process Area, Top 10 Highest-Loss Events, and Average Loss by Process Area.

Filters include Event Type, Process Area, Frequency, and Severity.

### Page 3 — GenAI Risk Intelligence

The third page acts as the GenAI interpretation layer.

It contains Verified Findings, supporting Evidence, a GenAI Insight Panel, AI Validation & Correction, and a Data & Model Transparency note.

The GenAI Insight Panel provides Business Explanation, Why It Matters, and Recommended Investigation based on the selected event type.

### Dashboard Screenshots

Page 1 — Operational Risk Command Center

Page 2 — Risk Driver & Loss Analysis

Page 3 — GenAI Risk Intelligence



##  7. Key Findings & Recommendations

### System Failure — Highest Total Loss

System Failure recorded 497 events with a total financial loss of 53,811.56 kUSD and an average loss of 108.27 kUSD per event.

System Failure has the highest aggregate financial loss among the five event types.

Recommendation: Review recurring system failures, identify high-impact loss patterns, and prioritize resilience improvements in affected areas.

### Retail Banking — Highest Process-Area Loss

Retail Banking recorded 507 events with a total financial loss of 53,743.59 kUSD and an average loss of 106.00 kUSD per event.

Retail Banking has the highest aggregate financial loss among the five process areas.

Recommendation: Review processes contributing to financial exposure and investigate areas where operational controls can be strengthened.

### Phishing — Highest Average Loss per Event

Phishing recorded 252 events with a total financial loss of 40,789.80 kUSD and an average loss of 161.86 kUSD per event.

Phishing has the lowest event count and lowest aggregate financial loss among the five event types, but the highest average loss per event.

Recommendation: Review high-loss phishing incidents and examine authentication and email-security controls.

### Largest Process × Event Loss

The largest observed process-area and event-type financial-loss combination was Retail Banking + System Failure, with 13,758.30 kUSD.

The analysis demonstrates that the highest aggregate exposure is not necessarily the same as the highest individual-event impact.



## 8. Tools & Skills

### Tools

Python
Oracle SQL / Oracle SQL Developer
Microsoft Power BI
Microsoft Excel
GenAI

### Skills

Data Cleaning
Data Quality Validation
Exploratory Data Analysis
Descriptive Statistics
SQL Analysis
Risk Analytics
Financial-Loss Analysis
Power BI
DAX
Data Visualization
KPI Development
Dashboard Design
Analytical Validation
GenAI Integration
Responsible AI
Business Interpretation
Evidence-Based Recommendations

### Core Project Principle

Python → Analysis

SQL → Validation

Power BI → Visualization



Analyst → Final Review


