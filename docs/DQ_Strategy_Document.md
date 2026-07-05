# DQ Strategy Document — DQ_Delivery

**Author:** [your name]
**Project:** DQ_Delivery
**Last updated:** [date]
**Status:** Draft — In Progress

> This document is built incrementally throughout Course 1. Each module adds to a specific section.
> Do not delete the guiding questions — answer them inline, then remove the guidance text in italics once filled in.
> Mentor reviews this document in full at the Phase 1 → Phase 2 checkpoint (end of Block II).

---

## 1. Purpose & Scope

*Added in: Module 01 — The Modern Data Ecosystem*

### 1.1 Business Goal

*What is DQ_Delivery and what business problem does the data platform solve? Who uses the Operations Dashboard and what decisions does it support?*

[Your answer]

### 1.2 Data Sources in Scope

*List the three source systems and what each one provides. One line per source is enough at this stage*

| Source System | Format | Provides |
|---|---|---|
| CRM | | |
| OMS | | |
| PMS | | |

### 1.3 Project Team & DQE Responsibilities

*Who would realistically be on a team running this kind of pipeline (even if some roles are hypothetical for this training project)? What is the DQE specifically responsible for here — and what is explicitly NOT the DQE's job?*

[Your answer]

### 1.4 Definition of "Done"

*What does "this project's data quality work is done" mean? Be specific — not "all bugs fixed," but a real, testable definition for a DQE engagement.*

[Your answer]

---

## 2. Acronyms & Definitions

*Business and technical terms specific to this project. Add to this table as new terms appear in later modules — don't try to fill it all in now.*

| Term | Definition |
|---|---|
| DQE | Data Quality Engineer |
| STM | Source-to-Target Mapping |
| | |

---

## 3. Entry & Exit Criteria

*Added in: Module 05 — DQA vs DQ: Scope, Role & Lifecycle*

### 3.1 Entry Criteria

*Under what conditions does DQ testing start in this project? What needs to exist before you can begin (data availability, environment readiness, documentation)?*

[Your answer]

### 3.2 Exit Criteria

*Under what conditions is testing considered complete for a given scope (e.g., for Phase 1, or for a specific layer)? Include measurable acceptance thresholds where possible, not just "testing is finished."*

[Your answer]

### 3.3 Four Lines of Defense — Mapped to DQ_Delivery

*Map the four lines of defense (Pre-screening → Staging Gate → Standardized Gate → Curated/Dashboard validation) to the actual DQ_Delivery pipeline. What gets checked at each line?*

| Line of Defense | What It Checks in DQ_Delivery |
|---|---|
| Pre-screening | |
| Staging Gate | |
| Standardized Gate | |
| Curated / Dashboard validation | |

---

## 4. DQ Best Practices for This Project

*Added across Module 03 (Data Modeling), Module 04 (Medallion Architecture), Module 07 (Profiling)*

### 4.1 Pre-Screening Checks

*What do you check before any data even enters the pipeline? Reference your raw file inspection findings (Module 03) and physical model audit (Module 04).*

[Your answer]

### 4.2 Vital Checks by Dimension

*A short checklist — for each of the 6 DQ dimensions, name at least one vital check that applies to this project's data. Full detail goes in Section 7.*

[Your answer]

### 4.3 Reconciliation Approach

*How will you verify that numbers match across layers (staging → standardized → curated → dashboard)? Which tables/metrics are reconciliation priorities for DQ_Delivery?*

[Your answer]

### 4.4 Profiling Metrics to Track

*Which metrics will you track over time, and why? (e.g., row counts per layer, null rates per critical column, job run times once pipelines run on a schedule)*

[Your answer]

### 4.5 SCD Mapping

*Which tables in DQ_Delivery are candidates for Slowly Changing Dimension tracking? Which SCD type applies, and why?*

[Your answer]

### 4.6 Data Contracts

*What should a Data Contract define before data is accepted into the staging layer? Sketch the shape of a contract for one source (e.g., crm.customers_staging) — fields, types, required/optional, allowed values.*

[Your answer]

---

## 5. Testing Types & Levels

*Added in: Module 07*

*Which testing types apply to this project, and at what level? Map them to the Medallion-style layers in DQ_Delivery.*

| Testing Type | Level | Applies Where in DQ_Delivery |
|---|---|---|
| Unit | Single table/column | |
| Integration | Layer-to-layer | |
| Reconciliation | Cross-layer | |
| End-to-End | Source → Dashboard | |
| Regression | | |
| Smoke | | |

---

## 6. Test Data & Environment (TDM Strategy)

*Added in: Module 11 — Test Data Management*

### 6.1 PII Inventory

*List every field across the schema that qualifies as PII. Classify as Sensitive or Non-Sensitive.*

| Table | Field | PII Type |
|---|---|---|
| | | |

### 6.2 TDM Approach

*How will test data be handled for this project? Masking, synthetic generation, or both? Which fields need which approach?*

[Your answer]

### 6.3 Environment Notes

*Local Docker setup specifics relevant to testing — anything a future reader of this document needs to know to reproduce your test environment.*

[Your answer]

---

## 7. DQ Dimensions & Measurement Structure

*Added in: Module 06 — 6 Dimensions of Data Quality*

*For each dimension: a measurement formula and an acceptance threshold, grounded in actual DQ_Delivery tables/columns.*

| Dimension | Measurement Formula | Threshold | Example Column |
|---|---|---|---|
| Completeness | `null_rate = nulls / total_rows * 100` | | |
| Accuracy | | | |
| Consistency | | | |
| Timeliness | | | |
| Uniqueness | `duplicate_rate = duplicates / total_rows * 100` | | |
| Validity | | | |

---

## 8. Test Cases

*Added incrementally from Module 09 (STM analysis) through Module 15 (Regex & Validation). Minimum 15 test cases, each traceable to a business rule.*

| ID | Table | Column | DQ Dimension | Business Rule | Expected Result | Module |
|---|---|---|---|---|---|---|
| TC-001 | | | | | | |
| TC-002 | | | | | | |

*Add rows as test cases are designed. Each test case implemented in SQL or pytest should reference its ID (e.g., a comment `-- TC-014` in the SQL file).*

---

## Document History

| Date | Module | Change |
|---|---|---|
| | M01 | Initial draft — Section 1 |
