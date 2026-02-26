# Details of data structure to ' Digestate_HF_and_NW_N2O_v2.csv '

## Overview
- Supplement to supporting documentation for CINAg experiments.
- 8 columns, 2800 rows.
- Data from digestate wheat trial 2017 at Henfaes Research Center (HF) and North Wyke (NW).
- N2O fluxes measured under different digestate treatments: C (control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- Two sites: HF and NW; randomized block design (Blocks 1–5); plots provide yield measurement basis.
- “NA” indicates Not Assessed.

## Dataset structure (columns and explanations)
- Site: HF or NW (Henfaes or North Wyke).
- Treatment: C, D, AD, DNI, ADNI.
- Block: 1–5, blocking factor of randomized block design.
- Plot: plot identifier; most yield measurements derived from plots, with exceptions for monthly samplings in specific plots.
- Date: date of measurement.
- N2O_qa1: all N2O flux data for each chamber/plot used to derive cumulative values during the entire experimental period.
- N2O_qa2: cumulative N2O flux data after data cleaning—flux values from fits with R^2 < 0.6 are removed and set to zero. R^2 threshold is configurable (arbitrary for qa2/qa3).
- N2O_qa3: cumulative N2O flux data after additional cleaning—fits with R^2 < 0.6 are removed; all negative N2O flux values replaced with zero.

## Data quality and cleaning notes
- R^2 threshold (0.6) used to determine which cumulative fits are retained for qa2 and qa3; threshold can be modified as needed.
- qa2 and qa3 involve replacing data with zero under specific fit quality criteria.
- Negative N2O flux values are set to zero in qa3.

## Spatial and measurement details
- Plot sizes differ by site:
  - HF: harvest area 1.2 m × 6.5 m for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI.
  - NW: harvest area 2 m × 4.5 m for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI.
- Data originates from two field trial locations and aggregates chamber/plot measurements across the experimental period.

## Usage notes for GIS specialists
- Potential map fields: Site, Plot, Block, Date, Treatment, and N2O flux metrics (N2O_qa1, N2O_qa2, N2O_qa3).
- Join keys: Site, Plot (and optionally Block) to align with spatial plots or sensor locations.
- Suitable outputs: maps of instantaneous flux (qa1) or cumulative flux (qa2/qa3), with QA flags implied by qa2/qa3 cleaning criteria.
- Be mindful of data cleaning: qa2/qa3 thresholds affect which observations contribute to cumulative summaries.
- Noting NA values: use as Not Assessed where applicable.