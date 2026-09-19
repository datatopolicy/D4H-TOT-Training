# Wednesday, March 31 — Writing, Tables, Figures & Maps

> **Theme:** IMRAD structure, best practices for data visualization, creating maps in Excel.
> **Slide deck:** `assets/slides/TOT_Day3_Wednesday.pptx`
> **Template:** `assets/templates/Report_Template_IMRAD.docx`

---

## Day 2 Debrief

**9:00–9:30**

Quick poll on Tuesday's content. Targeted clarification only — PivotTable field-area confusion is the most common sticking point; have the drag-and-drop diagram ready.

Confirm every team has a populated objectives list and at least one calculated rate before the day's writing work begins.

---

## IMRAD Structure

**9:30–10:00**

| Section | Purpose |
|---|---|
| **Introduction** | Background and objectives: why this topic matters and what decision it informs |
| **Methods** | Data source, period, disaggregation approach, and a summary of cleaning decisions |
| **Results** | Findings organized by objective, each with a supporting table or chart, in plain language |
| **Discussion** | Interpretation, clearly separated from recommendations, plus limitations |

**Executive Summary vs. IMRAD body:** The Executive Summary uses an **inverted pyramid** (finding first); the IMRAD body uses a build-up structure. Both coexist in one report, at different sections.

📝 **Distribute now:** `assets/templates/Report_Template_IMRAD.docx` — teams begin populating it today.

> 🗂️ **Facilitator tip:** Contrast: "Today we'll learn IMRAD" (mechanics-first) vs. "Every one of you has had a busy colleague ask 'so what does this mean?' about a report — IMRAD is how you answer that before they even ask" (relevance-first).

---

*☕ Tea Break — 10:30–11:00*

---

## Best Practices for Creating Tables

**11:00–12:00**

**Publication-quality table checklist:**

- [ ] Specific title that **states the takeaway**, not just the variable name
- [ ] Rows in a **meaningful sort order** (e.g., rate descending, not alphabetical)
- [ ] **Sensible rounding** — rates to one decimal place; counts as whole numbers
- [ ] **Source and date footnote**
- [ ] **Small-numbers flag** preserved for any cell with fewer than 20 underlying events

**Common mistake:** Pasting an entire raw PivotTable as the "headline table."
**Fix:** Curate a top/bottom view or an aggregated version for the reader's actual decision need.

> 🗂️ **Facilitator tip:** Demonstrate Paste Special → Picture (or a linked table) for moving a finished table into Word without breaking its formatting.

---

## Tables Exercise

**12:00–12:30**

Each team builds their report's **headline summary table** from their own analysis, applying the five-point checklist above and inserting it into their `Report_Template_IMRAD.docx`.

---

*🍽️ Lunch — 13:00–14:00*

---

## Best Practices for Creating Figures

**14:00–14:30**

**Chart-type matching rule:**

| Finding type | Chart type |
|---|---|
| Trend over time | Line chart |
| Comparison across categories | Sorted bar chart (sorted by value, not alphabetically) |
| Part-to-whole (≤ 4 categories) | Stacked bar or pie |
| Part-to-whole (> 4 categories) | Stacked bar — never pie |
| Precise values a reader needs to look up | Table, not chart |
| Geographic distribution | Choropleth map |

**Publication-quality finishing touches:**
- Title states the **takeaway** (e.g., "Rural districts report mortality rates more than twice the urban rate") — written *before* building the chart
- Data labels shown **directly on bars or points**, not only via gridlines
- One **consistent, muted color palette** across all charts in the report
- No 3-D effects, no heavy gridlines, no unnecessary legends for a single series

---

## Figures Exercise

**15:00–15:30**

Each team builds **two charts** from their own findings:
1. A **line chart** for a trend-over-time finding
2. A **sorted bar chart** for a category-comparison finding

Teams self-score both charts against the five-point checklist, then swap with a neighboring team for a 5-minute peer critique.

---

## Creating Maps in Excel

**16:00–16:30**

**When a map helps:** geographic clustering or spread is itself the finding (cases concentrated along a border, a spatial gradient from urban centers outward).

**When a bar chart is better:** "District A higher than District B" with no spatial pattern — a sorted bar communicates the ranking more precisely than a color-shade comparison.

**Building a choropleth map:**
1. Insert → Charts → Maps → **Filled Map**
2. Administrative unit names must **exactly match** Excel/Bing's geographic name recognition (pre-test in advance)
3. Set **deliberate color-scale breakpoints** — don't accept the automatic default, which can visually overstate small differences
4. Always show **exact numeric values** alongside the map in a companion table

> 🗂️ **Facilitator tip:** Confirm venue internet connectivity — Map Chart requires it. Have a pre-built fallback map image per country ready as a backup.

---

*End of Day 3 → Tomorrow: report templates, recommendations, and sustained group-project drafting time*
