# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999) focusing on soil biota diversity and function at the Sourhope field site (Scottish Borders, grid reference NT8545019630).
- Project 2645 studied diversity and activity of Enchytraeid worms and their role in soil carbon cycling over a one-year period.
- Data cover Enchytraeid abundance and delta 13C values in cholesterol, to link worm communities with carbon turnover.

## Data Content
- Three CSV data files:
  - P2645_Enchy_13C_Cholesterol.csv: Delta 13C values of enchytraeid cholesterol.
  - P2645_Enchy_Abundance_July2000.csv: Enchytraeid abundance in July 2000.
  - P2645_Enchy_Abundance_Oct2000.csv: Enchytraeid abundance in October 2000.
- Measurements and variables include:
  - Sampling design: blocks (1–5), main plots (A–F), sub-plots, and cell coordinates (CELL_X, CELL_Y).
  - Treatments: Control vs. lime-treated (TREATMENT).
  - Temporal aspect: days after 13CO2 pulse; sampling dates (ACTUAL_DATE or SAMPLING_DATE).
  - Enchytraeid data: genus and species (GENUS, SPECIES, SP), counts (COUNT), derived abundance per m² (ABUNDANCE), and sampling unit identifiers (SUID, LOC_ID for abundance files).
  - Isotopic data: D13C_CHOLESTEROL_UNCORRECTED and D13C_CHOLESTEROL_CORRECTED with associated ERROR and CHOLESTEROL_DIFF.
  - Quality control: QC_CODE (e.g., 900 = Lost, 901 = Too Small) and ANALYSIS_CODE linking to GC-c-IRMS analyses.

## Methods and Provenance
- Field sampling: July and October 2000 across five blocks; soil samples to 5 cm depth using a 5 cm diameter corer. Samples stored at 4°C and processed promptly.
- Enchytraeid extraction and identification:
  - Wet funnel extraction; live counts by morphology, followed by genetic confirmation (PCR-SSCP).
  - Biomass estimates: average dry weight per worm (Fridericia = 0.001 g; others = 0.0002 g).
- Isotopic tracing:
  - In situ 13C pulse-labelling of vegetation using a mobile SID system; three replicate plots per treatment and per block in early 2000.
  - Post-pulse sampling occurred at days 11, 20, and 50 after pulse.
  - Lipids extracted from half-worms, derivatized with BSTFA+TMCS, and analyzed by GC-MS and GC-C-IRMS for 13C in cholesterol.
- Analytical workflow:
  - GC-MS for compound separation and identification.
  - GC-C-IRMS for precise δ13C values, corrected for exogenous carbon in derivatization.
  - Mean analytical error reported as 0.48 ‰.
- Documentation and references for methods provided (e.g., O'Connor 1955; Nielsen & Christensen 1959; Jones et al. 1991; Ostle et al. 2000; Scott et al. 2003).

## Data Structure and Metadata
- Data files are structured with detailed field descriptions and data types:
  - Core fields across files include BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, DAYS_AFTER_PULSE, ACTUAL_DATE/SAMPLING_DATE, and Genus/SPECIES information (where applicable).
  - Abundance files include SUID, LOC_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE.
  - Cholesterol isotopic file includes ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, ERROR, CHOLESTEROL_DIFF, and related fields.
- Descriptions emphasize experimental design alignment with Scott et al., 2003, and provide data type guidance (Text, Number, Date).
- Data alignment notes: detailed provenance links and cross-references to supporting information with EIDC catalogue record.

## Quality Assurance and Limitations
- QA steps include numeric range checks, formatting conformity, and logical integrity checks.
- Data are subject to quality assurance but the issuing body (NERC Soil Biodiversity Programme) does not warrant accuracy or fitness for a specific use.
- Liability disclaimer: no responsibility for loss or damage arising from use of the data.

## Access, Usage, and Rights
- Data are provided as Supporting Information and available via the EIDC catalogue record.
- Accompanying methodological detail, references, and dataset descriptions support reuse and integration with related soil biodiversity datasets.

## References and Documentation
- Jones, D.M. et al. 1991. Determination of δ13C values by GC-IRMS.
- Nielsen, C.O. & Christensen, B. 1959. The Enchytraeidae taxonomy.
- O'Connor, F.B. 1955. Extraction of enchytraeid worms.
- Ostle, N. et al. 2000. In situ 13C pulse labelling.
- Scott, J. et al. 2003. Sourhope Field Data Handbook.
- Usher, M.B. et al. 2006. UK Soil Biodiversity Programme.