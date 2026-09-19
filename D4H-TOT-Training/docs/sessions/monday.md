# Monday, March 29 — Foundations

> **Theme:** Understanding the project, health equity, and cleaning data in Excel.
> **Slide deck:** `assets/slides/TOT_Day1_Monday.pptx`
> **Practice file:** `assets/workbooks/Data_Cleaning_Practice.xlsx`

---

## Welcome and Introductions

**9:00–9:30**

Round-robin introductions (name, agency, one hope for the week). Room norms set. The week's theme arc is previewed without going into the full schedule.

> 🗂️ **Facilitator tip:** Keep introductions to 30 seconds each with a visible timer. Note names and agencies — you'll use them for cold-calling and pairing decisions all week.

---

## Introduction to the D4H Data Analysis Project

**9:30–10:00**

- **Goal:** strengthen government agencies' analytical and reporting capacity for surveillance and mortality data, including CRVS data.
- **Six principles:** government-platform publication · government-led question setting · Excel-based descriptive analytics · health equity · government data ownership · SOP-based institutionalization.
- **Seven-phase arc** from this week's TOT through recurring, institutionalized reporting.
- **Objective 8:** building an in-country trainer cadre is what sustains the project after CDC Foundation's direct involvement ends.

> 🗂️ **Facilitator tip:** State the government data-ownership principle early and clearly — it shapes every data-handling decision the rest of the week.

---

## Review the TOT Schedule and Team Project

**10:00–10:30**

Walk through the Monday–Friday schedule. Introduce the **team project**: each country team uses their own Pre-TOT dataset (priority disease/condition, five years, by district and sex) to practice every skill taught this week, building toward a real report presented Friday.

📋 **Handout:** `assets/templates/Pre_and_Post_TOT_Deliverables_Checklist.docx`

> 🗂️ **Facilitator tip:** If a team has not completed a Pre-TOT deliverable, flag it for a lunchtime catch-up. Let them proceed with generic practice datasets in the meantime.

---

*☕ Tea Break — 10:30–11:00*

---

## Principles of Equity

**11:00–11:30**

**Operational definition:** Results broken down by sex, location, and an available socioeconomic proxy — so a policymaker sees *who* is most affected, not only an average.

**Three standard disaggregation dimensions:** Sex · Location (district/urban/rural) · SES proxy (where available).

**Small-numbers rule:** Flag any cell with fewer than 20 underlying events as *"interpret with caution"* — do not compute a rate for it.

**Framing:** Present equity findings as targeting information for resource allocation, never as a performance judgment.

---

## Group Projects: Country Teams Report on SOPs and Data-Access Challenges

**11:30–12:30**

Each country team presents (5 minutes) their Pre-TOT data-source inventory: sources, department/institution, timeliness/quality, known access challenges. Facilitator records cross-country patterns on a flip chart.

Each team identifies one SOP gap to close by Friday.

> 🗂️ **Facilitator tip:** Enforce the 5-minute limit strictly. Save deep troubleshooting for a side conversation at lunch.

---

*🍽️ Lunch — 13:00–14:00*

---

## Establish Data Analysis Objectives

**13:30–14:30**

A good objective is **specific and answerable**: you can say exactly what analysis would answer it and what the result would look like (a specific table or chart).

| ❌ Weak | ✅ Strong |
|---|---|
| "Analyze malaria." | "Identify whether rural districts show a higher malaria rate than urban districts, to target outreach resources." |

Each team drafts 2–4 objectives for their priority topic, each tracing back to a real government decision or bulletin.

> 🗂️ **Facilitator tip:** Apply the "specific and answerable" test to the first team's draft live as a model before releasing all teams.

---

## Cleaning Data in Excel

**14:30–15:30**

**Four classic dirty-data problems:** duplicate records · inconsistent category spelling · blank cells · out-of-range values.

**Core functions:**

```excel
=TRIM(A2)                          ' removes extra spaces
=PROPER(A2)                        ' standardizes capitalization
=SUBSTITUTE(A2,"Femle","Female")   ' fixes a known misspelling
=IFS(A2<0,"Invalid",A2>120,"Invalid",TRUE,"Valid")
=COUNTIFS($B$2:$B$200,B2,$C$2:$C$200,C2)>1   ' duplicate flag
```

**Key principle:** Flag problems in a new column — never silently delete a row. This preserves the audit trail.

📊 **Practice file:** `assets/workbooks/Data_Cleaning_Practice.xlsx`

---

## Combining Data Sets in Excel / Teams Analyze Data

**16:00–17:00**

INDEX/MATCH is the standard join method — more resilient than VLOOKUP to column reordering.

```excel
=INDEX(PopCol, MATCH(DistrictName, DistrictCol, 0))
```

> ⚠️ Always include the exact-match `0` argument in MATCH — omitting it is the most common silent lookup error.

Teams spend the remainder applying today's skills to their own five-year priority-topic dataset.

📊 **Reference:** `assets/workbooks/Rates_and_Census_Practice.xlsx`

---

*End of Day 1 → Tomorrow: descriptive statistics, census-based rates, and PivotTables*
