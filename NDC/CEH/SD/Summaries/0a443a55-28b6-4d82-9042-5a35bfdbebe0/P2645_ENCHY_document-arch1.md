# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

- Context and aims
  - Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) at Sourhope, Scottish Borders, to understand soil biodiversity and the functional roles of soil organisms in key ecological processes.
  - 24 projects examined soil structure, cycles (C and N), and micro- to macro-fauna; this component investigated Enchytraeidae diversity and their role in soil carbon cycling.

- Data collected
  - Enchytraeid abundance data
  - Delta 13C values of enchytraeid cholesterol (stable isotope data)
  - Treatments: Control vs lime-treated plots
  - Sampling dates: July 2000 and October 2000
  - Experimental design: five blocks, main plots (A–F), sub-plots, and cell grids

- Sampling design and methods
  - Sampling units: five blocks; main plots; sub-plots; 5 cm soil depth
  - Sampling events: July and October 2000
  - Extraction and counting: wet funnel method to extract enchytraeids; live specimens counted and identified morphologically, then genotyped with PCR-SSCP
  - Biomass estimation: average dry weights (Fridericia = 0.001 g; other genera = 0.0002 g)
  - In situ 13C pulse-labelling: 13C-enriched CO2 pulse (50 atom%) applied to vegetation in three blocks; control chambers received natural abundance CO2
  - Post-pulse sampling: days 11, 20, and 50 after pulse; enchytraeids extracted from cores; worms halved for spectroscopy and identification; halves prepared for isotope analysis

- Measurements and analysis
  - D13C values from enchytraeid cholesterol
  - Lipid extraction and derivatisation: BSTFA + 1% TMCS; GC-MS and GC-C-IRMS analyses
  - GC-MS: compound separation and identification via reference spectra
  - GC-C-IRMS: online combustion to CO2; isotopic ratios relative to PeeDee Belemnite; correction for BSTFA-derived carbons
  - Analytical accuracy: mean error around 0.48 ‰
  - Data corrections: cholesterol (uncorrected and corrected) values; corrections account for exogenous carbon from derivatisation

- Data structure and content
  - P2645_Enchy_13C_Cholesterol.csv: Delta 13C values of enchytraeid cholesterol
    - Key fields: BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, DAYS_AFTER_PULSE, ACTUAL_DATE, GENUS, SPECIES, ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, ERROR, CHOLESTEROL_DIFF
  - P2645_Enchy_Abundance_July2000.csv: Enchytraeid abundance July 2000
    - Key fields: SUID, LOC_ID, SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE
  - P2645_Enchy_Abundance_Oct2000.csv: Enchytraeid abundance October 2000
    - Key fields: SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE
  - Abundance conversion: ABUNDANCE represents numbers of enchytraeids per m2 (core area and conversion factor provided)

- Quality control and limitations
  - Verification included numeric range checks, formatting checks, and logical integrity checks
  - Data provided with QA but no warranty of accuracy or fitness for a specific use; no liability for losses or damages from use

- Provenance and references
  - Based on Sourhope Field Experiment and Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003)
  - Supporting references and methodological details available through the listed sources (e.g., EIDC catalogue, Usher et al., 2006)

- Relevance for analysis and potential uses
  - Enables correlations between Enchytraeid abundance and carbon assimilation (d13C) pathways
  - Allows assessment of lime treatment effects on soil biota and carbon cycling
  - Supports cross-dataset analyses with other Soil Biodiversity Programme data
  - Requires careful alignment of blocking structure (BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X/CELL_Y) and sampling dates for robust inference
  - Note on scope: local-scale, plot- and core-level data; integration with broader datasets may require harmonisation of units and metadata