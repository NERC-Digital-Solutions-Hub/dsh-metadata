# Details of data structure to ' Digestate_HF_and_NW_N2O_cum.csv'

## Overview
- Dataset comprises 7 columns and 40 rows from a 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations (Rothamsted/Bangor collaboration).
- N2O flux data collected for plots under different digestate treatments: C (control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), and ADNI (acidified digestate with DMPP).
- plots include a randomised block design with blocking factor and site-specific plot sizes.
- Some plots (1, 19, 25, 31, 47) were used for monthly samplings for the 150 kg N ha-1 treatment.

## Data columns and meanings
- Site: HF (Henfaes) or NW (North Wyke).
- Treatment: C, D, AD, DNI, ADNI.
- Block: 1–5; blocking factor of the randomised block design.
- Plot: plot number; all yield measurements derive from these plots except plots 1, 19, 25, 31, 47 used for monthly samplings for 150 kg N ha-1.
- Date: date of the measurement.
- N2O_qa1: all N2O flux data for each chamber/plot over the full experimental period used to derive cumulative values.
- N2O_qa2: cumulative N2O flux data after removing fits with R2 < 0.6 and replacing with zero flux; R2 threshold is adjustable.
- N2O_qa3: cumulative N2O flux data after removing fits with R2 < 0.6 and replacing negative Flux_N2O values with zero; R2 threshold is adjustable.
- Note: Each N2O-related column references data processing steps (qa1, qa2, qa3) applied to flux calculations.

## Data processing and quality assurance
- N2O_qa2 and N2O_qa3 involve data fits with an R squared cutoff of 0.6; fits below this threshold are removed and replaced with zero flux.
- Negative flux values are set to zero in qa3.
- The R2 threshold is described as arbitrary and can be changed for both qa2 and qa3.

## Experimental design details and plot alignment
- Plots and harvest areas differ by site:
  - HF: plots sized 1.2 m × 6.5 m (harvest area) for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI treatments.
  - NW: plots sized 2.0 m × 4.5 m (harvest area) for nitrogen addition rates; 2.0 m × 9 m for C, D, AD, DNI, ADNI treatments.

## Provenance and supplemental context
- This document supplements supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Data originate from the 2017 digestate wheat trial across HF and NW sites, contributed by Banogor/Bangor University and Rothamsted Research teams.