# Substrate utilisation profiles and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland [NERC Soil Biodiversity Programme] - Supporting Information

- Purpose and context
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, focusing on soil biodiversity and the functional roles of soil organisms.
  - Aimed to understand bacterial community ecology and how agriculture and climate change may affect biodiversity and ecosystem functioning in Britain's remaining native grasslands.

- Study site and design
  - Location: Sourhope experimental field site, Scottish Borders, UK (grid NT854196); temperate upland grassland (SH).
  - Soil: shallow, organic-rich brown forest soil over glacial till derived from andesitic lava.
  - Plot type: control plot; unimproved grazed pasture dominated by grasses (e.g., Agrostis capillaris).

- Sampling regime
  - Dates: 8, 10, 14 July 1999; 5 October 1999; 3 April 2000; 30 August 2000.
  - For each date: three replicate cores per sample, 2.5 cm diameter, to ~20 cm depth.
  - Depth increments: cores split into four 5-cm layers (0–5 cm, 5–10 cm, 10–15 cm, 15–20 cm); distinct stratification observed (organic vs mineral horizons).

- Laboratory methods
  - Subsample processing: 1 g soil for dry weight; remainder stored at -70°C prior to nucleic acid extraction and BIOLOG analyses.
  - BIOLOG-GN substrate utilisation: prepared soil suspensions (0.5% w/v), washed and inoculated into BIOLOG GN plates; plates incubated at 18°C until color development ceased; scoring of substrate utilisation as present/absent (color change).
  - Moisture measurement: percentage moisture determined as mean of three replicate cores; soils oven-dried at 105°C for 24 h.

- Data products (two CSV files)
  - BIOLOG substrate utilisation data: Substrate utilisation profiles (BIOLOG GN plates) for samples from 1999 and 2000; three cores per sample date per depth.
  - Soil moisture data: Percentage moisture content for the same samples (mean of three replicate cores).

- Data structure and key fields
  - Substrate utilisation file (P2136_Biolog_Utilisation.csv) includes:
    - SAMPLING_DATE (date)
    - MAX_DEPTH (cm)
    - BIOLOG_CELL (text)
    - SUBSTRATE (text)
    - SUBSTRATE_TYPE (text)
    - UTILISATION (numeric; 1 if substrate utilisation detected, 0 otherwise)
  - Soil moisture file (P2136_Soil_Moisture.csv) includes:
    - SAMPLING_DATE (date)
    - MAX_DEPTH (cm)
    - PERCENTAGE_MOISTURE (numeric, %)
  - Documentation notes provide column descriptions, units, and data types.

- Related information and references
  - Influences on bacterial community structure and soil biodiversity discussed in Griffiths et al. (2003).
  - Sourhope Field Data Handbook (2003) and Usher et al. (2006) provide broader context for UK soil biodiversity research.
  - Data available via the EIDC catalogue; includes QA steps but no warranty on accuracy by NERC.

- Usage notes and caveats
  - Data are subject to quality assurance; NERC does not warrant accuracy or fitness for a specific use and bears no liability for misuse or results obtained from the data.
  - The datasets are designed for integration with broader environmental monitoring and biodiversity analyses, enabling cross-dataset comparisons and temporal studies.