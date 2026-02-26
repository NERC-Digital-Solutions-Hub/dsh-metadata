# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics

- Objective: quantify pollinator communities (bumblebees, honey bees, solitary bees, hoverflies) in winter-sown oilseed rape and relate them to local plant diversity in crop margins and landscape context within the Wessex region, UK.

- Study scope and timing: field surveys conducted in 2014 and 2015 across 12 fields per year in southern England; area characterized by arable and intensive grasslands with remnant calcareous grassland.

- Data sources and integration: dataset designed to be used with other Wessex BESS WP4 datasets; field data linked to landscape data via GIS-derived metrics.

- Field data collection and measurements:
  - Pollinator sampling methods:
    - Pan traps (15 cm diameter, UV yellow) for solitary bees, hoverflies, and other visitors.
    - Transects walked to record Bombus spp. and Apis mellifera visitation within 2 m of flowers.
  - Local plant diversity:
    - Quadrats in field margins and cropped areas; plant species identified (Stace 1997) and percent cover recorded.
  - Habitat features recorded at field edge:
    - Hedge presence and proportion of hedge, field margin, and margin width.
  - Sampling design:
    - Three 58 m transects per field per sampling event; edges with/without hedges included; transects positioned using stratified random sampling.

- Landscape characteristics and scale:
  - GIS-based assessment within 0.5 to 3 km buffers around sampling points.
  - Land cover and habitat datasets combined to derive: grassland types (intensive, restored, species-rich), semi-natural habitat, arable land, mass flowering crops, and presence of grassland restoration projects.
  - Within-buffer metrics include area and proximity of grassland types, semi-natural habitats, oilseed rape, arable crops, and habitat diversity.

- Variables and data structure:
  - Local-scale: edge length, hedge proportion, margin length/width, margin area, growth stage of oilseed rape near pan traps.
  - Habitat and plant metrics: margin insect-pollinated plant cover, total plant species richness in margins, crop richness, and margins’ area metrics.
  - Landscape-scale: counts and areas of grassland types, semi-natural habitat, oilseed rape, arable land; various buffer-based measures (0.5–3 km) for each habitat category.
  - Pollinator data: counts by species/caste per transect and per pan trap; species codes linked across files (NERSPollinatorSpeciesList, NERCPanTrapData, NERCPollTrans).

- Data quality assurance and ethics:
  - Standardized field and lab protocols; data entered in MS Access with anomaly checks.
  - Training provided by project staff; ethics approval obtained from University of Exeter CLES Penryn Research Ethics Committee (2014/622).

- Datasets and metadata:
  - Files: NERCPollinatorSpeciesList.csv; NERCPanTrapData.csv; NERCPollTrans.csv; NERCPollLandscapeSurvey.
  - Metadata conventions: linking keys FarmID, FieldID, TransectID, PointCode, and SpeciesCode enable cross-dataset integration.
  - Data quality notes: some pan traps missing due to damage; incomplete taxonomic resolution for certain groups (e.g., Papilionoidea to family/superfamily) and limited gender data outside Apoidea; several species identifications recorded only to higher taxonomic levels.

- Limitations and considerations for policy use:
  - Data gaps and incomplete metadata can hinder rapid verification; some datasets require transformation for compatibility with other systems.
  - Public sharing of underlying datasets can be a barrier; documentation and data governance are essential to enable reuse and transparency.
  - Taxonomic resolution and missing gender/caste data may affect fine-scale interpretation of pollinator function and pollination delivery.

- Key references and classification schemes:
  - Growth stage coding for crops (Lancashire et al. 1991); LCM2007 land cover map (Morton et al. 2011); British plant communities (Rodwell 1992); flora references (Stace 1997); Salisbury Plain ecological surveys (Walker & Pywell 2000).