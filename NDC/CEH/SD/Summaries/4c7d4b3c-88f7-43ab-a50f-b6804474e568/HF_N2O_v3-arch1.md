# Details of data structure to ' HF_N2O.csv '

## Overview
- N2O emissions dataset from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University).
- 6 columns, 4404 rows.
- Data from a mix of automatic chambers (online analysis) and manual static chambers.
- Used to study effects of different nitrogen fertiliser types and application schedules on N2O flux.

## Dataset structure and columns
- Time: Midpoint of each measurement time period.
- Treatment: Fertiliser type
  - AN = ammonium nitrate (Nitram)
  - U = urea
  - IU = inhibited urea (Agrotain)
  - C = 0N control
- N_app: Fertiliser application sequence (1, 2, or 3)
  - 1st and 2nd applications: 90 kg ha-1
  - 3rd application: 60 kg ha-1
- Block: Blocking factor in the randomized block design (1–4)
- Plot: Plot number (1–16). Note: block 4 has no measurements in this dataset (n = 3 for that block)
- Flux_N2O: N2O flux for each chamber measurement period
  - Unit: µg N2O-N m h

## Data processing and quality control
- Flux values with R^2 < 0.6 were flagged; where applicable, negative N2O values were set to 0.
- Data are presented as flux measurements from various chamber systems with specified measurement periods.

## Measurement methodology
- Flux measurements obtained using:
  - Automatic chambers with online analysis (Los Gatos Research N2O Isotopomer)
  - Manual static chambers
- For the first cut:
  - 12 automatic chambers used on N treatments (AN, U, IU)
  - Manual static chambers used for the 0N control (C) group (n = 4)
- For cuts 2 and 3:
  - 12 automatic chambers used on plots 1–12
  - No manual chambers used; no measurements from block 4
- Manual-chamber measurements occurred on 13 occasions during cut 1
- Automatic chambers measured sequentially for a 30-minute time period per chamber

## Experimental design and scope
- Grassland fertiliser trial with distinct N fertiliser types and an unamended control.
- N_app schedule tied to application events with defined N rates.
- Blocking and plot structure to account for spatial variability.
- Partial data for block 4 (no measurements in this dataset) and mixed use of measurement methods across cuts.

## Practical considerations for analysis
- Potential analyses include:
  - Comparing N2O flux across fertiliser treatments (AN, U, IU) and control (C)
  - Assessing effects of application sequence (N_app 1–3) on flux
  - Evaluating block and plot-level variability
  - Integrating automatic vs manual chamber data with attention to method differences
- Limitations and caveats:
  - Missing data for block 4 (n = 3)
  - Manual chamber measurements limited to cut 1
  - Flux data filtered by R^2 threshold and zeroed for negative values
- Data scale and units to consider:
  - Time periods and flux measurements are time-indexed
  - Flux_N2O units: µg N2O-N m h

## Provenance and context
- Supplemental data accompanying the CINAg experiments documentation.
- Data origin: HF_N2O.csv from the 2016 fertiliser trial at Henfaes Research Station, Bangor University.
- Supplement provides the structure and methodological context for use in subsequent analyses.