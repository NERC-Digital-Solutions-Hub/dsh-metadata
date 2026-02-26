# Survey of British calcareous grasslands, 1990 and 2007. Dataset Summary

## Overview
- National-scale survey of calcareous grasslands in Britain conducted during 1990–1993 and a resurvey in 2007 (2006–2009).
- Aims to be repeatable with minimal observer bias; plots are representative of calcareous grasslands and managed nature reserves.
- Data include vegetation and soil measurements collected using standardized methods.
- Available via the NERC Environmental Information Data Centre (EIDC) with a DOI.

## Data Scope
- Geographic coverage: Britain.
- Time period:
  - 1990 survey: 1990–1993; 128 plots across 56 sites.
  - 2007 survey: 2006–2009; 48 plots (per site) across 35 of the 56 sites.
- Data types:
  - Vegetation data: vascular plants, bryophytes, and macro lichens (1990); bryophytes and lichens not recorded in 2007.
  - Soil data: pH (top 10 cm), soil organic content, and various chemical constituents (NO3-, NH4+, Ca2+, Na+, Mg2+, K+, Al3+, plant-available P via Olsen extraction), NaCl extracts, and moisture-corrected organic matter.
  - Site-level metadata: National Vegetation Classification (NVC), altitude, aspect, slope, coastal status, soil type, etc.
- Documentation includes key publications on climate change, air pollution, and nitrogen deposition impacts on calcareous grasslands.

## Sampling Design & Methods
- Plot design:
  - Fixed 12 x 12 m plots (typically 12 x 12 m; some 6 x 24 m) with permanent copper marker loops for relocation (7 loops per plot, buried 5–15 cm, designed to last >20 years).
  - Each plot subdivided into four 6 x 6 m blocks, further into nine 2 x 2 m units; a total of 36 sub-quadrats per plot.
- Vegetation sampling:
  - Within each plot, 36 quadrats of 0.5 x 0.5 m are used to record presence/absence (frequency) of vascular plants, bryophytes, and macro lichens.
  - Species are grouped into grasses, other herbs, and lower plants; growth form data collected for selected dominants.
  - Vouchers collected for difficult taxa; detailed notes recorded to aid interpretation.
- Soil sampling:
  - Soil pH measured in 1990 in the field; 2007 samples collected in top 10 cm, stored and analyzed in the lab.
  - Chemical analyses include plant-available P (Olsen), NO3-, NH4+, base cations, Al, and organic matter via loss on ignition.
- Relocation and data quality:
  - Relocation accuracy around 5 cm; data capture time per plot varies from 3 to 12 hours; grid setup about 45 minutes.
  - Data handling uses VESPAN II and MATCH for alignment with NVC plant communities; frequency data used to derive constancy classes.
- Data limitations:
  - 1990 data include bryophytes; 2007 data do not, reducing comparability for bryophyte components.
  - The sampling technique yields presence/absence frequencies rather than general cover estimates; plots are not directly comparable to other datasets outside this method.

## Data Structure & Files
- CG_SITES.csv: site-level metadata (site name, status, year, OS grid references, NVC, soil pH, altitude, aspect, slope, coastal flag, notes, organic content, ammonium, nitrate, average soil depth, soil type).
- CG_VEG.csv: vegetation data per plot per year (plot ID, year, species recorded, BRC reference numbers, growth form, and count of occurrences across 36 quadrats).
- Data lineage and keys:
  - PLOT_ID: unique plot identifier (plot number + year).
  - PLOT: numerical plot number.
  - SITE: site name.
  - YEAR: survey year.
  - OSGR/EASTING/NORTHING: position data.
  - NVC/PH/ALT/ASPECT/SLOPE/COASTAL: site attributes.
  - AMMONIUM/NITRATE/AVE_SOIL_DEPTH/SOIL_TYPE: soil chemistry and context.
  - CG_VEG includes SPECIES_REC, BRC_NUM, BRC_NAME, COUNT, GROWTH.
- Notes:
  - 999 denotes no data in the CSVs.
  - 2007 dataset excludes bryophytes; 1990 dataset includes bryophytes and lichens.

## Data Quality, Standards & Limitations
- Strengths:
  - Standardized, repeatable survey methodology designed for relocation and longitudinal comparison.
  - Comprehensive metadata and structured data capture enabling integration and analysis with vegetation classification frameworks (NVC) and related publications.
  - Robust sampling design with multiple plots across diverse geographic/climatic contexts and management regimes.
- Limitations:
  - Bryophyte data not collected in 2007, reducing year-to-year comparability for bryophytes.
  - Frequency-based presence/absence data; lack of broad cover estimates for all taxa.
  - Relocation markers rely on copper loops which may be affected by marker loss; some plots data missing from 1990 (data recovered for 121 plots instead of 128).
  - The method is unique and not directly directly comparable with other datasets outside this approach.

## Provenance, Access & References
- Origin: 1990 – DoE Contract; 2007 – NERC Grant; principal investigators: Rich, Cooper, Rodwell, Malloch, Van Den Berg, Vergeer, Smart, Guest, Ashmore.
- Dataset citation:
  - Rich, T.C.G. et al. (2015). Survey of British calcareous grasslands, 1990 and 2007. NERC Environmental Information Data Centre. https://doi.org/10.5285/38a73c7b-3e3c-4517-a33f-bd28b292b9e1
- Analytical tools referenced: VESPAN II, MATCH; data interpretation aligned with British Plant Communities.

## Considerations for Data Leaders
- Data governance:
  - Clear documentation of sampling design, metadata fields, and data processing steps facilitates reuse and integration into broader data ecosystems.
  - Data accessible via a persistent DOI and centralized data archive (NERC EIDC); evaluate ongoing update and maintenance plans.
- Data system planning:
  - The dataset demonstrates a robust, repeatable methodology with explicit relocation and sampling protocols, useful as a blueprint for long-term ecological monitoring data systems.
  - Metadata should emphasize method reproducibility, data lineage, and comparability constraints (e.g., year-to-year bryophyte coverage differences).
- User needs and dissemination:
  - Provides structured CSVs with explicit field definitions, enabling policy, conservation, and ecology teams to extract plot-level trends, species constancy, and soil-vegetation interactions.
  - Potential to integrate with other calcareous grassland datasets for broader analyses of climate change and deposition impacts.