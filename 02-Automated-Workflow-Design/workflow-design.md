
# Automated & AI-Augmented BIM Workflow Design
## Clash Detection & Coordination

## 1. Overview of the Redesigned Workflow

The proposed automated workflow eliminates manual triggers and 
repetitive coordination tasks by introducing three layers of 
intelligence: rule-based automation, parametric logic, and 
AI-assisted decision support.

---

## 2. Workflow Stages

### Stage 1 — Automated Model Monitoring (Trigger Layer)
**Tool:** BIM 360 / ACC API + Python script

- A scheduled Python script monitors the BIM 360 project folder 
  every 24 hours for new model versions
- When a new upload is detected, the script automatically:
  - Logs the upload timestamp and discipline
  - Triggers the clash detection pipeline
  - Sends an automated notification to the BIM coordinator

**Replaces:** Manual model checking and manual clash test initiation

---

### Stage 2 — Rule-Based Clash Test Execution (Automation Layer)
**Tool:** Navisworks API / BIM 360 Model Coordination

- Pre-configured clash test sets run automatically across all 
  discipline pairs:
  - Architecture vs Structure
  - Structure vs MEP
  - Architecture vs MEP
  - MEP internal (ductwork vs pipework vs cable trays)
- Clash tolerance rules are parametrically defined:
  - Hard clash threshold: 0mm clearance
  - Soft clash threshold: defined per system (e.g. 50mm for MEP)
- Approved clash exceptions (e.g. sleeved penetrations) are stored 
  in a rule database and automatically filtered out

**Replaces:** Manual test configuration and manual exception review

---

### Stage 3 — AI-Assisted Clash Classification (Intelligence Layer)
**Tool:** Machine Learning classifier (Python / scikit-learn)

- A trained ML model classifies each clash by:
  - **Severity:** Critical / Major / Minor
  - **Type:** Hard clash / Soft clash / Duplicate / Acceptable
  - **Responsible discipline:** Auto-assigned based on element 
    ownership rules
- The model is trained on historical clash data from previous 
  project cycles
- Clashes classified as Acceptable are automatically closed with 
  a documented reason
- Critical clashes are flagged and escalated immediately

**Replaces:** Manual clash inspection, manual grouping, 
manual severity assessment

---

### Stage 4 — Automated Issue Assignment (Integration Layer)
**Tool:** BCF API + Autodesk Construction Cloud

- Classified clashes are automatically pushed to the project 
  management system as BCF issues
- Each issue includes:
  - Clash severity and type
  - Responsible discipline and element IDs
  - Suggested resolution approach (AI-generated)
  - Due date based on coordination cycle schedule
- Responsible discipline teams receive automated notifications

**Replaces:** Manual BCF export, manual email assignment, 
manual spreadsheet tracking

---

### Stage 5 — Automated Reporting (Output Layer)
**Tool:** Python (pandas + reportlab) / Power BI

- At the end of each coordination cycle a report is 
  automatically generated containing:
  - Total clashes detected vs resolved
  - Clash breakdown by discipline pair and severity
  - Trend analysis comparing current vs previous cycles
  - Outstanding critical issues requiring coordinator attention
- Report is distributed automatically to stakeholders via email

**Replaces:** Manual report compilation and formatting

---

## 3. Data Inputs

| Input | Source | Format |
|---|---|---|
| Discipline BIM models | BIM 360 project folders | .rvt / .ifc |
| Clash tolerance rules | BIM Execution Plan | Rule database |
| Approved exceptions | Previous coordination logs | JSON |
| Historical clash data | Past project archives | CSV / JSON |
| Project schedule | Construction programme | XML / JSON |

---

## 4. Automation Logic Summary

| Process | Automation Type | Tool |
|---|---|---|
| Model version monitoring | Scheduled script | Python + BIM 360 API |
| Clash test execution | Rule-based automation | Navisworks API |
| Clash classification | ML classification | scikit-learn |
| Issue assignment | API integration | BCF + ACC API |
| Report generation | Scripted output | Python + Power BI |

---

## 5. AI Integration Points

1. **Clash severity classification** — supervised ML model trained 
   on labelled historical clash data
2. **Responsible discipline prediction** — rule-based logic 
   combined with element ownership metadata
3. **Resolution suggestion** — NLP-based system recommending 
   standard solutions for recurring clash types
4. **Trend analysis** — pattern recognition identifying 
   design teams producing recurring clash categories
