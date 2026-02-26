# Details of data structure to ' HF_N2O.csv '

## Overview
- Supplement to supporting documentation for data series describing the HF_N2O.csv dataset.
- Contains 6 columns and 4404 rows of N2O emission data from a 2016 grassland fertiliser trial at Henfaes Research Station (Bangor University).

## Data structure and variables
- Time: Midpoint of each measurement time period.
- Treatment: Coded as AN (ammonium nitrate), U (urea), IU (inhibited urea), C (0N control).
- N_app: Fertiliser application number (1, 2, or 3; 1st & 2nd applications at 90 kg ha-1, 3rd at 60 kg ha-1).
- Block: Blocking factor of the randomized block design (1–4).
- Plot: Plot number (1–16; with some blocks/plots treated differently across cuts).
- Flux_N2O: N2O flux for each chamber measurement period (units: µg N2O-N m h). Note: flux data were cleaned per quality rules below.

## Data processing and quality control
- Flux_N2O values with R² < 0.6 and all negative N2O values were replaced with 0.
- Measurements obtained using a mix of instruments and protocols described below; data reflect the combination of automatic and manual chamber methods.

## Sampling design and measurement methodology
- Measurement approach:
  - Automatic chambers with online analysis (Los Gatos Research N2O Isotopomer) and manual static chambers.
- Experimental design by cut, treatment, and plot:
  - Cut 1: 12 automatic chambers were used on N treatments (AN, U, IU). Manual static chambers used for 0N control (C), n = 4.
  - Cuts 2 & 3: The 12 automatic chambers were used on plots 1–12; no manual chambers were used.
  - Consequently, no measurements from block 4 in this dataset; total n = 3 for that block reference.
- Manual chamber measurements:
  - 13 occasions during cut 1.
- Automatic chamber measurements:
  - Each chamber measured sequentially for a 30-minute time period.

## Coverage, limitations, and notes for data use
- The dataset captures N2O flux from a subset of plots and blocks across the first cut and the subsequent cuts only via automatic chambers.
- No manual chamber data for cuts 2 and 3; no measurements from block 4 in this dataset.
- Data are suitable for self-serve analyses of N2O flux patterns under different fertiliser treatments, with explicit data cleaning applied to flux values.