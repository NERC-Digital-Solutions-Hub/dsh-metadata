# Digestate_HF_and_NW_Production.csv

- Supplemental data describing the data structure for the Digestate_HF_and_NW_Production.csv dataset, part of the CINAg experiments documentation.

## Overview
- 7 columns and 90 rows.
- Data originate from a 2017 wheat trial conducted at Henfaes Research Center (HF) and North Wyke research station (NW), involving digestate and nitrogen treatments.
- Comparisons include zero N control, digestate forms, and chemical N at varying application rates.
- All yield data are reported at 100% dry matter.

## Dataset scope and sites
- Sites: Henfaes (HF) and North Wyke (NW).
- Experimental setup includes randomized blocks and plot-level treatments.
- Plot sizes differ by site and treatment type as specified in the data documentation.

## Columns and their meaning
- Site: HF or NW.
- Plot: Experimental plot number.
- Block: Blocking factor (1–5) of the randomized block design.
- Treatment: Digestate-related treatments:
  - C = zero N control
  - D = digestate
  - AD = acidified digestate
  - DNI = digestate with nitrification inhibitor (DMPP)
  - ADNI = acidified digestate with nitrification inhibitor (DMPP)
  - N-75, N-150, N-225, N-300 = NH4NO3 at 75, 150, 225, and 300 kg N ha^-1 respectively
- Plant_yield: Whole plant yield at 100% dry matter (tonnes ha^-1).
- Grain_yield: Grain yield at 100% dry matter (tonnes ha^-1).
- TGW: Thousand grain weight at 100% dry matter (grams).

## Measurements and data characteristics
- All yield measurements are 100% dry matter.
- NA indicates data not assessed.
- The dataset combines two sites with potentially different harvest area dimensions.

## Treatments and nitrogen context
- Digestate treatments (D, AD, DNI, ADNI) are evaluated against a zero N control (C).
- Nitrogen fertilization rates (N-75 to N-300) provide comparisons with chemical N inputs.
- The treatment naming distinguishes digestate form and presence of a nitrification inhibitor (DMPP).

## Plot sizes and harvesting details
- HF: Plots with nitrogen addition rates have harvest areas of 1.2 m × 6.5 m; C, D, AD, DNI, ADNI plots have harvest areas of 1.2 m × 14 m.
- NW: Plots with nitrogen addition rates have harvest areas of 2 m × 4.5 m; C, D, AD, DNI, ADNI plots have harvest areas of 2 m × 9 m.

## Provenance and usage notes
- This document is a supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Provides data-structure details for Digestate_HF_and_NW_Production.csv to aid data discovery, governance, and cross-site analysis.
- Implications for data leaders: facilitates data integration across sites, metadata interpretation, and assessment of data gaps, quality, and applicability for policy or research contexts.