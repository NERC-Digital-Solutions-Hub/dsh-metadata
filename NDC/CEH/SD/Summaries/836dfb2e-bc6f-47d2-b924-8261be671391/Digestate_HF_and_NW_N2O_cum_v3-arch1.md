# Details of data structure to ' Digestate_HF_and_NW_N2O_cum.csv '

## Overview
- Supplement to the supporting documentation for CINAg experiments.
- Provides details of the data structure for the Digestate_HF_and_NW_N2O_cum.csv dataset.
- Data originate from a 2017 digestate wheat trial conducted at two sites: Henfaes Research Center (HF) and North Wyke (NW), involving Bangor University and Rothamsted Research.

## Dataset scope
- 7 columns and 40 rows.
- Focused on nitrous oxide (N2O) flux measurements from plots under different digestate treatments.

## Sites and treatments
- Sites: HF (Henfaes) and NW (North Wyke).
- Treatments:
  - C: zero nitrogen control
  - D: digestate
  - AD: acidified digestate
  - DNI: digestate with nitrification inhibitor (DMPP)
  - ADNI: acidified digestate with nitrification inhibitor (DMPP)

## Experimental design
- Design: randomised block design with Block values 1–5.
- Plot identifiers provided for data extraction; plots 1, 19, 25, 31, and 47 used for monthly samplings at the 150 kg N ha-1 treatment.

## Data columns and meanings
- Site: HF or NW.
- Treatment: C, D, AD, DNI, ADNI.
- Block: blocking factor (1–5).
- Plot: plot number from which yield-related measurements were derived.
- Date: date of the measurement.
- N2O_qa1: all N2O flux data for each chamber/plot for the entire experimental period used to derive cumulative values.
- N2O_qa2: cumulative N2O flux data after data-fitting; values from fits with R^2 < 0.6 were removed and replaced with zero flux. R^2 cutoff is adjustable for qa2.
- N2O_qa3: cumulative N2O flux data after additional processing; fits with R^2 < 0.6 removed and all negative N2O flux values replaced with zero. Note: N2O_qa3 is an additional QA step (negative values set to zero).

## Data processing and quality assurance
- N2O_qa2 and N2O_qa3 involve excluding poorly fitted data (R^2 < 0.6) and handling negative flux values by replacing with zero.
- R^2 thresholds are adjustable, affecting qa2 and qa3.

## Plot and measurement details
- Plot sizes differ by site and treatment:
  - HF: harvest areas of 1.2 m x 6.5 m for nitrogen addition rates; 1.2 m x 14 m for C, D, AD, DNI, ADNI treatments.
  - NW: harvest areas of 2 m x 4.5 m for nitrogen addition rates; 2 m x 9 m for C, D, AD, DNI, ADNI treatments.

## Data provenance and usage
- Dataset linked to the broader CINAg experiment documentation and its supporting materials.
- Designed to enable analysis of N2O flux responses to different digestate treatments across two field sites and to support data discovery with metadata.