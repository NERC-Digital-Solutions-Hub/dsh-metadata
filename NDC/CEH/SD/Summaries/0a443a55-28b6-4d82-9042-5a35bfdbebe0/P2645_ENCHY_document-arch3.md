# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

- Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) conducted at Sourhope, aiming to understand soil biodiversity and the functional roles of soil biota; 24 projects funded, including Project 2645 on Enchytraeidae diversity and activity.
- Focus of the dataset: Enchytraeid abundance and delta 13C values of enchytraeid cholesterol to study their role in soil carbon cycling.

## Data Collected and Study Context

- Measurements include:
  - Enchytraeid abundance (counts) and biomass estimates
  - delta 13C values from enchytraeid cholesterol
- Experimental design:
  - Sampling in July and October 2000 across five blocks
  - Treatments: control and lime-treated main plots
  - 5 cm soil depth sampling using a 5 cm diameter corer
- Isotopic labeling:
  - In situ pulse-labeling of above-ground vegetation with 13C-enriched CO2 on 28 September 2000
  - SID system with three replicate plots for each treatment
  - Post-pulse soil sampling on days 11, 20, and 50
- Enchytraeids:
  - Identified morphologically and via genetic markers
  - Biomass estimated from species-specific dry weights
- Data are organized into three CSV datasets detailing cholesterol isotopes and Enchytraeid abundance.

## Methods and Measurement

- Enchytraeid extraction and counting:
  - Wet funnel extraction from soil cores
  - Live counts initially by morphology; confirmation with genetic markers
- Isotopic analysis:
  - Extraction and derivatization of cholesterol (BSTFA + 1% TMCS) for GC-MS and GC-C-IRMS
  - GC-MS used for compound separation and identification
  - GC-C-IRMS used to determine delta 13C values relative to PeeDee Belemnite
  - Correction for three exogenous carbon atoms from derivatization
  - Analytical mean error reported as 0.48 ‰
- Data handling:
  - Data quality control includes numeric range checks, formatting, and logical integrity checks
  - Results include both uncorrected and corrected delta 13C values for enchytraeid cholesterol
- References and methodological context provided (e.g., pulse labeling technique, O’Connor extraction method, and standard references).

## Data Structure and Formats

- P2645_Enchy_13C_Cholesterol.csv
  - Fields include: BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, DAYS_AFTER_PULSE, ACTUAL_DATE, GENUS, SPECIES, ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, ERROR, CHOLESTEROL_DIFF, CHOLESTEROL_DIFF
- P2645_Enchy_Abundance_July2000.csv
  - Fields include: SUID, LOC_ID, SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE
- P2645_Enchy_Abundance_Oct2000.csv
  - Fields include: SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SP, COUNT, ABUNDANCE
- Abundance conversion notes:
  - ABUNDANCE represents numbers of Enchytraeid worms per square metre, derived from core counts with a specified conversion factor.

## Quality Assurance and Limitations

- Verification steps: numeric range checks, formatting conformity, and logical integrity checks
- Data are subject to QA procedures, but the issuing body disclaimers that they cannot warrant accuracy or fitness for a particular use
- The issuing organization (NERC) does not assume liability for data use or consequences arising from its use
- Documentation includes detailed data dictionaries and methodological descriptions to aid interpretation and reuse

## Access and References

- Supporting information noted as available via the EIDC catalogue record (Sourhope Field Data Handbook, 2003)
- Key references for methods and context:
  - Jones et al. 1991; Nielsen & Christensen 1959; O’Connor 1955; Ostle et al. 2000
  - Scott et al. 2003. Sourhope Field Data Handbook 2003
  - Usher et al. 2006. Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme
- Data integrates with broader Soil Biodiversity Programme outputs and supports linking soil fauna diversity with carbon turnover processes. 

## Relevance for Monitoring Frameworks

- Demonstrates integration of biological indicators (Enchytraeid abundance) with functional isotopic tracers (delta 13C in cholesterol) to assess soil carbon cycling mechanisms.
- Highlights critical data governance needs for monitoring frameworks:
  - Rich metadata and clear data dictionaries for multi-dataset integration
  - Standardized data formats and field definitions (BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X/Y)
  - Documentation of data provenance, processing steps, and corrections (e.g., BSTFA derivatization corrections)
- Exposes practical barriers typical for monitoring datasets:
  - Metadata completeness and data sharing considerations
  - Commitment to data quality assurance while recognizing limitations on guarantee of accuracy
  - Need for transparent data lineage and explicit data governance to enable reuse in policy evaluation and decision-making