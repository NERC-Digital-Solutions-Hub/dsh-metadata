# Substrate utilisation profiles and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland [NERC Soil Biodiversity Programme] - Supporting Information

- Context and aims
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, Scottish Borders.
  - Aimed to understand soil biodiversity and functional roles of soil organisms in key ecological processes; involved 24 projects on soil structure, processes, and micro/macro-fauna.
  - Focus of this data: bacterial community ecology in Britain’s native grasslands; temporal and spatial diversity across soil depths; assessment of carbon source utilisation (Biolog-GN) for a subset of the community.

- Study site, sampling design, and scope
  - Control plot at Sourhope experimental field site; temperate upland grassland.
  - Sampling dates: 8, 10, 14 July 1999; 5 October 1999; 3 April 2000; 30 August 2000.
  - For each date: three replicate cores (2.5 cm diameter, ~20 cm depth); cores stratified into 0–5 cm (litter/organic), 5–10 cm, 10–15 cm (organic/mineral mix), 15–20 cm (mineral horizon).
  - Samples stored at -70 C prior to analyses; 1 g used for dry weight, remainder stored for molecular and substrate analyses.
  - Sampling outside main plots and from untreated soil.

- BIOLOG-GN substrate utilisation analyses
  - 9 ml of 0.5% soil suspension prepared, washed to remove impurities, and inoculated into 96-well BIOLOG-GN plates.
  - Plates incubated at 18°C; presence/absence of colour change used to indicate substrate utilisation.
  - Moisture content for each sample determined as mean of three replicate cores via oven drying.

- Data products and structure
  - Two CSV data files:
    - P2136_Biolog_Utilisation.csv — BIOLOG GN substrate utilisation profiles.
    - P2136_Soil_Moisture.csv — soil moisture percentages.
  - Key fields (Biolog file):
    - SAMPLING_DATE, MAX_DEPTH, BIOLOG_CELL, SUBSTRATE, SUBSTRATE_TYPE, UTILISATION (1 = utilisation, 0 = no utilisation).
  - Key fields (Moisture file):
    - SAMPLING_DATE, MAX_DEPTH, PERCENTAGE_MOISTURE (mean of three cores).
  - Data types documented: date, numeric, text.

- Documentation, references, and ancillary resources
  - Related publication: Griffiths et al. 2003 on influence of depth and sampling time on bacterial community structure (FEMS Microbiology Ecology).
  - Sourhope Field Data Handbook (2003) and EIDC catalogue for supporting information.
  - Cited UK Soil Biodiversity Research Programme article (Usher et al. 2006).

- Data quality, usage, and liability
  - Data are subject to quality assurance procedures; no warranty on accuracy or fitness for specific uses.
  - NERC cannot be held liable for losses or damages arising from use of these data.