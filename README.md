
# The Digital Divide: Access, Opportunity, and the Path Forward (Shiny Dashboard)

**Course:** Data Visualisation & Communications (RMIT)
**Project Type:** Individual Project (Interactive Storytelling Dashboard)
**Tech:** R, Shiny, flexdashboard / RMarkdown, tidyverse
**Live App:** [https://qqptxa-sowmiya-kumar.shinyapps.io/Data_Vis_A3_s4040536/](https://qqptxa-sowmiya-kumar.shinyapps.io/Data_Vis_A3_s4040536/)

---

## Project Overview

This project is a **narrative-driven, multi-tab Shiny dashboard** that explores the **global digital divide**—who has internet access, who is left behind, and how internet access relates to **economic opportunity**, **education**, and **employment outcomes**.

The dashboard is designed to fit on a single HD screen per tab (no scrolling) and combines **data visualisation, storytelling, and interpretation** into a deployable product.

---

## Key Questions

1. **Access & Inequality:** Which countries and regions remain digitally excluded?
2. **Change Over Time:** Are regions closing the gap (2010–2022), or falling further behind?
3. **Opportunity Link:** How does internet access relate to GDP per capita, literacy, tertiary education, and employment?
4. **Actionable Insight:** What patterns are consistent across datasets, and what trade-offs/limitations exist?

---

## Dashboard Structure

### Tab 1 — The Digital Divide Reality

* Global internet penetration (choropleth map)
* Top/bottom “digital extremes” comparison
* Regional progress trends over time (time series)

### Tab 2 — Digital Access = Economic Opportunity

* Internet access vs GDP per capita (relationship view)
* Internet access vs education metrics (literacy / tertiary)
* Internet access vs employment outcomes (employment-to-pop ratio)
* Income-group lens to contextualize inequality (World Bank income groups)

### Tab 3 — Inference & References

* Plain-language findings and interpretation
* Evidence caveats (data gaps, comparability limits)
* Full dataset references

---

## Datasets

This project integrates multiple open datasets (CSV format):

* `employment_to_pop_ratio.csv`
* `GDP_Per_capita.csv`
* `Individuals_using_internet.csv`
* `literacy_rate_age_ab_15.csv`
* `tertiary_ed_enrollment.csv`
* `world-bank-income-groups.csv`

These are sourced from reputable public sources such as **World Bank Open Data** and **Our World in Data**, with references documented inside the dashboard.

---

## Methods Summary

* Data wrangling and standardisation across datasets (country names/IDs, year alignment)
* Feature engineering for:

  * regional summaries
  * top/bottom comparisons
  * trend lines over time
  * grouped views by income level
* Visual encoding choices optimised for:

  * clarity at a glance
  * consistent axes and labels
  * reduced cognitive load for mixed audiences
* Storytelling approach:

  * structured narrative flow (reality → drivers/opportunity → inference)
  * annotations and explanatory text to guide non-technical users

---

## Results Highlights

Key insights demonstrated in the dashboard:

* A persistent global access gap remains, with the lowest connectivity concentrated in specific regions.
* Regions show unequal improvement rates; some “catch-up” trends exist but are not uniform.
* Internet access shows a clear relationship with economic/education indicators, but strength varies by region and income group.
* The dashboard provides a stakeholder-friendly interpretation layer, not just charts.

---

## Repository Structure

```
.
├── data/
│   ├── employment_to_pop_ratio.csv
│   ├── GDP_Per_capita.csv
│   ├── Individuals_using_internet.csv
│   ├── literacy_rate_age_ab_15.csv
│   ├── tertiary_ed_enrollment.csv
│   └── world-bank-income-groups.csv
│
├── app/
│   └── GlobalDgitalDivide.Rmd        # rmd file
│
├── README.md

```



---

## How to Run Locally


1. Open the `.Rmd` in RStudio.
2. Install packages (once).
3. Click **Run Document**.


Packages to install from the project root:

```r
install.packages(c(
  "shiny", "flexdashboard", "rmarkdown",
  "tidyverse", "plotly", "readr", "dplyr", "countrycode",
  "janitor", "DT"
))

rmarkdown::run("GlobalDigitalDivide.Rmd")
```

---

## Deployment

The live version is deployed on **shinyapps.io**:

**Live App:** [https://qqptxa-sowmiya-kumar.shinyapps.io/Data_Vis_A3_s4040536/](https://qqptxa-sowmiya-kumar.shinyapps.io/Data_Vis_A3_s4040536/)

---

## Notes on Data Use

All datasets are open/public. This repository is intended for **portfolio demonstration and academic purposes**.

---

## References

Primary sources used include:

* **World Bank Open Data**
* **Our World in Data**

(Full citation details are included inside the dashboard’s “Inference & References” tab.)



