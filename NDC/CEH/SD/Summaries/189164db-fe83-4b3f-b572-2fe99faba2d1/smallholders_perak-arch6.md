# Data on the locations of and temperatures (in deg C) recorded by dataloggers deployed in the soil during surveys at 24 oil palm smallholder farms in Perak, Malaysia, over approximately a 24-hour period.

## Overview
- A multi-component data collection from 24 oil palm smallholder farms in Perak, Malaysia, conducted May–July 2022.
- Sites include three collaboration levels with Wild Asia: WAGS-BIO, WAGS, and Independent farmers.
- Aimed at assessing effects of plantation management practices on soil temperature, biodiversity, microclimate, vegetation, soil conditions, and socio-economic factors.
- Data were collected in four transect locations per smallholding (T1–T4) spaced 20 m apart (totaling 96 sampling points per dataset) and underwent quality checks at the University of Cambridge.
- Outputs designed for cross-dataset analyses and product development (dashboards, reports, self-serve tools).

## Datasets Included

- Temperature and logger location data (soil)
  - 24 oil palm smallholder farms; 96 locations total (4 points per farm).
  - Dataloggers: single Thermochron iButton buried at 5 cm depth; data collected in field campaigns.
  - Variables (high-level): PlantationCode, SamplePoint (T1–T4), TempHr1–TempHr24 (and TempHr25–TempHr26 in extended data); timing and data quality flags; NA for early collection instances.
  - Data flow: field collection → downloaded/checked by Cambridge team → standardized format.

- Insect and arachnid observational data (butterflies, Nephila orb-weaving spiders, assassin bugs)
  - Standard 100 m transects; 5 m × 5 m survey plots.
  - Observations recorded with species IDs, weather notes, air temperature, and microhabitat context; activity states (flying, resting, sunning, interacting, nectaring); plant species for nectaring; specimen photos for verification.
  - Variables include SpeciesID, WeatherCond, AirTemp, Date, TimeSeenCaught, Microhabitat, and counts by behavior categories.
  - Data handling: entered by field teams; quality-checked by Cambridge; identification at order level for many taxa.

- Set-up and collection timing for sticky traps, dataloggers, and bait cards
  - 96 locations across four sample points; 24-hour exposure periods.
  - Sticky traps: 30 cm × 30 cm, glue-side up, 40 cm above ground.
  - Bait cards: mealworms attached to palm trunks to assess predation (removal after 24 h).
  - Variables cover set-up/collection times by trap point (StickyTrapSetupTimeT1–T4, DataLoggerSetupTimeT1–T4, BaitSetupTimePalm1–Palm4, etc.) plus weather and notes.
  - Additional fields track data logger IDs, palm locations, and collection timing.

- Arthropod abundance on sticky traps
  - Abundance data by major orders (e.g., Ants, Termites, Wasps; and non-Ant Hymenoptera) with counts per trap.
  - Includes TotalSpecimenNumber, OrdinalAbundance, and taxon-specific counts; notes on non-ant Hymenoptera and other groups.
  - Data collection supported by image-based identification to order level; NA entries exist for missing sites.

- Vegetation, microclimate, and soil environmental data (47 plantations)
  - Detailed environmental mapping across plantation plots and neighboring habitats; GPS coordinates for plot corners and center; transect-based environmental sampling at four central points per plantation (T1–T4).
  - Vegetation metrics: cover (%) by crop, bare ground, ferns, other vegetation, leaf litter, palm fronds; vegetation height; canopy openness (both dot-densiometer and visual estimates); leaf litter depth; epiphyte cover.
  - Microclimate: air temperature and humidity at multiple points; palm age/heights; palm health/herbivory; health scores; photos and notes.
  - Soil metrics: leaf litter, soil moisture (1–10 scale), soil pH, soil depth to A horizon, soil samples (wet/dry weights), soil structure visuals (VESS scores across up to 4 layers per point), soil depth and layer-specific measurements.
  - GPS and land-use metadata: GPSCodeCentre, GPSCodeT1–T4; SideLength A–L; SideHabitat A–L; CropTypeName and CropTypePc pairs; horizon depths; soil series and profile descriptions.
  - Extensive derived fields include canopy openness (visual and densiometer), soil horizon depth, soil moisture/pH, and VESS-related scores.

