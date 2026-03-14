# Olympic Athlete Performance & Participation Analysis (Power BI)

## Project Overview

Analysed **120 years of Olympic history** using Power BI to understand
who competes, who wins, and which sports dominate medal counts.

Built an interactive dashboard with DAX measures and dynamic filters
across sport, country, year, and gender — enabling drill-down from
global trends to individual athlete performance.

Primary goal: identify whether rising female participation is
translating into proportional medal achievement, and which sports
and athletes drive the majority of Olympic medals.

---

## Dataset

| Column | Description |
|---|---|
| Unique ID | Unique identifier per athlete entry |
| Competitor Name | Athlete name |
| Sex | Male / Female |
| Nation Code | Country code (USA, IND, AUS etc.) |
| Year | Year of the Olympic Games |
| Season | Summer / Winter |
| Sport | Sport category (Swimming, Athletics etc.) |
| Event | Specific competition within the sport |
| Medal | Gold, Silver, Bronze, or Not Registered |

> Each row represents one athlete competing in one specific event
> in one specific Olympic year.

**Scope:** 116,776 competitors · 34,088 medals · 120 years of data

Source: Olympic athlete dataset — Kaggle

---

## Metrics Defined

| Metric | Definition |
|---|---|
| Total Competitors | Total athletes across all Olympics in the dataset |
| Total Medals | Count of Gold, Silver, and Bronze medals awarded |
| Medals by Sport | Medal volume per sport — identifies dominant disciplines |
| Medals by Competitor | Medal tally per athlete sorted descending |
| Medals by Year | Trend of medals awarded across Olympic cycles |
| Medals by Gender | Medal split between male and female athletes |
| Competitors by Gender | Participation distribution by gender over time |

---

## Key Findings

| Metric | Value | Interpretation |
|---|---|---|
| Total Competitors | **116,776+** | Full dataset scope across 120 years |
| Total Medals Awarded | **34,088+** | Combined Gold, Silver, Bronze count |
| Male Participation | **75.29%** | Dominant across most of Olympic history |
| Female Participation | **24.71%** | Rising significantly from the 1980s onward |
| Male Medal Share | **72.3%** | Mirrors participation distribution |
| Female Medal Share | **27.7%** | Improving but lagging participation growth |
| Top Sport by Medals | **Athletics** | Highest medal contribution in Olympic history |
| Second Sport | **Swimming** | Dominates Gold and Silver totals |
| Third Sport | **Gymnastics / Rowing** | Strong consistency across cycles |

---

### The Lag Effect

> Female participation has been rising since the 1980s — but the
> medal distribution tells a more nuanced story. Participation is
> growing faster than the performance gap is closing.

Breaking it down:

- **Participation gap:** 75.29% male vs 24.71% female
- **Medal gap:** 72.3% male vs 27.7% female
- **What this means:** Female athletes are slightly overperforming
  their participation share in medals — but the absolute gap
  remains large because 120 years of historical imbalance compounds

This suggests that sports infrastructure and competitive opportunity
for female athletes has **not kept pace with entry-level inclusion.**

---

### The Concentration Effect

> Athletics and Swimming together account for the **majority of all
> Olympic medals** — making them the two sports with the highest
> structural influence on any nation's overall medal count.

At the individual level:

> **Michael Phelps** has accumulated more total medals than most
> entire nations have across their full Olympic history.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard building and visualisation |
| **DAX** | Measures for medal share, gender ratios, trend calculations |
| **Power Query** | Data cleaning and type casting |

---

## Approach

1. Loaded raw Olympic dataset and cleaned in Power Query —
   handled null medals, cast Year to integer, standardised
   Sex column values
2. Built **star schema** — athlete fact table with sport, nation,
   and year as dimension references
3. Wrote **DAX measures** for:
   - Total Competitors
   - Total Medals (filtered to exclude Not Registered)
   - Gender participation percentage
   - Gender medal share percentage
4. Built interactive visuals with cross-filter enabled
5. Added slicers for Sport, Season, Nation Code, and Year
   to enable drill-down analysis

---

## Visuals Built

| Visual | What it answers |
|---|---|
| KPI cards | Total competitors and total medals at a glance |
| Stacked horizontal bar — medals by sport | Which sports dominate medal counts |
| Stacked bar — medals by competitor | Which athletes lead all-time tallies |
| Line chart — medals by year | How medal volume has changed across cycles |
| Gender split charts | Participation vs medal share side by side |
| Slicers | Filter entire dashboard by sport, year, nation, season |

---

## How to Use

1. Download the **PBIX file** from this repository
2. Open in **Power BI Desktop**
3. Use slicers to filter by sport, country, year, or season
4. Cross-filter by clicking any visual to drill into that segment
5. Hover over data points for exact values

---

## Key Takeaway

**Participation is rising. The performance gap is closing more
slowly than headline numbers suggest.**

Athletics and Swimming dominate Olympic medals structurally.
At the individual level, one athlete — **Michael Phelps** — has
accumulated more medals than most countries have in total.
