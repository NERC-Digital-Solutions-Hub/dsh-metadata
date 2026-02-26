# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- A dataset examining how natural enemies of pests in winter-sown oilseed rape relate to local plant diversity and landscape structure in the Wessex region, southern England.
- Collected during 2013 and 2014 as part of the Wessex BESS project (NERC-funded).
- Intended for integration with other Wessex BESS WP4 datasets to support GIS-based analyses and mapping.

## Data and collection methods
- Natural enemies collected with:
  - Suction sampling (canopy-dwelling parasitoids; identified to species for Hymenoptera, key groups for Coleoptera and spiders).
  - Pitfall traps (ground-dwelling predators; identified to species for major beetle and spider groups).
- Pest larvae monitored via water traps (sub-sample of fields).
- Field margins and cropped areas surveyed for local plant diversity using quadrats; hedges recorded.
- Field sampling across 12 fields per year, with transects (three 58 m transects per field) and sampling points at 8 m, 33 m, and 58 m into the crop.

## GIS data and landscape context
- Landscape characteristics derived by integrating multiple spatial datasets within a GIS (ArcGIS, v10.1):
  - CEH Land Cover Map 2007 (LCM2007)
  - Natural England Priority Habitats Inventory (PHI)
  - Local National Vegetation Community surveys (NVC)
- Grassland types classified using field data and expert knowledge, distinguishing species-rich, restoring, improved grasslands, semi-natural habitats, and arable land.
- Landscape metrics calculated in buffers from 0.5 to 3 km around collection points, at 0.5 km intervals:
  - Areas and proportions of grassland types and semi-natural habitats
  - Distances and areas related to restored, species-rich, and other grassland patches
  - Density and arrangement of surrounding arable land

## Local habitat and plant diversity metrics
- Field-edge habitat characteristics along transects:
  - Length of field edge, hedge proportion, field margin proportion and width
- Margin plant diversity assessed with five 1 m² quadrats within 20 m of transect start
- In-crop plant diversity assessed with quadrats 8 m, 33 m, and 58 m into the crop
- Species identification following Stace (1997) with percent cover recorded

## Natural enemies and pest data structure
- Data collected per transect and sampling point:
  - Suction samples yield identified Hymenoptera parasitoids and other key predators
  - Pitfall traps yield ground-dwelling taxa (Carabidae, Staphylinidae, Araneae groups)
  - Water traps quantify pest larvae counts (Meligethes, Ceutorhynchus, Dasineura) and parasitoid/ectoparasite associations
- Taxonomic and sample information standardized with linked files:
  - NERCPestNatEnSpeciesList.csv (species, taxonomic codes, gender when applicable for Hymenoptera)
  - NERCPitfall.csv (pitfall sample data and species counts)
  - NERCSuctionSample.csv (suction sample data and species counts)
  - NERCWaterTrap.csv (water trap pest counts and parasitism indicators)
  - NERCNatEnLandscapeSurvey.csv (landscape and habitat summary per field/point)
- Linking key: SpeciesCode (from NERCPestNatEnSpeciesList.csv) to connect species data across sampling methods
- Target pest larvae and natural enemy taxa have specific coded columns (e.g., Meligethes, Dasineura, Ceutorhynchus, parasitized counts)

## Data quality, governance, and ethics
- Field and lab protocols standardized; data entry in MS Access with QA checks.
- Training provided; ethics approval granted by CLES Penryn Research Ethics Committee (2014/622).
- Acknowledges missing data and field limitations (e.g., Field 3.1 transect reduction due to crop failure; several pitfall data losses).

## Usability and integration for GIS specialists
- Enables map-based analyses of how natural enemy communities and pest pressure relate to:
  - Habitat amount and configuration (grassland, semi-natural habitats)
  - Field-edge features (hedges, margins)
  - Buffer-scale landscape context (0.5–3 km)
- Data joinable via:
  - SpeciesCode to cross-link abundance data across Suction, Pitfall, and Water Trap datasets
  - Point/field identifiers to landscape and habitat metrics
- Suitable for creating spatial visualizations of:
  - Spatial distribution of key natural enemies by field/ transect
  - Relationships between pest larvae counts and landscape diversity
  - Habitat suitability and refuge area maps for biological control agents
- Can be combined with other WP4 datasets for broader ecological and policy-relevant insights

## Field, location, and temporal scope
- Field surveys conducted in 2014 and 2015 across the Wessex region (coordinates provided for study area boundaries).
- Location context: arable-dominated landscape with calcareous grassland remnants and diverse habitat patches.

## File archive (overview)
- NERCPestNatEnSpeciesList.csv
- NERCPitfall.csv
- NERCSuctionSample.csv
- NERCWaterTrap.csv
- NERCNatEnLandscapeSurvey.csv

## Potential map products and applications
- Spatial distribution maps of natural enemy groups by field and transect
- Landscape-scale predictors of natural enemy presence and pest pressure
- Buffer-based habitat and species richness maps (0.5–3 km) for agricultural planning
- Data-driven guidance for hedgerow and margin management to support biological control
- Integrated GIS-ready dataset for policy briefings and stakeholder communications in oilseed rape pest management

## Context and references
- Scientific background and taxonomic references supporting identification and classification of key parasitoids, beetles, and spiders (Ferguson et al. 2010; Joy 1932; Lott 2009/2011; Luff 2007; Morton et al. 2011; Rodwell 1992; Stace 1997; Toynton & Ash 2002; Walker & Pywell 2000).