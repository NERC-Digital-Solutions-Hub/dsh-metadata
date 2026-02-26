# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' HF_N2O.csv '

- Overview
  - Provides details for the HF_N2O.csv dataset (6 columns, 4404 rows) containing N2O emissions data from a grassland fertiliser trial in 2016 at Henfaes Research Station, Bangor University.

- Dataset structure and fields
  - Time: midpoint of each measurement time period
  - Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea), C (0N control)
  - N_app: 1, 2, or 3 denoting fertiliser applications; 1st & 2nd applications are 90 kg ha^-1, 3rd application is 60 kg ha^-1
  - Block: 1–4 blocking factor of the randomised block design
  - Plot: 1–16 (Plot numbering includes codes -2 and -1)
  - Flux_N2O: N2O flux for each chamber measurement period (units: µg N2O-N m h)
  - Data cleaning: Flux data with R^2 < 0.6 and all negative N2O values replaced with 0

- Measurements and instrumentation
  - N2O fluxes measured using a combination of automatic chambers with online analysis (Los Gatos Research N2O Isotopomer) and manual static chambers
  - For the first cut: 12 automatic chambers on N treatments (AN, U, IU); manual static chambers used for 0N control (C), n = 4
  - For cuts 2 & 3: 12 automatic chambers used on plots 1–12; no manual chambers; no measurements from block 4 (n = 3)
  - Manual-chamber measurements: 13 occasions during cut 1
  - Automatic-chamber measurements: measurements from each chamber sequentially for a 30-minute time period

- Data quality and processing notes
  - Flux data with R^2 < 0.6 are excluded or adjusted; all negative N2O values replaced with 0

- Experimental design context
  - Grassland fertiliser trial conducted in 2016
  - Treatments span different nitrogen fertiliser types and application schedules
  - Blocking and plot structure implemented to control spatial variability

- Data provenance
  - Supplement to the associated supporting documentation for CINAg experiments (referenced PDF) and the HF_N2O.csv dataset