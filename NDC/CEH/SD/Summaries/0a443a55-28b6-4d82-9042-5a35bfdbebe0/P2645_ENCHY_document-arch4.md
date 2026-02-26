# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

## Overview and context
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope Farm, Scottish Borders, to study soil biota diversity and functional roles.
- Project 2645 focused on diversity and activity of Enchytraeidae and their role in soil carbon cycling.
- Data collected to quantify Enchytraeid abundance/biomass and delta 13C values from enchytraeid cholesterol, integrating field sampling with 13C pulse-labelling.

## Data collected
- Enchytraeid abundance and biomass in upland pasture.
- Delta 13C values of enchytraeid cholesterol (uncorrected and corrected for derivatization effects).
- Associated metadata: block, main plot, sub-plot, sampling date, treatment (control vs lime), and cell coordinates.

## Field and laboratory methods
- Sampling design: July and October 2000, five blocks; each block includes control and lime-treated main plots; multiple sub-plots and cells.
- Soil sampling: 5 cm depth, 5 cm diameter corer; wet funnel extraction to retrieve enchytraeids.
- Identification: live morphology initially, supplemented by PCR-SSCP genetic markers.
- Biomass: estimated from average dry weight per genus (Fridericia = 0.001 g; others = 0.0002 g).
- 13C pulse-labelling: in situ CO2 pulse with 50 atom% 13C; three replicates per treatment in pulsed and natural abundance conditions.
- Sampling post-pulse: days 11, 20, and 50; enchytraeids counted; halves of worms used for identification and isotope analysis.
- Isotope analysis: BSTFA derivatization, GC-MS for compound separation, GC-C-IRMS for delta 13C of cholesterol; corrections for exogenous carbons due to derivatization.
- Analytical accuracy: mean error ~0.48‰ for d13C measurements.

## Data structure and content
- Three CSV files:
  - P2645_Enchy_13C_Cholesterol.csv: Delta 13C values for enchytraeid cholesterol; fields include BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, DAYS_AFTER_PULSE, ACTUAL_DATE, GENUS, SPECIES, ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, ERROR, CHOLESTEROL_DIFF.
  - P2645_Enchy_Abundance_July2000.csv: Enchytraeid abundance July 2000; fields include SUID, LOC_ID, SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE.
  - P2645_Enchy_Abundance_Oct2000.csv: Enchytraeid abundance October 2000; fields include SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, GENUS, SP, COUNT, ABUNDANCE.
- Abundance calculations convert core counts to per square meter values using specified area factors.
- QC codes: 900 = Lost; 901 = Too Small.

## Quality control, provenance, and caveats
- Data validated with numeric range checks, formatting checks, and logical integrity checks.
- NERC disclaims warranty of data accuracy and fitness for a particular use; data provided without liability for loss or damage from use.
- Cited supporting information and methodology references available (e.g., Scott et al. 2003 Sourhope Field Data Handbook; Jones et al. 1991; Nielsen & Christensen 1959; O'Connor 1955; Ostle et al. 2000).

## Governance, standards, and reuse considerations
- Rich metadata describing experimental design (blocks, treatments, sampling dates, coordinates) supports data discoverability and interoperability within soil biodiversity datasets.
- Detailed methods and corrections (uncorrected vs corrected d13C; derivatization corrections) enhance reproducibility and cross-study comparisons.
- Data formats (CSV) and explicit column definitions facilitate integration into broader data systems and cross-network analyses.
- References to data stewardship and data availability channels (e.g., EIDC catalogue) indicate pathways for data access and provenance tracking.

## Practical implications for data leaders
- Highlights the importance of documenting experimental design, sampling regime, and correction procedures to enable reuse and meta-analysis.
- Demonstrates need for robust quality control and clear liability boundaries for data providers.
- Underlines value of providing comprehensive metadata and data dictionaries to support discovery, discovery, and cross-project data integration within networks focusing on soil biodiversity and carbon cycling.