# Substrate utilisation profiles and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland [NERC Soil Biodiversity Programme] - Supporting Information

- Purpose and context
  - Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) focused on understanding soil biodiversity and the functional roles of soil organisms in ecosystem processes at Sourhope, Scottish Borders.
  - Data describe bacterial functional potential via substrate utilisation (BIOLOG-GN) and soil moisture, aimed at assessing temporal and spatial variability in semi-natural grassland soils.

- Data products included
  - BIOLOG GN Substrate utilisation profiles (P2136_Biolog_Utilisation.csv)
    - Fields include: SAMPLING_DATE, MAX_DEPTH (cm), BIOLOG_CELL, SUBSTRATE, SUBSTRATE_TYPE, UTILISATION (1 = substrate used, 0 = not used).
  - Soil moisture data (P2136_Soil_Moisture.csv)
    - Fields include: SAMPLING_DATE, MAX_DEPTH (cm), PERCENTAGE_MOISTURE (mean of three replicate cores).

- Sampling site and design
  - Location: Sourhope field site, Scottish Borders, UK; grid reference for site sampling NT854196; broader Sourhope farm grid NT8545019630.
  - Site characteristics: temperate upland grassland with a shallow, organic-rich brown forest soil over glacial till.
  - Depths and cores: cores to ~20 cm; four 5-cm depth increments (0–5, 5–10, 10–15, 15–20 cm). Three replicate cores per sampling date.
  - Dates: 8, 10, 14 July 1999; 5 October 1999; 3 April 2000; 30 August 2000.
  - Procedures: 1 g soil used for dry weight; remainder stored at −70 °C prior to nucleic acid extraction and BIOLOG analyses. BIOLOG-GN plates prepared from 0.5% soil suspensions, incubated at 18 °C, scored for colour development (presence/absence).

- Data collection and measurement details
  - BIOLOG-GN assay: three replicate plate wells per sample prepared and scored for substrate utilisation (binary 1/0).
  - Soil moisture: moisture percent calculated as mean of three replicate cores, determined by oven drying at 105 °C for 24 hours.

- Data structure and accessibility
  - Two comma-separated value files are provided with clearly defined metadata for each column (date, depth, sample, substrate type, and utilisation).
  - The dataset records temporal (sampling date) and vertical (depth) variation in bacterial substrate utilisation and moisture content at a single upland grassland site, enabling integration with GIS datasets that cover soil properties, land use, and environmental layers.

- Usage notes and context
  - Related publications for context and methodological background:
    - Griffiths et al. (2003) on depth and sampling time effects on bacterial community structure.
    - Sourhope Field Data Handbook (2003).
    - Usher et al. (2006) on understanding soil biodiversity.
  - Cautions:
    - Data are subject to quality assurance but are not warranted for accuracy or fitness for a particular use by NERC; no liability for use.

- Practical GIS considerations
  - Useful for spatial-temporal analyses of soil bacterial functional capacity and moisture within upland grassland contexts.
  - Depth- and date-resolved measurements allow cross-coring and layering with other soil GIS layers (e.g., soil type, horizon properties, climate data), though explicit per-sample coordinates beyond the stated site reference are not provided in the files.