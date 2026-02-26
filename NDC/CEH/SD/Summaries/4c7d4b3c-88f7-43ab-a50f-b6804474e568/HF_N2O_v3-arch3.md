# Details of data structure to ' HF_N2O.csv '

## Overview
- Supplement to supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Contains the N2O emissions dataset from a grassland fertiliser trial (2016) at Henfaes Research Station (Bangor University).
- Dataset used for monitoring environmental health measures related to agricultural N2O emissions.

## Dataset structure
- Columns: 6; Rows: 4404.
- Columns and content:
  - Time: Midpoint of each measurement time period.
  - Treatment: Coded as AN (ammonium nitrate), U (urea), IU (inhibited urea), C (0N Control).
  - N_app: Fertiliser application event number; values 1, 2, or 3 (with corresponding application rates: first two applications 90 kg ha^-1, third application 60 kg ha^-1).
  - Block: Blocking factor in randomized block design (values 1–4).
  - Plot: Plot numbers (1–16).
  - Flux_N2O: N2O flux for each chamber measurement period; unit given as µg N2O-N m h (as stated in document).
- Data cleaning note: Flux_N2O values with R^2 < 0.6 and all negative values replaced with 0.

## Experimental design and data collection
- Trial: Grassland fertiliser trial conducted in 2016.
- Measurement approach:
  - N2O fluxes measured using a combination of automatic chambers with online analysis (Los Gatos Research N2O Isotopomer) and manual static chambers.
- First cut:
  - 12 automatic chambers applied to N treatments (AN, U, IU).
  - Manual static chambers used for 0N Control (C); n = 4.
- Remainder of experiment (cuts 2 & 3):
  - 12 automatic chambers used on plots 1–12.
  - No manual chambers used; block 4 measurements (n = 3) not present in these cuts.
- Manual chamber measurements:
  - Conducted on 13 occasions during cut 1.
- Automatic chamber measurements:
  - Conducted for each chamber sequentially over a 30-minute period.

## Data quality and processing
- Quality control:
  - Flux data with R^2 < 0.6 are flagged (and effectively excluded/flagged by the note that these values are associated with the replacement rule).
  - Negative N2O values are replaced with zero.
- Instrumentation:
  - Combination of online analysis from automatic chambers and traditional manual static chambers, enabling cross-method comparison across treatments and controls.
- Data handling considerations:
  - For transparency and reproducibility, data originate from two measurement approaches and differ by cut and treatment assignment.

## Data coverage and limitations
- Temporal and spatial coverage:
  - Coverage differs by experimental cut period; manual chamber data limited to cut 1 (13 occasions) and absent in cuts 2 & 3 for most blocks.
  - In later cuts, block 4 has no data due to the use of only plots 1–12 with automatic chambers.
- Metadata and accessibility:
  - Dataset aims to be open with provenance to original originators; however, some data have been transformed (e.g., negative values reset to zero) and R^2-based filtering applied.
- Data structure implications for monitoring frameworks:
  - Mixed measurement modalities require harmonised metadata to enable comparability.
  - Clear handling rules for data quality flags (R^2 threshold) and data cleaning (negative value replacement) are essential for downstream analyses.

## Notes for monitoring framework authors
- This dataset demonstrates the importance of:
  - Documenting measurement methods and treatment/control allocations.
  - Recording blocking and plot-level design to interpret spatial variability.
  - Stating data quality criteria (e.g., R^2 threshold) and data cleaning rules.
  - Maintaining a record of changes across experimental cuts (e.g., transition from manual to automatic chambers and associated data gaps).
  - Ensuring metadata captures unit definitions and any transformations applied to raw measurements.

## Related documentation
- Supporting documentation: Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Primary data file: HF_N2O.csv