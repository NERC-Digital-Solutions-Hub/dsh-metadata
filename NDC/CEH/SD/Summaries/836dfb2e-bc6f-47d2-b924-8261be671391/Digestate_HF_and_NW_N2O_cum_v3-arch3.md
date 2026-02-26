# Digestate_HF_and_NW_N2O_cum.csv

## Purpose and scope
- Supplement to the supporting documentation for data series related to N2O cumulation from a digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Describes the data structure and key processing steps of the Digestate_HF_and_NW_N2O_cum.csv dataset.

## Data structure and variables
- Dataset described as consisting of 7 columns and 40 rows, capturing N2O flux information across plots and treatments.
- Core fields include:
  - Site: HF (Henfaes) or NW (North Wyke)
  - Treatment: C (control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)
  - Block: 1–5 (randomised block design)
  - Plot: plot identifier from which yield-related measurements are derived
  - Date: date of the measurement
  - N2O_qa1, N2O_qa2, N2O_qa3: N2O flux data processed through quality assurance steps
- Note: The document outlines these fields and their purpose, including options for data cleaning and QA.

## Sites, treatments, and experimental design
- Two experimental sites: HF (Henfaes) and NW (North Wyke).
- Treatments follow a five-level scheme: C, D, AD, DNI, ADNI.
- Experimental design uses a randomized block structure with blocks 1–5.

## Measurements, units, and data fields
- Measurements pertain to N2O fluxes collected from plots/chambers over the experimental period.
- Data fields include:
  - N2O_qa1: all N2O flux data for each chamber/plot during the period used to derive cumulative values
  - N2O_qa2: cumulative N2O flux data after removing fits with R^2 < 0.6 and replacing with zero flux
  - N2O_qa3: cumulative N2O flux data after removing fits with R^2 < 0.6, replacing negative N2O values with zero
- Date marks when each measurement was taken; plot sizes and harvest area details accompany the dataset.

## Data quality assurance and processing
- QA steps:
  - qa1: all flux data prior to cumulative calculations
  - qa2: excludes low-quality fits (R^2 < 0.6) and replaces with zero flux
  - qa3: further excludes poor fits and sets negative flux values to zero
- R^2 threshold for excluding poor fits is explicit but noted as configurable ("arbitrary and can be changed" for both qa2 and qa3).
- Data cleaning decisions emphasize transparency and reproducibility of cumulative N2O calculations.

## Plot design and harvest area
- HF plots: two harvest-area configurations
  - For nitrogen addition rates: 1.2 m × 6.5 m
  - For C, D, AD, DNI, ADNI treatments: 1.2 m × 14 m
- NW plots: two harvest-area configurations
  - For nitrogen addition rates: 2 m × 4.5 m
  - For C, D, AD, DNI, ADNI treatments: 2 m × 9 m

## Data governance and reuse considerations
- The dataset is framed as part of a larger set of supporting documentation, implying the need for clear metadata and provenance to enable reuse.
- QA procedures and explicit documentation of treatment definitions support transparency and comparability across studies.
- Potential reuse considerations include:
  - Ensuring clarity on data cleaning thresholds (R^2) and their justifications
  - Access to measurement dates and plot-level details for temporal analyses
  - Availability of underlying data and metadata to enable independent verification and integration with other data series
- The surrounding documentation indicates a pathway to openness and standardised data management, aligned with monitoring framework practices.