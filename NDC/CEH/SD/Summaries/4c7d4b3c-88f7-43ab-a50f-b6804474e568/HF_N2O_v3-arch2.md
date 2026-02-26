# HF_N2O.csv

## Overview
- N2O emissions dataset from grassland fertiliser trial 2016 at Henfaes Research Station (Bangor University).
- 6 columns, 4404 rows.
- Key variables: Time, Treatment, N_app, Block, Plot, Flux_N2O.

## Data structure and column definitions
- Time: midpoint of each measurement time period.
- Treatment: AN | U | IU | C (N fertilizer type; AN = ammonium nitrate, U = urea, IU = inhibited ureа, C = 0N control).
- N_app: 1 | 2 | 3 (fertiliser application sequence; 1st & 2nd applications 90 kg ha−1, 3rd application 60 kg ha−1).
- Block: 1 | 2 | 3 | 4 (randomised block design).
- Plot: 1–16 (plot identifier within blocks).
- Flux_N2O: N2O flux for each chamber measurement period, unit µg N2O-N m−2 h−1.
- Data quality notes:
  - Flux values with R^2 < 0.6 and all negative N2O values replaced with 0.

## Measurement methodology
- Measurement approach: combination of automatic chambers with online analysis (Los Gatos Research N2O Isotopomer) and manual static chambers.
- First cut:
  - 12 automatic chambers on N treatments (AN, U, IU).
  - Manual static chambers on 0N control (C), with n = 4.
- Cuts 2 & 3:
  - 12 automatic chambers on plots 1–12.
  - No manual chambers (block 4 measurements not included in these cuts; n = 3).
- Manual chamber measurements:
  - Conducted on 13 occasions during cut 1.
- Automatic chamber measurements:
  - Each chamber measured sequentially for a 30-minute period.

## Experimental design context
- Grassland fertiliser trial conducted in 2016 at Henfaes Research Station.
- Randomised block design with four blocks (1–4) and plots 1–16.
- Treatments include AN, U, IU, and C (control) with specified N_app application scheme.

## Data processing and quality notes
- Flux data underwent quality control: removal or adjustment of low-reliability measurements (R^2 < 0.6) and replacement of negative flux values with zero.
- Time-centered measurements and chamber-specific data used to compute fluxes per measurement period.

## Practical considerations for analysts
- Be mindful of differences between cuts (automatic chambers used throughout, but manual chambers only in cut 1 for controls).
- Missing data relate to block 4 in later cuts due to study design changes.
- N_app coding corresponds to application timing and rates; interpretation should align with the fertiliser schedule.
- Dataset supplements broader documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf) for full context.