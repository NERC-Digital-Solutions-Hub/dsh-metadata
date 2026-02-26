# Data on the locations of and temperatures (in deg C) recorded by dataloggers deployed in the soil during surveys at 24 oil palm smallholder farms in Perak, Malaysia

## Overview
- Large, multi-faceted data collection across 24 oil palm smallholder farms in Perak, Malaysia, conducted May 2022–July 2022 (and related environmental work December 2021–February 2022).
- Aims to compare effects of plantation management practices on soil temperature, biodiversity, vegetation structure, and soil/vegetation microhabitat.
- Includes four sampling locations per plantation (T1–T4) spaced ~20 m apart, totaling 96 datalogger points for soil temperature measurements; dataloggers buried at 5 cm depth and linked to plot-level metadata.
- Data curated by field teams and quality-checked by researchers at the University of Cambridge to ensure consistency and plausibility.

## Datasets and main data types
- Soil temperature (datalogger) data
  - 96 points across 24 farms; hourly temperature records for up to 26 hours after setting (TempHr1–TempHr26).
  - Each record tagged by PlantationCode and SamplePoint (T1–T4); unit in °C.
- Insect observations (biodiversity surveys)
  - Standard transect walks (100 m) recording butterflies, Nephila orb-weaving spiders, assassin bugs; 5 m × 5 m observational plots.
  - Variables include SpeciesID, weather, date, time seen; microhabitat; counts by behavior (Flying, Resting, Sunning, Interacting, Nectaring); plant species for nectaring.
  - Location-linked via PlantationCode and sampling point identifiers.
- Arthropod abundance from sticky traps
  - 96 traps across four sampling points per plantation; 24-hour collection with field photography.
  - Counts by taxonomic groups (e.g., Ants, Termites, various orders) plus TotalSpecimenNumber and OrdinalAbundance; Notes field for other observations.
- Predator-prey and bait-card data (mealworms)
  - Setup and collection times for sticky traps, dataloggers, and bait cards; number of mealworms remaining on bait cards (MealwormsRemainingPalm 1–4).
  - Spatial alignment with sampling points (palm locations) and plantation codes.
- Vegetation, microclimate, and soil conditions (47 plantations)
  - Environmental survey data across central transects using 3 m × 3 m grids around plot centers (vegetation cover categories, canopy density, leaf litter, herbivory, health of nearby palm, etc.).
  - Canopy openness measures (both field-based visual estimates and densiometer counts); air temperature/humidity at locations T1–T4; palm age/height/epiphyte cover/herbivory/health; interlinked with GPS-centred plantation data.
  - Soil metrics: leaf litter depth, soil moisture, soil pH, A-horizon depth, soil block sampling with VESS (visual evaluation of soil structure) and Sq scores for soil layers.
  - GPS coordinates and corner/centre references included (GPSCodeCorner1–12, GPSCodeCentre, GPSCodeT1–T4).
- Plantation characteristics and social/economic surveys (49 plantations; includes some sites in Indonesia for broader project)
  - Social data collected via interviews; variables cover plot size, palm counts, demographics, management practices, attitudes toward wildlife and nature, income, intercropping, and management motivations.
  - Plantation-type categorization reflecting Wild Asia’s partnership level (WAGS-BIO, WAGS, Independent); district-level identifiers; lat/long; plantation area; palm density; landowner status and related attributes.
  - Economic data include OP (oil palm) and non-OP crop yields, prices, and buyers; management motivation and costs for herbicides, fertilizers, intercropping, organic manures, and other controls.
  - Numerous variables capture farmer demographics, education, income, time/allocation to farming, and perceptions of soil and environment.
  
## Spatial and temporal dimensions
- Spatial coverage
  - Plantations dispersed across Perak with a centralized transect framework; GPS coordinates provided for plantation centers, sampling points (T1–T4), and plantation corners.
  - Data layers include environmental polygons (plot boundaries), canopy measurements, and neighboring habitat types along plantation sides.
- Temporal coverage
  - Soil temperature data collected during field campaigns in May–July 2022.
  - Biodiversity and predator-prey data collected concurrently with soil data or in adjacent field campaigns.
  - Vegetation, soil, and microclimate surveys conducted December 2021–February 2022.
  - Social/economic surveys conducted December 2021–July 2022, with some interviews by phone due to COVID considerations.

## Data structure and linkage
- Core linking key: PlantationCode (plot identifier) used across datasets to join temperature, biodiversity, vegetation, soil, and social/economic data.
- Spatial linkage: GPSCodeCentre, GPSCodeT1–T4, GPSCodeCorner1–12 connect plantation geometry to field measurements.
- Temporal attributes included: Date, StartTime/EndTime for setup and collection phases, and hourly timestamps for temperature data.
- Data quality and formatting
  - Field data uploaded and quality-checked by Cambridge team to ensure consistency with timing and plausibility.
  - Insect identifications aided by local guides and field photography; sticky-trap images cross-validated for order-level identifications.

## GIS-oriented considerations and uses
- Map-ready datasets for visualizing spatial gradients in soil temperature, canopy openness, vegetation cover, and soil health across the plantation network.
- Enables comparisons by Wild Asia partnership level (WAGS-BIO, WAGS, Independent) to assess management impact on microclimate and biodiversity.
- Facilitates integration with habitat data (side habitat categories) and plantation corner coordinates for precise polygon and transect mapping.
- Supports cross-dataset analyses, such as correlating soil temperature with canopy density, leaf litter depth, and soil moisture/pH; linking ecological observations (butterflies, spiders, ants, termites) to microhabitat conditions.
- Potential for temporal analyses of temperature and biodiversity changes across campaigns, and spatial analyses of predation rates via bait-card data.
- Suitable for GIS workflows that join by PlantationCode, then export to standard formats (CSV, shapefiles, GeoJSON) and project into a common coordinate system (WGS84, as lat/long coordinates are provided).

## Data quality, limitations, and caveats
- Social/economic data are self-reported and may contain inaccuracies; acknowledged as a caveat in interpretation.
- Some fields are NA due to non-applicability, missing responses, or field decisions; dataset preserves schema for cross-site comparability.
- The broader project includes sites beyond Perak (e.g., Riau, Indonesia), which may be relevant for cross-site analyses but requires careful geographic scoping.
- Temporal coverage reflects field conditions and collection schedules; mismatches in sampling intensity across datasets should be accounted for in analyses.

## Practical notes for users
- Use PlantationCode as the primary key to integrate soil temperature, biodiversity, vegetation, soil, and social data.
- Leverage GPS codes to reconstruct plantation geometry and transect placements; combine with SideLength and SideHabitat fields to model edge effects.
- Be mindful of NA values when performing gap- filling or imputation; document uncertainties associated with self-reported social data.
- When creating map layers, separate datasets by theme (soil microclimate, biodiversity observations, vegetation/soil health, plantation management) and then join them for composite spatial analyses.

## Intended audience and impact
- Designed for GIS specialists and data analysts seeking map-based data products to explore spatial patterns and relationships among plantation management, microhabitat conditions, and biodiversity within oil palm landscapes.
- Supports policy-relevant visualization and decision-support for sustainable plantation management, RSPO/MSPO assessment, and biodiversity monitoring at landscape scales.