# HF_NH3.csv

## Overview
- NH3 emissions dataset from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University).
- Contains 7 columns and 476 rows detailing daily NH3 emissions following fertiliser applications.
- Measurements used wind tunnels on plots amended with urea or inhibited urea (agrotain).
- Emissions tracked for 3 weeks after fertiliser applications with daily sampling.
- Experimental design: 16 plots (1–16) in a randomised block design with 4 blocks (1–4).
- Fertiliser applications: first and second applications at 90 kg ha-1; third application at 60 kg ha-1.
- Emissions reported as Emission_rate_kghad (kg NH3-N ha-1 d-1).

## Data structure and fields
- Time_Start: Date and time at start of sampling period.
- Time_End: Date and time at end of sampling period.
- N_app: 1|2|3 indicating which fertiliser application (1st & 2nd application 90 kg ha-1, 3rd application 60 kg ha-1).
- Plot: Plot identifier (1–16) that was measured.
- Block: Blocking factor in the randomised design (1–4).
- Treatment: Fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea/agrotain).
- Emission_rate_kghad: Emission rate of NH3 from the plot for 1 day (kg NH3-N ha-1 d-1).

## Measurement and processing notes
- Data derived from wind tunnel measurements; global daily sampling over a 3-week period after fertiliser application.
- Wind tunnel anemometer failures:
  - Plot 3 during first and second applications, and Plot 14 during the third application failed.
  - Affected values were removed and replaced with the mean value from surrounding wind tunnels.
- Detection and data handling:
  - Limit of detection for NH4-N: 0.1 mg L-1.
  - Negative NH3 flux values replaced with 0.
- Dataset size: 7 columns, 476 rows.

## Context and provenance
- Supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Specifically documents the data structure and preparation steps for HF_NH3.csv.

## Use and considerations for environmental monitoring
- Provides a standardised, traceable format suitable for monitoring environmental health and evaluating policy-related performance over time.
- Clear documentation of data cleaning (wind tunnel replacements, detection limits, and zeroing negatives) supports reproducibility.
- Aligns with broader objectives to increase dataset value and enable access to underlying data for broader analyses and integration with other environmental datasets.