# Details of data structure to ' Digestate_HF_and_NW_Production.csv '

## Overview
- Supplement to supporting documentation for data series in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Dataset: 7 columns, 90 rows
- Source: Digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke Research Station (NW)
- Variables capture wheat yields under digestate treatments and mineral N addition rates

## Dataset columns and units
- Site: HF or NW (location)
- Plot: Experimental plot number
- Block: Blocking factor (1–5) for randomized block design
- Treatment: Codes representing either digestate treatments (C, D, AD, DNI, ADNI) or mineral N rates (N-75, N-150, N-225, N-300)
  - C = zero N control
  - D = digestate
  - AD = acidified digestate
  - DNI = digestate with nitrification inhibitor (DMPP)
  - ADNI = acidified digestate with nitrification inhibitor (DMPP)
  - N-75 to N-300 = NH4NO3 at specified kg N ha-1
- Plant_yield: Whole plant yield at 100% dry matter (tonnes ha-1)
- Grain_yield: Grain yield at 100% dry matter (tonnes ha-1)
- TGW: Thousand grain weight at 100% dry matter (grams)
- All yield data reported at 100% dry matter; NA indicates not assessed

## Experimental design
- Experimental framework: Randomised block design with blocks 1–5
- Treatments include both digestate-based treatments and mineral nitrogen addition rates
- DMPP (nitrification inhibitor) present in DNI and ADNI treatments
- Data structure supports comparison between digestate amendments and conventional N fertilisers

## Plot dimensions by site
- HF (Henfaes):
  - Nitrogen addition rate plots: harvest area 1.2 m × 6.5 m
  - Digestate-related plots (C, D, AD, DNI, ADNI): harvest area 1.2 m × 14 m
- NW (North Wyke):
  - Nitrogen addition rate plots: harvest area 2 m × 4.5 m
  - Digestate-related plots (C, D, AD, DNI, ADNI): harvest area 2 m × 9 m

## Data provenance and purpose
- This document provides the data structure details for Digestate_HF_and_NW_Production.csv
- It serves as supplementary information to the broader CINAg experiments documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)
- Intended to enable data discovery, validation, and construction of data products (e.g., dashboards) for exploring digestate versus mineral N effects on wheat production.