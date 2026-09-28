# Behavioral Science Portfolio

A portfolio of behavioral data science projects at the intersection of bioinformatics, psychology, and public health, built in R.

The work is organized around one question: **what keeps people stuck, and what helps them move forward?** Each project looks at that question from a different angle, from family and social environment to biology and development.

**Author:** Maliha Arshad, Bioinformatics Scientist

---

## Featured Project: Roots and Resilience

**How Family Adversity Shapes Child and Adult Outcomes**

An exploratory analysis of National Health and Nutrition Examination Survey (NHANES) data examining the behavioral and social correlates of family adversity, and how they show up in child and adult outcomes.

| | |
|---|---|
| **Status** | Complete |
| **Data source** | NHANES (CDC National Center for Health Statistics) |
| **Language** | R |
| **Report** | [`roots_and_resilience.html`](roots_and_resilience.html) (rendered analysis) |
| **Code** | [`roots_and_resilience.Rmd`](roots_and_resilience.Rmd) (R Markdown source) |

### Research question

[Add 1-2 sentences: the specific question the analysis asks, e.g. "Is exposure to X during childhood associated with Y in adulthood?"]

### Data

- **Source:** NHANES, a nationally representative U.S. survey run by the CDC.
- **Cycles used:** [add survey years]
- **Sample:** [add sample size and inclusion criteria]
- **Key variables:** [list the main adversity, outcome, and covariate variables]

### Methods

- Data cleaning and wrangling with the tidyverse
- Exploratory data analysis and visualization
- [Add any statistical tests or models, e.g. regression, chi-square, survey weighting]

### Key findings

1. [Finding one, in plain language]
2. [Finding two]
3. [Finding three]

### Limitations

- NHANES is cross-sectional, so the analysis shows associations, not causation.
- [Add other limitations: self-report measures, missing data, sample restrictions]

---

## How to View the Analysis

**Option 1: Read the report.** Download `roots_and_resilience.html` and open it in any web browser. (GitHub shows HTML files as raw code, so download it or view it through GitHub Pages once that is enabled.)

**Option 2: Reproduce it in R.**

1. Download or clone this repository.
2. Open `roots_and_resilience.Rmd` in RStudio or Posit Cloud.
3. Install the packages the analysis uses. To see the full list, run:

```r
install.packages("renv")
renv::dependencies("roots_and_resilience.Rmd")
```

4. Install anything missing, for example:

```r
install.packages(c("tidyverse", "knitr", "rmarkdown"))
```

5. Click **Knit** (or run `rmarkdown::render("roots_and_resilience.Rmd")`) to regenerate the HTML report.

---

## Portfolio Roadmap

| # | Project | Focus | Status |
|---|---------|-------|--------|
| 1 | Roots and Resilience | Family adversity and outcomes using NHANES | Complete |
| 2 | Depression gene expression | Differential expression in major depressive disorder using GEO dataset GSE98793 and DESeq2 | In progress |
| 3 | Epigenetics and intergenerational trauma | DNA methylation datasets | Planned |
| 4 | Developmental outcomes | Adolescent Brain Cognitive Development (ABCD) Study | Planned |

The four projects are designed as a connected arc: from social and family context (Project 1), to molecular signals in depression (Project 2), to epigenetic mechanisms of trauma across generations (Project 3), to developmental outcomes in children (Project 4).

---

## Tools

R · R Markdown · tidyverse · DESeq2 (Project 2) · Posit Cloud · Git and GitHub

---

## Contact

[Add LinkedIn URL] · [Add email or portfolio site link]
