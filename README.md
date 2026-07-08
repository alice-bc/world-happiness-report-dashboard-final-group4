# World Happiness Dashboard

An interactive dashboard built with Streamlit exploring the World Happiness Report dataset (2015–2024). The dashboard was built as a group project and covers three areas: happiness trends over time, country-level changes, and correlations between happiness and related indicators.

---

## Setup

**1. Clone the repository**

```bash
git clone <repo-url>
cd <repo-folder>
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Run the dashboard**

```bash
python -m streamlit run app.py
```

The dashboard will open automatically in your browser at `http://localhost:8501`.

> If `streamlit run app.py` does not work, use `python -m streamlit run app.py` instead.

---

## Dataset

The dashboard uses `happiness_report_standardized.csv`, which was produced by the cleaning notebook (`1_world_happiness_cleaning.ipynb`). Make sure this file is in the same folder as `app.py` before running.

Key columns used:

- `Happiness score` — Cantril Ladder score (0–10)
- `Country_Standardized` — ISO-standardized country names
- `Region_Standardized` — UN sub-region classification (e.g. Northern Europe, South-eastern Asia)
- `Geographic_Group` — continent-level grouping added during EDA
- `Year` — 2015 to 2024

---

## Dashboard Structure

**Sidebar (global filters)**
- World Region — filters all three sections
- Subregion — narrows down within the selected region

**Section 1 — Happiness Trends Over Time**
- Global average always shown as a baseline
- World Region and Subregion lines added when selected
- Optional country highlight via multiselect
- Year range slider

**Section 2 — Where Did Happiness Change the Most?**
- Compares countries between two selected years
- Bar chart showing biggest increases and decreases
- Indexed factor trend chart — click a bar to focus on a country
- Summary metric cards

**Section 3 — Correlation Explorer**
- Horizontal bar chart showing correlation of each variable with happiness score
- Scatter plot with selectable x and y axes
- Continent baseline trend line shown when a subregion is selected

---

## Dependencies

| Package | Version |
|---|---|
| streamlit | ≥ 1.35.0 |
| pandas | ≥ 2.0.0 |
| altair | ≥ 5.0.0 |
