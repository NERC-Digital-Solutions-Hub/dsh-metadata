# Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru.

## Overview
- Dataset of taxonomic and abundance data for benthic macroinvertebrates from 10 rivers in glacial valleys (Parón, Huaytapallana, Llanganuco) in the Cordillera Blanca, Ancash, Peru.
- Aimed to analyze how aquatic biodiversity responds to glacial retreat across a gradient of glacier cover.
- Data originate from surveys conducted in 2019 and 2020 and are linked to the associated article.

## Data collection and processing
- Sampling area origins: waters originate on western flanks of Huandoy and Huascarán glaciers.
- Sampling period: Oct 14–30, 2019 and Oct 7–16, 2020.
- Site sampling design: at each site, defined a 15-meter section and collected 6 composite samples (5 subsamples per composite) across riffles, pools, and bankside habitats.
- Subsampling: each composite sample derived from 5 subsamples obtained with a 250 μm mesh net.
- Preservation and processing: field-preserved in 96% ethanol; in lab, samples washed through a 250 μm sieve; macroinvertebrates identified to the lowest possible taxonomic level (genus for Trichoptera, Ephemeroptera, Plecoptera; many Chironomidae to subfamily level).
- Taxonomic scope: 41 total taxa identified across seasons; 38 taxa in dry season and 39 taxa in wet season.
- Quality assurance: identical collector at all sites; processing within 48 hours; taxonomic IDs corroborated by a subject-matter expert; entire samples counted and records cross-checked by two professionals.

## Data structure and contents
- Data files: Macro_CBPeru_Wet.csv (wet season) and Macro_CBPeru_Dry.csv (dry season).
- Organization: sites in the first column; taxa in the first row; second column indicates replication number (RN, 1–6; P01 had 5 replicates in dry season due to conditions).
- Taxa coverage: 41 taxa total; wet season includes 39 taxa; dry season includes 38 taxa; includes a variety of Ephemeroptera, Plecoptera, Trichoptera, Diptera, Coleoptera, and other groups.
- Taxon labeling: rows/columns labeled with descriptive names and higher-level taxonomy where applicable (e.g., Sp1 = Andesiops sp.; Sp13 = Orthocladiinae sp1., etc.).

## Site and environmental context
- Each site coded P01–P10 with geography and glacier-related variables summarized in a table (Table 1):
  - Geographic coordinates (UTM 18S)
  - Valley name (Parón, Huaytapallana, Llanganuco)
  - Basin area (km²)
  - Glacier area (km²)
  - Glacier coverage (GCC, %)
  - Distance from glacier (km)
  - Slope (%)
  - Altitude (m above sea level)
- Key gradient focus: GCC values range from near 0% (no glacier coverage) to about 61.6% in the most glacier-dominated sites, enabling examination of biodiversity responses along glacial influence.

## Taxonomy and units
- Abundance data: counts of macroinvertebrates per site-season, across 41 identified taxa (genus-level identifications where possible).
- Notable taxonomic groups: Chironomidae and Chironomidae/Orthocladiinae are extensively represented; various Ephemeroptera, Plecoptera, Trichoptera families and genera included.
- Units: individual counts per taxon per site per sub-sample; data compiled per season in separate files.

## Data quality and provenance
- Provenance: data collected by Palacios, Medina, Loarte (sampling); Palacios, Gamboa, Brown (lab analysis); Castañeda, Polo, Tapia (support); Medina, Loarte, Brown, Pellicciotti (planning/management).
- Version: 1.0; created as part of the Macro_CBPeru dataset aligned with the cited article.
- Verification: multiple contributors corroborated identifications; data subjected to rigorous verification to ensure accuracy and consistency.

## Uses, applications, and interoperability
- Primary use: monitor and compare aquatic biodiversity across glacial influence gradients; support assessments of environmental health and policy performance over time.
- Potential integration: designed to be combined with other environmental datasets (e.g., physical habitat, water chemistry) for broader analyses of ecosystem response to glacier retreat.
- Accessibility: data structured for straightforward loading into analysis workflows and portals supporting environmental monitoring datasets.

## References
- Domínguez, E., & Fernández, H. (2009). Macroinvertebrados bentónicos sudamericanos. Sistemática y biología.
- Prat, N., Acosta, R., Villamarín, C., & Rieradevall, M. (2011). Guía para el reconocimiento de larvas de Chironomidae (Diptera) en ríos altoandinos de Ecuador y Perú.