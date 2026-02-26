# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

## Background
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) at Sourhope, Scottish Borders.
- Aimed to understand soil biodiversity and functional roles of soil biota in key ecological processes.
- Project 2645 focused on diversity and activity of Enchytraeidae in upland pasture and their role in soil carbon cycling.
- Investigated Enchytraeid abundance and the delta 13C values of enchytraeid cholesterol.

## Data collected
- Enchytraeid abundance and biomass estimates.
- Delta 13C values (d13C) of enchytraeid cholesterol.
- Data collected on control and lime-treated plots across five experimental blocks in July and October 2000.

## Study design and sampling
- Experimental setup: five blocks with control and lime-treated main plots.
- Soil sampling: cores to 5 cm depth using 5 cm diameter corers from all blocks; July and October 2000.
- Enchytraeid extraction: wet funnel method; worms counted and identified initially morphologically, later with genetic markers (PCR-SSCP).
- In situ 13C pulse-labelling: 13CO2 pulse over 10 daylight hours on 28 Sept 2000 using SID system; three replicate plots per treatment and sampling in both pulsed and natural abundance conditions.
- Within each plot: soil cores collected at days 11, 20, and 50 after pulse; half worms used for identification, half for isotopic analysis; specimens dried freeze-dried for analysis.

## Measurement details
- Isotopic analysis: lipids from half-worms extracted and derivatized (BSTFA + 1% TMCS); GC-MS for compound separation and verification; GC-C-IRMS for delta 13C measurements relative to PeeDee Belemnite standard.
- Corrections: adjust for exogenous carbon from BSTFA-derived trimethylsilyl groups; mean analytical error ~0.48 ‰.
- Instrumental setup: detailed GC and IRMS parameters (columns, temperatures, ramp rates, reactors) specified.

## Data structure and files
- P2645_Enchy_13C_Cholesterol.csv: Delta 13C values of enchytraeid cholesterol.
  - Key fields: BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), DAYS_AFTER_PULSE, ACTUAL_DATE, GENUS, SPECIES, ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, CHOLESTEROL_DIFF, ERROR, etc.
- P2645_Enchy_Abundance_July2000.csv: Enchytraeid abundance in July 2000.
  - Key fields include SUID, LOC_ID, SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE.
- P2645_Enchy_Abundance_Oct2000.csv: Enchytraeid abundance in October 2000.
  - Key fields include SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE, and taxonomic fields (GENUS, SP).

## Quality control and data provenance
- Verification included numeric range checks, formatting conformity, and logical integrity checks.
- Data are subject to quality assurance but do not come with guaranteed accuracy or suitability for a specific use.
- NERC disclaims responsibility for any loss or damage arising from data use; no liability for data accuracy.

## Context for monitoring and potential uses
- Provides a time-stamped, standardized dataset linking soil fauna (Enchytraeidae) to carbon turnover via 13C-enriched labelling.
- Enables examination of how soil biodiversity and functional activity relate to carbon cycling under different soil treatments (control vs lime).
- Useful for meta-analyses and integrative environmental monitoring when combined with other soil biodiversity and biogeochemical datasets.
- Highlights the importance of sharing underlying data to enhance interoperability and secondary analyses.