# Details of data structure to ' HF_N2O.csv '

- Overview
  - Supplement detailing the HF_N2O.csv dataset: 6 columns, 4404 rows.
  - N2O emissions data from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University).

- Dataset structure (columns and meaning)
  - Time: Midpoint of each measurement time period.
  - Treatment: Fertiliser type – AN (ammonium nitrate/Nitram), U (urea), IU (inhibited urea/agrotain), C (0N control).
  - N_app: Fertiliser applications encoded as 1, 2, or 3 (1st & 2nd applications = 90 kg ha^-1; 3rd application = 60 kg ha^-1).
  - Block: Blocking factor of a randomized block design (1–4).
  - Plot: Plot number (1–16).
  - Flux_N2O: N2O flux for each chamber measurement period, units = µg N2O-N m h.
  - Note: Flux data after cleaning include removal of low-quality data (R^2 < 0.6) and replacement of negative flux values with 0.

- Data collection and measurement approach
  - Measurement methods: Combination of automatic chambers with online analysis (Los Gatos Research N2O Isotopomer) and manual static chambers.
  - First cut: 12 automatic chambers used for N treatments (AN, U, IU); manual chambers used for 0N control (C) with n = 4.
  - Remainder (cuts 2 & 3): 12 automatic chambers on plots 1–12; no manual chambers. Block 4 had no measurements (n = 3 for that block).
  - Manual chamber measurements: 13 occasions during cut 1.
  - Automatic chamber measurements: sequential 30-minute time periods for each chamber.

- Data cleaning and quality notes
  - Flux_N2O values: negative values replaced with 0.
  - Dropped data: flux data with R^2 < 0.6 removed to ensure data quality.
  - Data provenance indicates a mix of measurement technologies across cuts, which may affect comparability.

- Design, coverage, and limitations
  - Experimental design: Randomised block design with blocks 1–4 and plots 1–16.
  - Coverage gaps: No data for block 4 in cuts 2 & 3; manual measurements limited to cut 1.
  - Implications: Potential confounding due to differing measurement methods between cuts and missing block data when analysing across time or treatments.

- Metadata and usage considerations for Data Leaders
  - Track data lineage: raw measurements vs. cleaned Flux_N2O values.
  - Consider the mixing of automatic and manual chambers when modelling flux responses across treatments.
  - Ensure awareness of treatment vs. control comparisons and the impact of missing block data.
  - Use metadata to inform data discoverability, data quality checks, and reproducible analyses.