# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- Study of natural enemies of crop pests in winter-sown oilseed rape (Brassica napus L.) in relation to local plant diversity and landscape characteristics.
- Field work conducted in 2014 and 2015 across the Wessex region, southern England.
- Data designed to be used alongside other Wessex BESS WP4 datasets to examine ecological interactions and pest regulation services.

## Data collection and methods
- Field sampling
  - Twelve fields surveyed per year.
  - In each field: three 58-meter transects perpendicular to the field edge, with transects chosen to include hedges and margins where possible.
  - Local margin and in-crop plant diversity measured using five 1 m^2 quadrats per transect near the start.
  - Hedge presence recorded; field edge margin structure and width assessed.
- Natural enemies sampling
  - Suction sampling (approx. 1 m^2 area for 7 seconds per sampling point) to capture canopy parasitoids (Hymenoptera: Parasitica).
  - Pitfall traps (6 cm diameter, ethylene glycol solution) for ground-dwelling natural enemies; two 4-day periods per year.
  - Water traps used to detect pest larvae dropping from the canopy (subset of fields).
  - Sampling points: three points per transect (8 m, 33 m, 58 m into the crop).
- Pest larvae monitoring
  - Water traps used to count key pest larvae: Meligethes spp., Ceutorhynchus spp., and Dasineura spp.; sub-samples analyzed.
- Temporal coverage
  - Field sampling conducted in 25 June–18 July 2013 and 30 May–18 June 2014 for suction; 10–13 June and 1–4 July 2013 and 2–9 June and 30 June–3 July 2014 for pitfall traps.
- Ethics and QA
  - Protocols followed for field and lab data collection; training provided; ethics approval obtained (CLES Penryn Research Ethics Committee, 2014/622).
  - Data entered in MS Access with QA checks; standardized datasheets used.

## Datasets and data structure
- Core data files
  - NERCPestNatEnSpeciesList.csv: taxonomic details and linkage codes for natural enemies and pests; includes method, gender (where applicable), and SpeciesCode to join with sampling data.
  - NERCPitfall.csv: pitfall trap counts by sample; includes SampleCode, SurveyDate, PointCode, SampleNo, and species counts (Columns 5–312).
  - NERCSuctionSample.csv: suction sample counts by point; includes PointCode and species counts (Columns 2–33).
  - NERCWaterTrap.csv: pest larva counts in water traps; includes SampleCode-linked pest counts (Meligethes, Dasineura, Ceutorhynchus) and parasitized/ecto-parasite indicators.
  - NERCNatEnLandscapeSurvey.csv: landscape context data; includes TransectID, FarmID, FieldID, Year, and a wide range of habitat metrics (in-crop and margin flora richness, percent cover, field edge metrics, hedge metrics, and extensive landscape buffers).
- Dataset scope
  - Local plant diversity: margin plant richness, in-crop plant richness, percent cover of non-crop plants.
  - Field edge structure: length of field edge, proportion hedge, margin width and margin area.
  - Landscape context (within 0.5–3 km radii, 0.5 km increments): grassland presence and type (intensive, species-rich, restored, semi-natural habitat), arable land, and various habitat quality/restoration indicators.
  - Habitat metrics extended to hedgerows and field margins: hedge height, hedge width, hedge length.
  - Landscape scoring includes grassland restoration and restoration density, species-rich grassland presence, and proximity metrics.

## Landscape characteristics and local habitat metrics
- Spatial data sources and integration
  - GIS-based combination of CEH Land Cover Map 2007, Natural England Priority Habitats Inventory, and local National Vegetation Community surveys.
  - Field-level verification within a 1 km buffer.
- Grassland classification
  - Semi-improved, species-rich (NVC communities CG2, CG3, CG6, MG5), intermediate (MG1, MG4, MG6), improved (MG7), plus a recovering/restoration category.
- Habitat buffers and radii
  - Calculations performed in buffers from 0.5 to 3 km (in 0.5 km steps) around sampling points to summarize habitat availability and composition.
- Local habitat variables
  - Details include margins, hedges, hedge height/width, margin width, margin edge area, and field-edge margin length.

## Geographic and temporal scope
- Region: Wessex region, southern England (NW corner: 51.4155 N, -2.2893 W; SE corner: 51.0871 N, -1.5038 W).
- Field scale: 12 fields per year; transects within each field verified against local habitat features.
- Year coverage: 2013 (sampling periods) and 2014 (sampling periods) for certain methods; field surveys carried out in 2014 and 2015 for the broader study period.

## Data quality, validation, and accessibility
- Data QA
  - Standardized field and lab protocols; trained personnel; data entry with anomaly checks.
- Data linkage
  - Species and sample linkage achieved via SpeciesCode across NERCPestNatEnSpeciesList.csv, NERCPitfall.csv, and NERCSuctionSample.csv.
- Data access
  - Datasets are designed to be used together with other Wessex BESS WP4 datasets, enabling cross-study analyses of natural enemies, plant diversity, and landscape context.

## Potential uses and relevance to environmental monitoring
- Supports analyses of how local plant diversity and landscape structure influence natural enemy communities and pest control services in oilseed rape.
- Enables standardized assessment of ecological health and pest regulation potential across farms and landscapes within the Wessex region.
- Data structure and quality controls align with monitoring aims to verify environmental health and policy performance over time, and to facilitate data sharing and broader reuse.