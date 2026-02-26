Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru

## Overview
- Dataset of taxonomic and abundance data for benthic macroinvertebrates collected from 10 rivers in glacial valleys (Cordillera Blanca, Ancash, Peru).
- Aimed at analyzing how aquatic biodiversity responds to glacial retreat across a gradient of glacier coverage.
- Data linked to the article: Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru.
- Sampling occurred in two seasons: October 2019 (dry season) and October 2020 (wet season).

## Data files and structure
- Two main abundance datasets:
  - Macro_CBPeru_Wet.csv (wet season)
  - Macro_CBPeru_Dry.csv (dry season)
- Structure details:
  - Sampling sites are in the first column; taxa are represented in the first row.
  - Each river site has 6 subsamples (except P01 in the dry season, which has 5 due to weather conditions); the second column records the subsample repetition (1–6).
  - The database contains the abundances of 41 identified taxa, with 38 taxa in the dry season and 39 in the wet season.
- Taxa information:
  - Taxa are listed with descriptions; some identifications are at the genus level (italicized names); others are identified to subfamily or higher taxonomic groups when necessary.
  - A comprehensive mapping of taxa names, families/subfamilies, and orders is provided (Table 2 in the dataset description).

## Sampling and laboratory methods
- Field sampling:
  - Water courses originate on western glacier flanks (Huandoy and Huascarán).
  - At each site: 15-meter reach, 6 random subsamples from riffles, pools, and bankside habitats.
  - Subsamples collected with a 250 μm mesh net (0.09 m2); approx. 1 minute per subsample.
  - Substrate preserved in 96% ethanol in the field; samples kept airtight.
- Laboratory processing:
  - Samples washed through a 250 μm sieve; macroinvertebrates picked and identified to the lowest possible taxonomic level.
  - Identification methods:
    - Genus-level for Trichoptera, Ephemeroptera, Plecoptera (Domínguez & Fernández 2009).
    - Several Chironomidae taxa identified to subfamily; morphotype approach based on Prat et al. (2011) used.
  - Counts include all life stages present (larvae, nymphs, pupae; adults included for Coleoptera).

## Site codes and geographic metadata
- ten sites coded P01–P10, representing 10 rivers across three glacial valleys (Parón, Huaytapallana, Llanganuco).
- Geographic variables per site include:
  - Coordinates (UTM 18S)
  - Valley/basin name
  - Basin area (km2)
  - Glacier area (km2) and Glacier Coverage Coefficient (GCC, %)
  - Distance from glacier (km)
  - Slope (%)
  - Altitude (m above sea level)
- GCC provides a gradient representing glacier influence at each site (ranging from near 0% to ~61.61%).

## Quality control and data provenance
- Field and laboratory quality controls:
  - The same person collected all substrate samples at a site.
  - Processing completed within 48 hours of collection.
  - Taxonomic identifications corroborated by a professional expert; counts verified by two professionals.
- Data provenance:
  - Data collection and curation responsibilities distributed among contributors by role (sample collection, laboratory analysis, supporting information, planning and management).
  - Version control: 1.0 (dataset description notes creation and authorship).

## Data details and taxa information
- 41 taxa listed across the two seasons; number of detected taxa per season is 39 (wet) and 38 (dry).
- Taxa are described with their family/subfamily and order, with a crosswalk to identification notes (Table 2 in the dataset description).
- Most chironomid taxa identified only to subfamily or morphotype due to identification limitations in Andean river systems.

## Considerations for data users (Data Leaders perspective)
- Data usefulness:
  - Enables analysis of biodiversity responses to glacial retreat across a clear GCC gradient.
  - Suitable for exploring richness, habitat associations, and seasonal shifts in macroinvertebrate communities.
- Data completeness and gaps:
  - Some taxa identification is limited (genus-level or subfamily-level identifications for Chironomidae), which may affect fine-resolution analyses.
  - Dry season sampling had one site with fewer subsamples (P01), affecting comparability for this site-season combination.
- Metadata and discoverability:
  - Detailed site-level geographic data and GCC values support spatial analyses and replication planning.
  - Clear documentation of sampling design, replication, and sequencing of data (wet vs. dry) facilitates reproducibility.
- Data governance and reuse:
  - Provenance and contributor roles are documented; methodology is described for reproducibility and potential data integration with other datasets.
  - References provided for taxonomic keys used in identifications (Domínguez & Fernández 2009; Prat et al. 2011).

## References included
- Domínguez, E., & Fernández, H. (2009). Macroinvertebrados bentónicos sudamericanos. Sistemática y biología.
- Prat, N., Acosta, R., Villamarín, C., & Rieradevall, M. (2011). Guía para el reconocimiento de larvas de Chironomidae (Diptera) de los ríos altoandinos de Ecuador y Perú.