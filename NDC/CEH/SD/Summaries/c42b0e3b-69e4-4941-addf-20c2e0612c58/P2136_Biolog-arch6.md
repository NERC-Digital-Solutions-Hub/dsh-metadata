# Substrate utilisation profiles and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, Scottish Borders.
- Aimed to understand soil biota diversity and functional roles in key ecological processes; supported multiple projects on soil structure, processes, and biota (microfauna to macro-fauna).

## Study site and sampling design
- Location: Sourhope experimental field site; temperate upland grassland; dominated by Agrostis capillaris.
- Plot type: Control plot; soils described as shallow, organic-rich brown forest soil on glacial till.
- Sampling dates: 8, 10, 14 July 1999; 5 October 1999; 3 April 2000; 30 August 2000.
- For each date: three replicate cores (2.5 cm diameter) to ~20 cm depth; cores separated into four 5-cm increments (0–5, 5–10, 10–15, 15–20 cm).
- Samples prepared for analysis: 1 g soil used for dry weight; remainder stored at -70°C prior to nucleic acid extraction and substrate utilisation analyses.

## BIOLOG-GN substrate utilisation analyses
- Processing: 9 ml of 0.5% soil suspension prepared, washed, and diluted; cells re-suspended in 20 ml PBS; 100 μl aliquots added to each well of 96-well BIOLOG-GN plates.
- Incubation: 18°C until color development ceased; scoring based on presence/absence of color change.
- Moisture measurement: moisture content calculated as mean of three replicate cores, oven-dried at 105°C for 24 h.

## Data structure and files
- Two CSV data files provided:
  - P2136_Biolog_Utilisation.csv: Biolog GN plate substrate utilisation profiles across sample dates and soil depths.
  - P2136_Soil_Moisture.csv: soil moisture percentages across sample dates and depths.
- Key variables and structure:
  - SAMPLING_DATE: date (data type: date).
  - MAX_DEPTH: maximum depth of core sample (cm) (numeric).
  - BIOLOG_CELL: Biolog cell identifier (text).
  - SUBSTRATE: substrate used (text).
  - SUBSTRATE_TYPE: substrate type (text).
  - UTILISATION: cell utilisation indicated by 1, otherwise 0 (numeric).
  - PERCENTAGE_MOISTURE: mean moisture (%) (numeric) for moisture file.

## Additional information and references
- Related publication: Griffiths, R. I., et al. (2003). Influence of depth and sampling time on bacterial community structure in an upland grassland soil. FEMS Microbiology Ecology, 43:35-43.
- Useful companion resources:
  - Sourhope Field Data Handbook 2003 (available via EIDC catalogue).
  - Usher, M.B., et al. (2006). Understanding biological diversity in soil: UK Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.
- Data disclaimer: Although QA procedures apply, NERC does not warrant data accuracy or fitness for a particular use and cannot be liable for any misuse or consequences arising from data use.