# Behavioral Science Portfolio

A portfolio of behavioral data science projects at the intersection of bioinformatics, psychology, and public health, built in R.

The work is organized around one question: **what keeps people stuck, and what helps them move forward?** Each project looks at that question from a different angle, from social and behavioral context to biology and development.

**Author:** Maliha Arshad, Bioinformatics Scientist

---

## Featured Project: Roots and Resilience

**Socioeconomic and behavioral patterns in depressive symptoms, and what looks protective**

An exploratory analysis of NHANES data asking which socioeconomic and behavioral factors track with depression severity, and which look protective. This is Project 1 of a connected series on family adversity, trauma, and resilience. It establishes the social and behavioral baseline that later projects build on with biological and developmental data.

| | |
|---|---|
| **Status** | Complete |
| **Data source** | NHANES, via the `NHANES` R package |
| **Language** | R (R Markdown) |
| **Report** | [View the rendered analysis](https://arshad-maliha.github.io/behavioral-science-portfolio/roots_and_resilience.html) |
| **Code** | [`roots_and_resilience.Rmd`](roots_and_resilience.Rmd) |

### Research question

What socioeconomic and behavioral factors predict depression severity in adults, and what looks protective?

### Data

- **Source:** National Health and Nutrition Examination Survey (NHANES), CDC National Center for Health Statistics, accessed through the `NHANES` R package.
- **Size:** 10,000 rows and 76 variables. The depression item is answered by about two-thirds of the sample, so the analysis uses those complete responses.
- **Outcome:** `Depressed`, self-reported frequency of feeling down, depressed, or hopeless (None, Several days, or Most days).
- **Factors examined:** `Poverty` (income-to-poverty ratio), `HHIncomeMid` (household income), `SleepTrouble`, `PhysActive`, `Gender`, and `Age`.

### Methods

- Data exploration and summary statistics with `skimr`
- Visualization with `ggplot2`: bar charts, boxplots, and proportional stacked bars comparing each factor across depression severity
- Correlation matrix and heatmap (`reshape2`) summarizing how the factors relate to depression severity

### Key findings

1. **Poverty and depression move together.** Median poverty index falls as depression severity rises, from roughly 3.3 in the "None" group to roughly 1.4 in the "Most days" group.
2. **Sleep trouble scales with severity.** About 20% of the "None" group report sleep trouble versus more than half of the "Most days" group.
3. **Physical activity looks protective.** Roughly 58% of the "None" group are physically active versus about 34% of the "Most days" group.
4. **Women are overrepresented at higher severity.** The female share rises from about half in the "None" group to about 60% in the "Most days" group.
5. **No single factor dominates.** Sleep trouble showed the strongest correlation with depression (r = 0.21), followed by poverty (r = -0.19), household income (r = -0.18), and physical activity (r = -0.11). The pattern points to multiple compounding burdens rather than one cause.

### Limitations

- The data are cross-sectional, so the analysis shows associations, not causation or direction.
- Depression is measured with a single self-report item, not a clinical diagnosis.
- The analysis is descriptive and bivariate. It does not model the factors together, so it cannot say whether they act independently.
- Correlations are modest in size (all |r| ≤ 0.21) and were computed on ordinal and binary variables recoded as numbers.
- The `NHANES` package provides a pre-processed 10,000-row sample in which some respondents appear more than once, so results are descriptive rather than formal population estimates.
- The package has no direct measures of childhood adversity, so this project looks at adult socioeconomic and behavioral correlates. Later projects bring in family and developmental data.

---

## How to Run the Analysis

**Option 1: Read the report.** Open the [rendered report](https://arshad-maliha.github.io/behavioral-science-portfolio/roots_and_resilience.html) in any browser, or download `roots_and_resilience.html` and open it locally.

**Option 2: Reproduce it in R.**

1. Download or clone this repository.
2. Open `roots_and_resilience.Rmd` in RStudio or Posit Cloud.
3. Install the packages used:

```r
install.packages(c("tidyverse", "NHANES", "skimr", "reshape2", "knitr", "rmarkdown"))
```

4. Click **Knit**, or run:

```r
rmarkdown::render("roots_and_resilience.Rmd")
```

---

## Portfolio Roadmap

| # | Project | Focus | Status |
|---|---------|-------|--------|
| 1 | Roots and Resilience | Socioeconomic and behavioral correlates of depressive symptoms (NHANES) | Complete |
| 2 | Depression gene expression | Differential expression in major depressive disorder, GEO dataset GSE98793 with DESeq2 | In progress |
| 3 | Epigenetics and intergenerational trauma | DNA methylation datasets | Planned |
| 4 | Developmental outcomes | Adolescent Brain Cognitive Development (ABCD) Study | Planned |

The projects form a connected arc: from social and behavioral context (Project 1), to molecular signals in depression (Project 2), to epigenetic mechanisms of trauma across generations (Project 3), to developmental outcomes in children (Project 4).

---

## Tools

R · R Markdown · tidyverse · ggplot2 · skimr · DESeq2 (Project 2) · Posit Cloud · Git and GitHub

---

## Contact

linkedin.com/in/maliha-arshad-036269146 · arsh.maliha@gmail.com
