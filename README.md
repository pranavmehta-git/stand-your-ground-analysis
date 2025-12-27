# Do Stand Your Ground Laws Increase Homicides?

A difference-in-differences analysis of Stand Your Ground laws and homicide rates, replicating Cheng & Hoekstra (2013).

## Overview

Between 2000 and 2010, 21 U.S. states adopted "Stand Your Ground" laws that removed the duty to retreat before using deadly force in self-defense. This project uses difference-in-differences with staggered treatment timing to estimate the causal effect of these laws on homicide rates.

## Key Findings

- **8–10% increase in homicides**: Stand Your Ground laws are associated with a statistically significant increase in homicide rates
- **~600 additional deaths per year**: The effect translates to approximately 600 additional homicides annually in adopting states
- **Staggered adoption**: The analysis exploits variation in timing across states for identification
- **Parallel trends**: Evidence for the identifying assumption is stronger for some state comparisons than others

## Methods

The analysis employs:
- Event study plots comparing treated vs. never-treated states
- Two-way fixed effects (TWFE) estimation with state and year fixed effects
- Clustered standard errors at the state level

## Visualizations

The project includes:
1. Distribution of homicide rates across states
2. State-by-state changes in homicide rates (2000–2010)
3. Event study plot: Florida vs. never-treated states
4. Event study plot: 2006 adopters vs. never-treated states

## Data

The analysis uses replication data from Cheng & Hoekstra (2013), containing state-year observations from 2000–2010 with:
- Homicide counts and rates
- Stand Your Ground law adoption dates
- Demographic and policy covariates

**Note**: Data file (`castle_expanded2.rdata`) not included in repository.

## Files

```
├── stand-your-ground-analysis.Rmd   # Main R Markdown analysis
├── README.md                         # This file
├── .gitignore                        # Git ignore rules
└── LICENSE                           # MIT License
```

## Requirements

- R (≥ 4.0)
- R packages:
  - `tidyverse`
  - `fixest`
  - `ggfixest`
  - `bacondecomp`
  - `knitr`
  - `kableExtra`

Install required packages:

```r
install.packages(c("tidyverse", "fixest", "ggfixest", "bacondecomp", "knitr", "kableExtra"))
```

## References

Cheng, C., & Hoekstra, M. (2013). Does strengthening self-defense law deter crime or escalate violence? Evidence from expansions to castle doctrine. *Journal of Human Resources*, 48(3), 821-854.

Cunningham, S. (2021). *Causal Inference: The Mixtape*. Yale University Press. [Chapter 9](https://mixtape.scunning.com/09-difference_in_differences)

Huntington-Klein, N. (2021). *The Effect: An Introduction to Research Design and Causality*. [Chapter 18](https://theeffectbook.net/ch-DifferenceinDifference.html)

## Acknowledgments

This analysis was completed as part of the *Data Analysis for Policy Research using R* course at Columbia University, taught by **Prof. Harold Stolper**.

## License

MIT License - see [LICENSE](LICENSE) for details.

## Author

Pranav Mehta
