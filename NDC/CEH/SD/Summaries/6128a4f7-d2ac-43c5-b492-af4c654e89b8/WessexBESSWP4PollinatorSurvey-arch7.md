# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics.

## Overview
- Study area: Wessex region, southern England; surveys conducted in 2014–2015 in largely arable and intensive grassland with remnant calcareous grassland.
- Objective: relate pollinator abundance and diversity in winter-sown oilseed rape to local plant diversity (in-crop and field margins) and landscape characteristics.
- Project context: part of the NERC Wessex BESS WP4 program.

## Data and methods (GIS and field procedures)
- Pollinator data collection:
  - Methods: pan traps and transects.
  - Taxonomic focus: Bombus spp. and Apis mellifera recorded to species/caste when possible; pan traps captured additional visitors (hoverflies and other Hymenoptera/Diptera) identified to family or species where feasible.
- Local plant diversity:
  - Field margins and cropped areas surveyed with quadrats (five 1 m² quadrats in margins; one quadrat per crop sampling point).
  - Hedge presence recorded; edge structure quantified (edge length, hedge proportion, field margin proportion and width).
- Field layout:
  - Three 58 m transects per field, stratified random to include hedges and margins where possible.
  - Sampling aligned to conditions (transects surveyed 10:00–16:00, temperature >12°C, wind <6–8 m/s).
- Landscape characteristics (GIS workflow):
  - Data sources integrated in ArcGIS 10.1:
    - CEH Land Cover Map 2007
    - Natural England Priority Habitats Inventory (PHI)
    - Local National Vegetation Community surveys (NVC)
  - Grassland classification: semi-improved, agrienvironment/restoration, species-rich, intermediate, improved.
  - Buffers: calculated areas for grassland types, semi-natural habitats, and arable land within radii from 0.5 to 3 km at 0.5 km intervals.
  - Crop species recorded within 1 km buffers; other landscape features included to derive restoration, species-rich, and grassland metrics.
  - Field verification: grassland type classifications verified in the field within a 1 km buffer.
- Data structure and linkage:
  - Four main CSV files with linked identifiers:
    - NERCPollinatorSpeciesList.csv
    - NERCPanTrapData.csv
    - NERCPollTrans.csv
    - NERCPollLandscapeSurvey.csv
  - Consistent linking keys: FarmID, FieldID, TransectID, PointCode, SpeciesCode.
- Temporal scope:
  - Field surveys conducted across 2014 and 2015; 12 fields surveyed per year.

## Datasets and variables (key content)
- NERCPollinatorSpeciesList.csv:
  - Taxonomic level: species/genera/families; includes species codes, functional group classifications, and collMeth (method of collection).
  - Details for linking to pan traps and transects; notes on missing or partially identified taxa.
- NERCPanTrapData.csv:
  - Per-point pan trap data: PointCode, DateSet, growth stage context, percent plant cover, SppRichPlants, and counts by species across columns.
  - Note: several pan trap entries missing due to knocks over (specific PointCode entries listed as missing).
  - Transect linkage with TransectID and Year.
- NERCPollTrans.csv:
  - Transect-level counts by date and year; per-species/caste counts across days; linked to TransectID.
- NERCPollLandscapeSurvey.csv:
  - Landscape metrics per transect: IPSpeciesCount, various Grassland/ Habitat metrics (IG*, RES*, SppRich*, SN*, OSR*, TotAr*), habitat composition within 0.5–3 km buffers (Area and Distance metrics), boundary and hedge metrics (MarginLength, MarginWidthM, LengthHedgeM, HedgeHeightM, HedgeWidthM).
  - Extensive buffer-based variables (IGArea1, IGDist1, ResArea1, ResDist1, SppRichArea1, SppRichDist1, etc.) across 0.5–3 km radii.
  - Other covariates: MarginAreaFieldEdge, EstAmountIP, MarginLength, MarginWidthM, etc.

## Spatial analysis and GIS workflow
- GIS integration:
  - Landscape context derived by overlaying multiple spatial datasets (LCM2007, PHI, NVC) and field knowledge to classify grassland types and semi-natural habitats.
  - Validation: field verification within a 1 km buffer to ensure GIS-derived classifications align with on-the-ground conditions.
- Scale and radii:
  - Analyses conducted at multiple spatial scales using concentric buffers from 0.5 to 3 km around transect midpoints.
  - Crop-specific context within 1 km buffer used for crop species data.
- Data linkage:
  - Datasets joined via FarmID, FieldID, TransectID, PointCode, and SpeciesCode to enable integrated analyses of pollinator counts, plant diversity, and landscape context.

## Quality assurance and ethics
- Protocols:
  - Standardized field and lab data collection protocols; explicit datasheets for each collection type.
  - Data entry in MS Access with anomaly checks.
- Ethics:
  - Study approved by CLES Penryn Research Ethics Committee (application 2014/622).
- Data gaps:
  - Some pan trap data missing due to equipment mishaps; transparent note in metadata.

## Practical notes for GIS use
- Dataset is designed for integration with other Wessex BESS WP4 data for broader ecological analyses.
- Rich linkage across species, trap, transect, and landscape variables supports multi-scalar GIS analyses of pollinator-habitat relationships.
- Metadata provides key field identifiers and taxonomic details to support reproducibility and cross-dataset joins.

## Limitations and considerations
- Missing pan-trap entries require handling in analyses (imputation or exclusion decisions).
- Raster/vector dataset resolutions and compatibility across the three main landscape data sources may influence harmonization.
- Temporal gap: data limited to 2014–2015; extrapolation beyond this period should be done cautiously.