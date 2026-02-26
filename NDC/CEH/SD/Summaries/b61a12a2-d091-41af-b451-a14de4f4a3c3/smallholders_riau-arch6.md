# Riau Biodiversity Data Collection (DataLoggers_Riau.csv; Inflorescences_Riau.csv; Pitfalls_Riau.csv; Transects_Riau.csv; Traps_Riau.csv; StickyTraps_Riau.csv; Environmental_Riau.csv; Social_Riau.csv)

- Overview
  - A collection of biodiversity and environmental datasets from biodiversity surveys in Riau, Sumatra, Indonesia, focusing on oil palm plantations and associated ecosystems.
  - Covers datalogger temperatures, inflorescence observations with pollinator data, pitfall and sticky trap arthropod abundances, transect-based insect and spider observations, trap setup/collection logistics, environmental vegetation/soil measurements, and social survey data from plantation managers.

- Key datasets at a glance
  - DataLoggers_Riau.csv
    - Location data for data loggers within plots (PlantationCode, Plot/SamplePoint) and hourly air temperature readings (TempHr1–TempHr25).
    - Includes data-logging site details and links to GPS coordinates (via GPSCode and GPSDataRiau.csv).
  - Inflorescences_Riau.csv
    - Inflorescence-level observations with two-day pollinator records (Pollinator counts by Day 1 and Day 2), weather, and dates/times.
    - Additional plant/inflorescence descriptors: Flowering status, PalmHeight, ground cover and canopy openness metrics, and related environmental context.
    - Includes detailed pollinator counts by taxa (e.g., AfricanOilPalmWeevilDay1/Day2, YellowCrazyAntDay1/Day2, WeaverAntDay1/Day2, etc.) and behavioral observations (Nectaring, Resting, Flying, Interacting).
    - Spatial linkage via GPSCode to GPSDataRiau.csv; heavily annotated with canopy, ground cover, and vegetation context.
  - Pitfalls_Riau.csv
    - Abundance data for arthropods captured in pitfall traps, with counts by major groups (e.g., Ants, Termites, Coleoptera, Diptera, etc.) across plots and sampling points.
    - Most taxa sorted to Order level; includes trap setup/collection timing and notes.
  - Transects_Riau.csv
    - Observational data for butterflies, orb-weaving spiders, and assassin bugs, including activity states (Flying, Resting, Sunning, Interacting, Nectaring) and microhabitat context.
    - Weather and air temperature recorded during surveys; species identifications (SpeciesID) and optional flowering plant associations.
  - Traps_Riau.csv
    - Set-up and collection timing for pitfall traps, sticky traps, dataloggers, and bait cards; includes GPS/plot linkage (PlantationCode) and per-sampling-point timings.
    - Detailed time stamps for setup/collection and mealworms remaining on bait cards per palm (Palm1–Palm4); includes numerous notes.
  - StickyTraps_Riau.csv
    - Abundance data for arthropods captured on sticky traps, with counts by taxon (Ants, Termites, Wasp, NonAntHymenoptera, Coleoptera, etc.) and total/ordinal abundance per trap.
    - Includes setup/collection dates and times, with notes.
  - Environmental_Riau.csv
    - Vegetation, microclimatic, and soil measurements in smallholder plantations, spanning plantation dimensions, neighboring habitats, and environmental context.
    - Variables cover plantation geometry (SideLengths), neighboring habitat types, GPS/centre/t1–t4 references, canopy openness, ground cover (crop, bare ground, ferns, litter, etc.), vegetation height, leaf litter depth, soil moisture, pH, horizon depth, VESS soil structure scores, and weight/quality metrics for soil samples.
    - Includes canopy/light measurements with multiple methods (CanopyOpennessDotsVisual/Numerical, CanopyOpennessVisual/NDots, CanopyOpennessDot counts, etc.).
    - Environmental context around palms (PalmAge, PalmHeight, EpiphyteCover, PalmHealth, PalmHerbivory) and related measurements.
  - Social_Riau.csv
    - Large social survey dataset covering plantation characteristics, management inputs, demographics, and motivational factors across Indonesia and Malaysia.
    - Key areas include PlantationType, PlantationArea, NoPalms, PalmsPerHectare, FarmerAge, Gender, Ethnicity, Education, Income (monthly, OP-specific), LandownerStatus, Intercropping, Crop types, profitability, and time commitments.
    - Management factors: Years in management, ManagementSalary, ManagementMotivation, YearsOnLand, Fertilizer/Herbicide use and costs (cost per ha, annual usage, volumes), intercropping, and organic/manure use.
    - Perception and value of nature: Definition of Nature, Ranked values (Economic, Food, Wildlife, Beauty, Culture, Health, None), and HoursFarming (daily/weekly), plus assessments of soil type and herbicide use.
    - Attitudinal and behavioral indicators: Influence rankings (Neighbours, Scientific, Cost, Effort, Consistency, Yields), and open-ended comments.

