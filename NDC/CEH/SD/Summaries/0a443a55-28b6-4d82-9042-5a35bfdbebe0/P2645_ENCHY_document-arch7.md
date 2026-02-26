# Enchytraeid worm abundance and delta 13C cholesterol data from Sourhope field experiment site, Scotland, 2000 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope field site, aiming to study soil biodiversity and functional roles in carbon and nitrogen cycles.
- 24 research projects; this component (Project 2645) focuses on diversity and activity of Enchytraeidae and their role in soil carbon cycling.
- Data include Enchytraeid abundance and delta 13C values of enchytraeid cholesterol, with isotopic labelling used to trace carbon assimilation.

## Data collected
- Enchytraeid abundance and biomass estimates from soil cores.
- Delta 13C values (d13C) of enchytraeid cholesterol, derived from isolated worms.
- Sampling across five blocks with control and lime-treated main plots, in July and October 2000.
- Isotopic pulse-labelling of above-ground vegetation with 13C-enriched CO2 for tracing C uptake.

## Sampling and measurement methods
- Soil sampling: July and October 2000, 5 cm depth, 5 cm diameter cores; five experimental blocks; control and lime-treated plots.
- Extraction and counting: Wet funnel method; worms counted and initially identified morphologically, then by genetic markers (PCR-SSCP).
- Biomass estimates: average dry weight—Fridericia genus 0.001 g; other genera 0.0002 g.
- Isotopic labelling: 13C-enriched CO2 pulse (50 atom % 13C) in 3 replicate plots per treatment; sampling at days 11, 20, and 50 post-pulse.
- Sample processing: worms halved; one half for identification, the other half for stable-isotope analysis after freeze-drying.
- Chemical analysis: derivatization with BSTFA+1% TMCS; GC-MS for compound separation; GC-C-IRMS for 13C isotopic ratios.
- Isotopic correction: corrections for exogenous carbon in derivatization group; calibration against PeeDee Belemnite standard; mean analytical error about 0.48 ‰.

## Data structure and content
- Three CSV data files:
  - P2645_Enchy_13C_Cholesterol.csv: Delta 13C values of enchytraeid cholesterol
    - Fields include BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, DAYS_AFTER_PULSE, ACTUAL_DATE, GENUS, SPECIES, ANALYSIS_CODE, QC_CODE, D13C_CHOLESTEROL_UNCORRECTED, D13C_CHOLESTEROL_CORRECTED, ERROR, CHOLESTEROL_DIFF
  - P2645_Enchy_Abundance_July2000.csv: Enchytraeid abundance (July 2000)
    - SUID, LOC_ID, SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE
  - P2645_Enchy_Abundance_Oct2000.csv: Enchytraeid abundance (October 2000)
    - SAMPLING_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SUB_SAMPLE, COUNT, ABUNDANCE, GENUS, SP, COUNT
- Descriptions and units included for each field; detailed metadata aligns with Scott et al., 2003 data handbook.

## Data processing and isotopic analysis
- GC-MS used to separate compounds; compound identities assigned via mass spectra.
- GC-C-IRMS measured stable carbon isotopes after combustion; data corrected for BSTFA derivatization.
- Isotopic values reported relative to PeeDee Belemnite standard.

## Quality assurance and limitations
- Verification steps included numeric range checks, formatting conformity, and logical integrity assessments.
- Data are subject to quality assurance, but NERC cannot warrant accuracy or fitness for any particular use; no liability for data use or results.

## Spatial and temporal context for GIS use
- Spatial schema: Block (1-5), Main Plot (A-F), Sub-Plot, and a grid with CELL_X and CELL_Y coordinates, enabling mapping of abundance and isotopic values across the Sourhope site.
- Temporal scope: two sampling campaigns (July and October 2000) and a 13C pulse labelling event on 28 September 2000.
- Data suitable for map-based visualization of Enchytraeidae abundance and carbon tracing via 13C-enriched cholesterol, across treatments and blocks.

## References / Further reading
- Jones, D.M. et al. 1991. Determination of d13C values of alcohols by GC-IRMS.
- Nielsen, C.O. & Christensen, B. 1959. The Enchytraeidae: taxonomy.
- O'Connor, F.B. 1955. Extraction of enchytraeid worms.
- Ostle, N. et al. 2000. In situ CO2-C-13 pulse labelling system.
- Scott, J. et al. 2003. SOURHOPE FIELD DATA HANDBOOK.
- Usher, M.B. et al. 2006. Understanding biological diversity in soil.
- Additional references provided within the dataset documentation for laboratory methods and isotope corrections.