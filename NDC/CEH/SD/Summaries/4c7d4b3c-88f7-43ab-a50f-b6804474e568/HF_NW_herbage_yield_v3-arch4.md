# Details of data structure to ' HF_NW_herbage_yield.csv '

## Overview
- Supplement to supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Describes the data structure for HF_NW_herbage_yield.csv
- Dataset characteristics: 7 columns, 96 rows
- Source data from grassland fertiliser trials conducted in 2016 at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research)

## Dataset context
- Represents herbage yield data from grassland fertiliser experiments
- Trials conducted at two sites: HF (Henfaes) and NW (North Wyke)
- Experimental design details embedded in the dataset (randomised block design with blocks and plots)

## Column definitions (7 columns)
- Date: Date of grass cut
- Site: HF or NW indicating trial location
- N_app: Fertiliser application level (1, 2, or 3)
  - 1st & 2nd applications at 90 kg ha-1
  - 3rd application at 60 kg ha-1
- Block: Blocking factor of the randomised block design (1–4)
- Plot: Plot identifier within a block (1–16); plot size 2 × 6 m
- Treatment: Fertiliser type (AN, U, IU, C)
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
  - C = 0N control
- Dry_tonnes_ha: Dry-weight yield of grass, expressed in tonnes per hectare

## Data provenance and usage context
- Data derive from the 2016 grassland fertiliser trials, enabling comparison of fertiliser types and application levels across two sites
- Dataset complements broader CINAg experimentation documentation (referenced supporting documentation and final check version)

## Implications for data governance and utilization (Data Leaders perspective)
- Metadata richness: clear column definitions and units support data discoverability and reuse
- Provenance: link to supporting documentation and trial context aids validation and reproducibility
- Standardization: consistent coding for sites, treatments, and plot/block identifiers facilitates cross-study aggregation
- Data quality considerations: explicit date, site, and treatment fields enable filtering, validation, and trend analysis
- Accessibility and updates: structured format and documentation support easier data updates and integration with data platforms
- Collaboration potential: dual-site data with a unified schema supports broader sharing within and across networks of partners