- Plantation characteristics and management practices (social-ecological survey; 49 plantations, broader project scope)
  - Collaboration levels with Wild Asia; plantation type and old plot codes; district identifiers; coordinates (lat/long); plantation area; palm density; farm ownership and management structure; farmer demographics (age, gender, marital status, household size, nationality/ethnicity with anonymization); years on land and in management; land-use history and recent conversions; management motivation and priorities.
  - Economic and employment data: total income, agricultural income, OP (oil palm) income, monthly earnings, and prices/yields (monthly and per hectare, where available).
  - Management and production practices: herbicide/fertilizer use (types, frequency, cost, volume, per-hectare rates), other vegetation control methods, cropping intercropping, manure use, frond use, livestock presence, pest/disease motivation, supplier influence, neighbor influence, and consistency of practices.
  - Attitudes and values: definitions of nature, ranked importance of nature-related values (economic, food, wildlife, beauty, culture, health, etc.). Time commitment to farming (daily/weekly) and relative emphasis on oil palm.
  - Data collection methods: mixed (telephone and face-to-face), ethical approval obtained, anonymized responses; NA used where data were not reliably answered or refused.
  - Data quality and caveats: self-reported information with potential errors; some questions not answered or answered in unforeseen ways; responses linked to other sites in the wider project via standardized formats.

## Study Design and Methods
- Field campaigns conducted by Wild Asia researchers, with Cambridge-based quality assurance and standardization efforts to ensure consistent data formats across datasets.
- Spatial design includes four sampling points per plot (T1–T4) with 20 m spacing; transects and point measurements implemented for soil, vegetation, microclimate, and biodiversity components.
- Taxonomic resolution generally limited to order-level for arthropods; species-level IDs supplemented by photographs and local guides where possible.
- Temporal scope spans December 2021–February 2022 for environmental mapping and May 2022–July 2022 for biodiversity and microclimate measurements (plus ongoing data collection in some components).

## Data Quality, Provenance, and Access
- Data downloaded and cleaned by field teams; standardized to ensure compatibility across datasets; cross-checked against field timing and device settings.
- Quality checks performed by University of Cambridge; explicit notes on realistic values and timing alignment; NA used for missing or non-applicable fields.
- Ethical considerations include informed consent, anonymization, and local-language survey tools; institutional ethics approval documented.
- Links and references: some datasets reference GPS coordinates and related data files (e.g., GPSDataPerak.csv) to enable geospatial linking.

## Integration and Use Cases for Data Support
- Potential to build cross-dataset dashboards and self-serve analytics comparing:
  - Soil temperature patterns across management groups (WAGS-BIO, WAGS, Independent) and plot designs.
  - Relationships between vegetation/ground cover, canopy openness, and arthropod/biodiversity metrics.
  - Predation and predator-prey dynamics from sticky traps and bait-card data.
  - Social-ecological drivers (management motivation, costs, yields, and farmer attitudes) with biophysical context.
- Data products could include: multi-dataset dashboards, GIS-enabled analyses, and reproducible reports that align management practices with biodiversity and soil health indicators.

## Caveats and Limitations
- Patchy data and missing values (NA) in several fields; some fields rely on self-reported information with potential inaccuracies.
- Taxonomic resolution limited in some datasets; field identifications may require expert verification for higher-level analyses.
- Temporal alignment across datasets may require careful synchronization given staggered collection windows across 2021–2022.

## What to Do Next (Data Support Perspective)
- Identify cross-dataset linkages via PlantationCode, GPS coordinates, SamplePoint, and dates to construct integrated analyses.
- Develop data products (dashboards/reports) enabling end users to explore soil temperature, microclimate, vegetation structure, arthropod abundance, and socio-economic factors by Wild Asia collaboration level.
- Create data dictionaries and a data integration plan to facilitate re-use by local stakeholders and researchers.