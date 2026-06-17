# ERPO-Augmented-Synthetic-Control

## Overview

This repository contains the replication code used to conduct the augmented synthetic control analyses examining the association between Extreme Risk Protection Order (ERPO) laws and firearm homicide rates in the United States.

The analyses were conducted using the Augmented Synthetic Control Method (ASCM) implemented through the PySynCon package. The code reproduces the analytical workflow used to generate study figures, including synthetic control estimation, placebo tests, statistical inference, and leave-one-out robustness analyses.

## Repository Contents

- `ERPO_Firearm_Homicide_ASCMAnalysis.ipynb` – main analysis notebook.

## Data Availability

The dataset used in these analyses is not included in this repository because it cannot be publicly redistributed.

Researchers with authorized access to the underlying data should place the required dataset file (`Death_and_Population_Data1999.csv`) in the same directory as the notebook before running the analysis.

## Analytical Workflow

The notebook performs the following steps:

1. Data preparation and construction of the analytic sample.
2. Calculation of firearm homicide rates per 100,000 population.
3. Estimation of augmented synthetic control models.
4. Extraction and reporting of donor-state weights.
5. Visualization of treated and synthetic trajectories.
6. Placebo testing and calculation of permutation-based p-values.
7. Leave-one-out robustness analyses for influential donor states.

## Replication Notes

The same analytical workflow was applied across all state-specific and outcome-specific analyses reported in the manuscript.

To reproduce a different analysis, users should update:

- the treated state (all references),
- the treatment year (all references),
- the outcome variable (overall, male, or female firearm homicide rates),
- figure labels and output file names.

All other data preparation procedures, donor pool restrictions, model specifications, placebo tests, and robustness checks were kept consistent across analyses.

This version reproduces the analysis for Colorado (treatment year: 2020) and female firearm homicide rates.

## Software

Analyses were conducted using Python version 3.12.13. and the PySynCon package.
