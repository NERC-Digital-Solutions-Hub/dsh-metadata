# Botanical material

## Overview
- Seeds from 14 Cerrado-native species were studied to analyze ultrastructure of the seed integument via scanning electron microscopy (SEM) and to gain insight into relationships between seed/fruit structure and fire adaptation.
- Seeds were collected from multiple populations across several protected areas in Brazil, with at least ten individuals per species from different populations.

## Data Collection and Sites
- Collection locations include:
  - Parque Nacional da Serra do Cipó, Minas Gerais (PNSC)
  - Reserva Natural Serra do Tombador, Goiás (RNST)
  - Parque Estadual do Jalapão, Tocantins (PEJ)
  - Estação Ecológica de Itirapina, São Paulo (EEI)
  - Estação Ecológica de Assis, São Paulo (EEA)
- Coordinates are provided for sites (e.g., 19° 17' S, 43° 33' W; 13° 35'-38' S, 47° 45'-51' W; etc.).
- Species and families include multiple Melastomataceae taxa (e.g., Acisanthera alsinaefolia, Cambessedesia hilariana, Microlicia sp., Pleroma cardinale, Pleroma frigidula, Pleroma stenocarpum, Stenodon campestre, Tibouchina melastomoides) and Xyridaceae or Velloziaceae representatives (Xyris hilariana, Xyris jupicai, Xyris paradisiaca, Vellozia seubertiana, Vellozia squamata, Vellozia variabilis, etc.).
- For each species, seeds were collected from different populations; representative sampling is indicated in Table 1.

## Imaging Method (SEM)
- Sample preparation aimed at ultrastructural analysis:
  - Fixation in Karnovsky solution
  - Dehydration through an alcohol series
  - Critical point drying using CO2
  - Mounting on aluminum supports with conductive tape
  - Metalization with gold (30–40 nm)
  - Examination with a Carl Zeiss EVO LS15 SEM
- For SEM, one representative seed per species was imaged (as noted in Table 1).

## Data and Documentation
- Data elements captured include: species name, family, collection date, and collection site codes (EEA, EEI, RNST, PNSC, PEJ).
- Seed images include scale information embedded within image files.
- The study references established methodologies:
  - Karnovsky (1965) for fixative preparation
  - Perez-Harguindeguy et al. (2013) for standardized trait measurements
  - Zirondi et al. (2019) on fire-related germination factors

## Quality and Standards
- Data files were provided as created with no additional quality checks described.
- Image scales are included within the image files, but broader data QC practices are not specified.

## GIS Relevance and Potential Uses
- Geospatial value:
  - Precise collection sites provide geolocational context to associate seed traits with habitat/landscape features.
  - Ability to map species distributions across the Cerrado, linking morphological/structural traits to spatial environments and fire regimes.
- Potential GIS applications:
  - Create a geodatabase of seed collection sites with metadata (species, family, date, site code).
  - Overlay collection sites with environmental layers (soil, fire history, vegetation type) to explore spatial patterns of fire-adapted seed traits.
  - Visualize sampling density and coverage across protected areas to identify data gaps.

## Limitations and Considerations for GIS
- Location data are given at site level (codes and coordinates are provided for sites), but exact per-seed coordinates are not specified.
- QC is limited to embedded scale data in images; no broader dataset-wide quality control is described.
- Some data standardization details are not explicit beyond references to standard methods.

## Next Steps for GIS Specialists
- Convert site-level metadata into a GIS-ready dataset (CSV/GeoJSON/SQL) with fields: species, family, collection_date, site_code, latitude, longitude, site_name.
- Link SEM image metadata to corresponding GIS records (e.g., by seed_id) to enable multimedia-rich records.
- Integrate with environmental layers and fire history datasets to support spatial analyses of fire-adaptation traits across the Cerrado.
- Assess and document data quality, and consider applying standardized trait documentation to facilitate broader data sharing.