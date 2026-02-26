# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

- Context: Part of the NERC Soil Biodiversity Thematic Programme (est. 1999) studying soil biota diversity and functional roles in ecological processes at Sourhope, Scottish Borders. Project 2645 focused on diversity and activity of Enchytraeidae and their role in soil carbon cycling.

- Data collected
  - Enchytraeid abundance and biomass measurements (July and October 2000) from control and lime-treated main plots across five blocks.
  - Delta 13C values from enchytraeid cholesterol measured after in situ 13C pulse labeling of vegetation (Sept 28, 2000).

- Sampling and measurement overview
  - Soil sampling: 5 cm depth using 5 cm diameter cores from each main plot; samples taken across blocks, stored at 4°C, processed within 1 week.
  - Abundance workflow: wet funnel extraction; worms counted and identified (live specimens initially; genetic markers used later). Biomass estimated from average dry weights (Fridericia = 0.001 g; others = 0.0002 g).
  - Stable isotope labeling: SID system delivered 13C-enriched CO2 to pulse chambers in three blocks; three replicates per treatment (Control and Lime) per block.
  - Sampling after labeling: soil cores collected on days 11, 20, and 50; enchytraeids extracted, counted, and halved for identification (PCR-SSCP) and isotope analysis (half frozen for analysis).

- Measurement details
  - d13C values from enchytraeid cholesterol measured by:
    - BSTFA + 1% TMCS derivatization.
    - GC-MS for compound separation and identification.
    - GC-C-IRMS for relative 13C isotope values, with calibration to PeeDee Belemnite standard.
  - Corrections: adjust d13C values for BSTFA-derived exogenous carbon atoms; analytical error ~0.48 ‰.

- Data structure (three CSV files)
  - P2645_Enchy_13C_Cholesterol.csv
    - Columns include BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, DAYS_AFTER_PULSE, ACTUAL_DATE, GENUS, SPECIES, ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, ERROR, CHOLESTEROL_DIFF.
  - P2645_Enchy_Abundance_July2000.csv
    - Columns include SUID, LOC_ID, SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE.
  - P2645_Enchy_Abundance_Oct2000.csv
    - Columns include SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, GENUS, SP, COUNT, ABUNDANCE.

- Quality control and caveats
  - QA steps: numeric range checks, format checks, and logical integrity checks.
  - NERC provides no warranty on data accuracy or fitness for a particular use; no liability for data usage.
  - Data represent a historical dataset with methodological specifics that users should consider when integrating with other data.

- References and provenance
  - Key methodological and contextual references are provided, including Scott et al. 2003 (Sourhope Field Data Handbook), and foundational works on enchytraeid taxonomy and stable isotope analyses.