- Data linkages and integration
  - Cross-dataset linkage primarily via PlantationCode and GPSCode fields; GPSCode references link to GPSDataRiau.csv (GPS coordinates storage) for spatial analyses.
  - Multi-day and multiple-plot data allow temporal and spatial cross-dataset analyses (e.g., canopy/opening vs. pollinator counts, soil properties vs. palm health, trap abundances vs. weather conditions).

- Data quality, formats and preparation considerations
  - Variety of formats and units across datasets (temperatures, dates, times, percentages, counts, metres, centimetres, currency; some fields include typographical inconsistencies).
  - Some fields reference free-text descriptions (WeatherCond, Notes) requiring standardization for machine-readability.
  - Large, descriptive data dictionaries are provided, but consolidation into a unified data dictionary and standardized schemas would aid self-serve analysis.
  - Potential data quality tasks: harmonize date/time formats, unify unit conventions (e.g., height, canopy metrics, moisture scales), validate GPS linkages, and resolve any inconsistent field naming.

- Practical data products and use cases (Data Support perspective)
  - Dashboards or pivot-table style reports enabling:
    - Spatial biodiversity patterns by plot and time (data from Transects, Inflorescences, Pitfalls, StickyTraps, and DataLoggers).
    - Relationships between canopy openness, soil properties, vegetation structure, and arthropod abundance.
    - Palm health, herbivory, epiphyte cover, and management practices across plantations (Environmental_Riau.csv and PalmHealth-related fields).
    - Social-ecological insights: how management motivations, cost pressures, and intercropping relate to biodiversity outcomes and inputs (Social_Riau.csv).
  - Data dictionaries and data dictionaries-enhanced metadata to support reuse and sharing.
  - Potential geospatial maps using GPS coordinates and GPSDataRiau.csv for visualization of plot-level biodiversity and environmental gradients.
  - Longitudinal analyses combining hourly/daily environmental data (DataLoggers_Riau.csv, Environmental_Riau.csv) with field observations (Inflorescences_Riau.csv, Transects_Riau.csv).

- Challenges and recommendations for the Data Support archetype
  - Challenges reflected in the dataset collection:
    - Patchy data and wide range of data formats across multiple topics (biodiversity, environmental, and social data).
    - Complex linking across datasets via multiple keys (PlantationCode, GPSCode) requiring careful data integration.
    - Communication of complex, multi-domain information (e.g., canopy openness, soil scores, and pollinator counts) for end users.
  - Recommendations:
    - Develop a centralized data dictionary mapping field names to standardized data types, units, and allowed values.
    - Create data cleaning pipelines to harmonize dates, times, units, and taxonomic/ordinal fields.
    - Implement consistent keys (PlantationCode, GPSCode) and validate cross-dataset linkages.
    - Build modular data products (dashboards, maps) that allow end users to filter by plantation, date, or dataset type and to export analysis-ready subsets.
    - Document data provenance and collection notes to aid reuse and reproducibility across projects and locations.