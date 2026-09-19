# All Training Materials

All files live in the `assets/` folder of this repository. Download them directly from GitHub or via the GitBook attachments panel.

---

## 📊 PowerPoint Slide Decks — `assets/slides/`

One deck per training day, covering every timetabled session in agenda order. All decks use a consistent design system (navy/teal/gold palette, icon-reinforced content slides, agenda-at-a-glance opening, and a closing slide with the next day's preview).

| File | Day | Key Topics |
|---|---|---|
| `TOT_Day1_Monday.pptx` | Monday | Project introduction, equity principles, cleaning & combining data in Excel |
| `TOT_Day2_Tuesday.pptx` | Tuesday | Census-based rates, descriptive statistics, PivotTables |
| `TOT_Day3_Wednesday.pptx` | Wednesday | IMRAD structure, tables, figures, maps |
| `TOT_Day4_Thursday.pptx` | Thursday | Report templates, recommendations, training methodologies, group projects |
| `TOT_Day5_Friday.pptx` | Friday | Presentation guidance, certification, workshop evaluation |

---

## 📈 Excel Practice Workbooks — `assets/workbooks/`

All workbooks contain **live formulas** — edit any input and the sheet recalculates automatically. Every workbook includes an **Instructions** tab explaining the exercise sequence.

### `Mortality_Linelist_Practice.xlsx`
300-row simulated death record line list (District, Sex, Age, Cause Category, Month).  
**Sheets:** Line List Data · Descriptive Statistics · Frequency Tables · Instructions  
**Key formulas:** `AVERAGE`, `MEDIAN`, `MODE.SNGL`, `STDEV.S`, `QUARTILE.INC`, `AVERAGEIF`, `COUNTIFS`  
**Session:** Tuesday — Descriptive Statistics & PivotTables

### `Data_Cleaning_Practice.xlsx`
Deliberately messy dataset seeded with 15 duplicates, 4 sex-spelling variants (`M`, `m`, `Male`, `male`, `Femle`), 12 blank ages, and 3 implausible ages (negative or >120).  
**Sheets:** Dirty Data · Cleaning Formulas (live answer key) · Instructions  
**Key formulas:** `TRIM`, `PROPER`, `IFS`, `COUNTIFS` (994 live formulas)  
**Session:** Monday — Cleaning Data in Excel

### `Rates_and_Census_Practice.xlsx`
Event counts for 8 districts joined to a 2020 census population table via `INDEX/MATCH`; inter-censal growth calculation to estimate 2027 population; crude death rate per 1,000 and per 100,000.  
**Sheets:** Event Counts 2027 · Census Population · Rate Calculation · Instructions  
**Key formula:** `= Census Pop × (1 + Growth Rate) ^ (Analysis Year − Census Year)`  
**Session:** Tuesday — Census Data & Rates

### `Priority_Disease_5yr_District_Sex_Template.xlsx`
Fill-in template for Pre-TOT Deliverable 3. Yellow-highlighted input cells, one example row (delete before submitting), and a full data dictionary tab.  
**Sheets:** 5-Year Dataset Template · Data Dictionary  
**Session:** Pre-TOT Deliverable — due before Monday March 29

---

## 📄 Word Templates & Guides — `assets/templates/`

### `TOT_Facilitator_Guide_and_Lecture_Notes.docx`
Complete session-by-session facilitator guide for all five days. For every timetabled session:
- Learning objective
- Key lecture content (detailed)
- Facilitator tips & common pitfalls
- Materials reference

### `SOP_and_Data_Dictionary_Templates.docx`
Two-part template:
- **Part A** — Standard Operating Procedure for requesting and accessing data (fill-in form with step-by-step process, approval contact fields, and known-challenges section)
- **Part B** — Data dictionary table template (Variable / Definition / Valid Values / Source)

### `Report_Template_IMRAD.docx`
Eight-section IMRAD-structured report template with inline guidance notes:
1. Executive Summary
2. Background & Objectives
3. Data Sources & Methods
4. Results — Findings
5. Equity Considerations
6. Discussion — Interpretation & Limitations
7. Recommendations
8. Annexes

### `Pre_and_Post_TOT_Deliverables_Checklist.docx`
Tick-box checklist covering every Pre-TOT and Post-TOT deliverable, with team sign-off and CDC Foundation confirmation fields.

---

## Using These Files

### In the Workshop
Materials are used in the order shown in each day's agenda. Participants open workbooks directly from their laptops; slide decks are projected from the facilitator's laptop.

### After the Workshop (Phase 6 Reproducibility)
The Excel workbooks are designed to be converted into **master workbooks** — separating raw data, cleaning logic, and output tabs so that a new reporting period's data can be pasted in and the output refreshes automatically. See the [Thursday session notes](sessions/thursday.md) for the reproducibility workflow.
