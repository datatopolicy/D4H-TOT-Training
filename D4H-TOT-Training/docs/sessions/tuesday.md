# Tuesday, March 30 — Statistics & Rates

> **Theme:** Descriptive statistics, census-based rates, and PivotTables.
> **Slide deck:** `assets/slides/TOT_Day2_Tuesday.pptx`
> **Practice files:** `assets/workbooks/Mortality_Linelist_Practice.xlsx` · `assets/workbooks/Rates_and_Census_Practice.xlsx`

---

## Day 1 Debrief

**9:00–9:30**

Quick poll: one thing that clicked yesterday, one thing still unclear. Address the two or three most common unclear points as a targeted refresher — not a full re-teach.

> 🗂️ **Facilitator tip:** PivotTable field-area confusion from Monday sometimes surfaces here early. Have the drag-and-drop diagram ready.

---

## Training Methodologies

**9:30–10:00**

Adult learners respond to **relevance-first framing**, not mechanics-first framing. The foundational teaching sequence for any technical skill:

| Stage | What happens |
|---|---|
| **I do** | Trainer demonstrates the full skill once, narrating every click and decision aloud. |
| **We do** | Trainer and participants perform the same task together, trainer pausing after each step to check screens. |
| **You do** | Participants complete an equivalent task independently on a new dataset; trainer circulates. |

**Reading the room:** three observable signs of confusion — leaning back from the screen · side conversations in a different language · note-taking that stops — and the corresponding trainer response for each.

> 🗂️ **Facilitator tip:** Ask for a show of hands on prior training experience to surface informal co-facilitators for later peer-teaching moments.

---

*☕ Tea Break — 10:30–11:00*

---

## Accessing and Using Census Data to Calculate Rates in Excel

**11:00–11:30**

**Why rates, not counts:** District A with 200 deaths and District B with 100 deaths doesn't mean District A has a worse situation if District A's population is four times larger.

**Inter-censal adjustment formula:**

```excel
Estimated Population =
  Census Population × (1 + annual growth rate) ^ (analysis year − census year)

' In Excel:
=CensusPop * (1 + GrowthRate) ^ (AnalysisYear - CensusYear)
```

**Rate formula:**

```excel
Rate = (Number of events ÷ Estimated Population) × Multiplier
' Crude death rate per 1,000:
=(D2/E2)*1000
```

**Choosing the multiplier:**
- Per **1,000** — crude death/birth rates (common events)
- Per **100,000** — rarer events (e.g., maternal mortality)
- Per **100 (%)** — immunization coverage

📊 **Practice file:** `assets/workbooks/Rates_and_Census_Practice.xlsx`

> 🗂️ **Facilitator tip:** Pre-test each country's administrative unit names against the census lookup table in advance — name mismatches are the most common lookup failure.

---

## Descriptive Statistics Review

**12:00–12:30**

Quick recap of mean, median, mode, standard deviation, and quartiles.

**Key insight:** Mortality and case-count data are frequently **right-skewed** (a small number of high-burden districts or extreme ages). The median and IQR are usually more representative than the mean and standard deviation for headline reporting.

Use a cold-call format ("why would you use median here?") rather than lecture — this is review, not new content.

---

*🍽️ Lunch — 13:00–14:00*

---

## Descriptive Statistics Using Excel

**14:00–14:30**

**Core functions:**

```excel
=AVERAGE(range)          ' mean
=MEDIAN(range)           ' median
=MODE.SNGL(range)        ' most frequent value
=STDEV.S(range)          ' sample standard deviation
=QUARTILE.INC(range,1)   ' first quartile (Q1)
=QUARTILE.INC(range,3)   ' third quartile (Q3)
=AVERAGEIF(range,"criteria",avg_range)   ' conditional mean
=AVERAGEIFS(...)         ' multi-criteria conditional mean
```

**Exercise:** Using `Mortality_Linelist_Practice.xlsx`, calculate mean and median age at death by Cause Category. Identify which category shows the largest mean–median gap and explain why (skew from a small number of very young or very old deaths).

📊 **Practice file:** `assets/workbooks/Mortality_Linelist_Practice.xlsx` — sheet: `Descriptive Statistics`

> 🗂️ **Facilitator tip:** Have participants predict which category will show the largest mean–median gap before calculating — this builds genuine statistical intuition rather than mechanical formula-entry.

---

## Data Analysis Using Pivot Tables

**15:00–15:30**

**Four PivotTable areas:**

| Area | What to drag here |
|---|---|
| **Rows** | Your primary category (e.g., District) |
| **Columns** | Your secondary category (e.g., Sex) |
| **Values** | Your measure (e.g., CaseID → Count) |
| **Filters** | Any dimension to filter the whole table |

**The key step participants most often miss:** After dragging a field to Values, right-click → **Value Field Settings** → choose `Count`, `Average`, `Sum`, etc. The default is Count of text, Sum of numbers — verify it is what you intended.

**Exercise:** Build a District × Sex two-way table from `Mortality_Linelist_Practice.xlsx` and cross-check against the COUNTIFS formula table on the `Frequency Tables` sheet.

> 🗂️ **Facilitator tip:** Demonstrate right-clicking into Value Field Settings live, prominently — this is the most common PivotTable confusion point.

---

## Teams Analyze Data

**16:00–17:00**

Teams apply today's rate-calculation and PivotTable skills to their own priority-topic dataset.

**Checkpoint before you leave today:**
- [ ] At least one PivotTable-based frequency table for your own topic
- [ ] At least one calculated rate using your own event data and census population

> 🗂️ **Facilitator tip:** Flag any team still blocked on data access — this becomes a Thursday check-in priority.

---

*End of Day 2 → Tomorrow: IMRAD structure, tables, figures, and maps*
