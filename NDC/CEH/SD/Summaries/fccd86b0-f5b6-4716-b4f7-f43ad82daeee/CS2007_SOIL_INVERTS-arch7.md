# Soil invertebrate data 2007 [Countryside Survey], Great Britain

## Overview
- A dataset of soil invertebrate (mesofauna) counts from samples taken at a maximum of 256 1km squares across Great Britain during 2007, at a depth of 0–8 cm.
- Includes taxon-level counts (major taxa) and derived biodiversity metrics to support map-based analyses and spatial comparisons.

## Dataset structure and key fields
- File: CS2007_SOIL_INVERTS.csv
- Core identifiers:
  - SQUARE: 1km square sampling site code
  - PLOT: Plot identifier within each 1km square (one of 5 plots)
  - YEAR: Survey year
- Taxon counts (example codes; all are numeric):
  - ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, COEN, CONE, COPU, COSM, COPE, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN, TOTAL_CATCH
- Summary/diversity metrics:
  - COLL_TOTAL: total collembolan
  - AC_COLL_TOTAL: total acari mites and collembolan
  - MC_RATIO: mites-to-springtails ratio (in soils, 0–8 cm)
  - TOTAL_TAXA: total invertebrate taxa richness per core
  - SHANNON: Shannon diversity index (invertebrates)
  - LC07, LC07_NUM: ITE Land Class 2007 (text and numeric code)
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: county or council name (as applicable)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Other notes:
  - 921 soil cores analysed; 3–5 cores randomly selected from 5 plots per square across 256 1km squares
  - 0–8 cm depth; extraction via dry Tullgren method; preserved in 70% ethanol
  - Identification to major taxa; Collembola and mites identified to morphotype level for finer resolution

## Spatial scope and GIS implications
- Spatial resolution: 1km square units across Great Britain
- Coverage: 591 squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland)
- Suitable for GIS workflows when joined to a 1km grid or mapped as a grid-based layer
- Rich attribute data for each square/plot enabling spatial analyses of biodiversity, land class, and environmental context (LC07, COUNTRY, EZ_DESC_07)

## Data collection, processing, and quality assurance
- Field and lab protocols:
  - Soil cores collected from top 0–8 cm (later surveys used different corner sampling; 2007 used western corner of Main Plots)
  - Tullgren extraction over 5 days; collection in 70% ethanol
  - Identification to Taxonomic level 1; Collembola and mites to morphotype level
- Quality control:
  - After initial identifications, 10% of first 500 samples re-counted and re-identified; additional verification at decreasing sample sizes (5% for next 300, 2% for final 252)
  - No significant differences found between original and validated data via t-tests
  - Acknowledges potential small losses of the very smallest taxa during transfer between sample tubes
- Quality assurance and governance:
  - Adheres to Defra/NERC Codes of Practice
  - Documentation and protocols summarized in Countryside Survey Soils Manual (2008)

## Usage, attribution, and references
- Data usage and dissemination require acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; All rights reserved
- Key sources and protocols:
  - Countryside Survey: Soils Manual (Emmett et al., 2008)
  - Countryside Survey Technical Report No. 3/07: Soils Manual
  - Related Land Classification and Countryside Survey publications (various years)
- Access to full methodologies and data handling is described in the CS2007 Soils Manual and associated CS Technical Reports

## Practical considerations for GIS specialists
- Data integration:
  - Join CS2007_SOIL_INVERTS.csv to a 1km square polygon grid using the SQUARE field
  - Leverage LC07, COUNTRY, COUNTY07, EZ_DESC_07 to enrich maps with environmental context
- Metric interpretation:
  - Use TOTAL_CATCH and TOTAL_TAXA for abundance and richness mapping
  - Use SHANNON for diversity mapping; MC_RATIO for community structure (mites vs. springtails)
  - Taxon-specific counts enable targeted habitat or soil health analyses
- Data quality and limitations:
  - Depth fixed at 0–8 cm; cross-check with other soil layers if integrating multi-depth data
  - Sampling design is stratified by Land Classes; results are designed for national and country-level reporting
  - Be mindful of potential small taxa losses during sample processing when interpreting fine-scale patterns
- Documentation and provenance:
  - Follow CS Soils Manual guidelines for any further processing or analysis
  - Maintain proper attribution when publishing maps or analyses derived from this dataset