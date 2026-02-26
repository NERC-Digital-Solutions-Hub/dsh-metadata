# Details of data structure to ' HF_N2O.csv '

- Dataset scope: N2O emissions data from a grassland fertiliser trial (2016) at Henfaes Research Station (Bangor University), stored in HF_N2O.csv. Contains 6 columns and 4404 rows.

- Data contents and columns:
  - Time: Midpoint of each measurement time period.
  - Treatment: Fertiliser type - AN (ammonium nitrate), U (urea), IU (inhibited urea), C (0N control).
  - N_app: Fertiliser application number (1, 2, or 3); first two applications are 90 kg ha-1, third application is 60 kg ha-1.
  - Block: Blocking factor in the randomized block design (1–4).
  - Plot: Plot number (1–16).
  - Flux_N2O: N2O flux for each chamber measurement period (µg N2O-N m h). Includes data quality adjustments.

- Data quality and cleaning rules:
  - Flux_N2O values with R^2 < 0.6 and all negative N2O values were replaced with 0.
  - Flux data derived from a mix of measurement methods and instruments; units standardized to µg N2O-N m h.

- Measurement methods and data collection:
  - Measurement approach:
    - A combination of automatic chambers with online analysis (Los Gatos Research N2O Isotopomer) and manual static chambers.
  - Experimental phases:
    - First cut (early phase): 12 automatic chambers used for N treatments (AN, U, IU); manual static chambers used for control (C), n = 4.
    - Remainder of the experiment (cuts 2 & 3): 12 automatic chambers used on plots 1–12; no manual chambers used (block 4 data unavailable, n = 3).
  - Temporal coverage:
    - Manual chamber measurements: 13 occasions during cut 1.
    - Automatic chambers: sequential measurements for a 30-minute time period per chamber.
  - Data provenance:
    - Flux data generated from both automatic and manual chamber measurements; combined in the HF_N2O.csv file with documentation of measurement method by period.

- Experimental design details:
  - Treatments reflect different N fertiliser types (AN, U, IU) plus a 0N control (C).
  - N_app indicates the fertiliser application events; exact application rates per event are specified.
  - Blocking design includes four blocks; plots numbered 1–16 across treatments and blocks.

- Data availability, limitations, and governance considerations for data stewards:
  - Incomplete or differing data coverage across blocks (e.g., lack of manual measurements in block 4 after cuts 2/3) should be documented and considered in analyses.
  - Data cleaning step (R^2 threshold and zeroing negative flux values) is a defined quality control rule to apply consistently.
  - Documentation should preserve method metadata (automatic vs manual chamber measurements) and period-specific design (which blocks/plots had which measurement methods).
  - Metadata should include column definitions, units, time semantics (midpoint timing), and provenance to support discovery, reuse, and reproducibility.
  - This dataset supplements broader CINAg experiment documentation; refer to supporting documentation for additional context and data series details.