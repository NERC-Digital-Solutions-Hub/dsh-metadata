# Riau Biodiversity Survey Data (Multiple CSV Files)

- An integrated set of datasets from biodiversity surveys and environmental assessments conducted in smallholder oil palm plantations in Riau, Sumatra, Indonesia, with additional context from related sites in Malaysia.

- Data streams include:
  - Microclimate and logger-based temperature data
  - Inflorescence-level pollinator observations
  - Pitfall trap arthropod abundances (by taxon)
  - Transect-based insect and arachnid observations (butterflies, spiders, and assassin bugs)
  - Trap, logger, and bait-card deployment and collection timing
  - Sticky trap arthropod abundances (by order)
  - Environmental, vegetation, microclimate, and soil measurements
  - Socio-economic and management questionnaire data for plantation managers

- Key linking identifiers and linkage:
  - PlantationCode (Plot ID) used across multiple datasets to align plot-level data
  - SamplePoint identifiers (e.g., T1–T4, and T1–T4 sub-sampling points) for precise site localization
  - GPSCode and GPSCodeCorner fields with links to GPSDataRiau.csv for spatial coordinates
  - Date and time fields (e.g., DateDay1, DateDay2, StartTime/EndTime, HH:MM formats) to enable temporal alignment
  - Weather and environmental descriptors (WeatherCondition, WeatherCond, WeatherConditionPM/VM, etc.)
  - For environmental data, multiple vegetation and soil metrics are captured by location and sampling point

- Datasets and their focus (high-level):
  - DataLoggers_Riau.csv: hourly air temperature readings from data loggers within plots (TempHr1–TempHr25)
  - Inflorescences_Riau.csv: oil palm inflorescences with pollinator observations on two separate days, including flower openness, pollinator counts, canopy openness, ground cover, and palm characteristics
  - Pitfalls_Riau.csv: pitfall-trap abundance by arthropod groups (sorted largely to Order level, with some taxa counted separately for abundant groups)
  - Transects_Riau.csv: observational data for butterflies, orb-weaving spiders, and assassin bugs, with weather and microhabitat context and counts for flying/resting/sunning/interacting/nectaring
  - Traps_Riau.csv: deployment and collection timing for pitfall traps, sticky traps, dataloggers, and bait cards, plus notes and equipment identifiers
  - StickyTraps_Riau.csv: sticky-trap arthropod abundances by major taxa and total specimen counts
  - Environmental_Riau.csv: vegetation, microclimate, and soil conditions at plantation plots, including plantation dimensions, crop cover, canopy/opening metrics, soil moisture/pH, soil depth, soil structure (VESS-related scores), and related vegetation metrics
  - Social_Riau.csv: plantation managers’ socio-economic and attitudinal data, including plantation characteristics, management motivations, nature-value rankings, income, intercropping, and perceived influences on management decisions

- Variables, units, and data types (representative highlights):
  - Temperature: Celsius (TempHr1–TempHr25; AirTemp, etc.)
  - Activity and abundance counts: integers (e.g., Ants, Bees, Lepidoptera, Flying/Resting/Nectaring counts)
  - Percent cover/flowers: percentages (e.g., FlowersFullyOpen, GroundCover, CanopyOpenness)
  - Spatial: metres, hectares, GPS coordinates (via GPSDataRiau.csv)
  - Temporal: dates (YYYY-MM-DD), times (HH:MM), and date-time fields for day-based observations
  - Plant and palm metrics: height (metres), leaf litter, palm health (ordinal scales), age/frond metrics
  - Soil: moisture (scale 1–10 or numeric), pH (numeric), horizon depth (cm), VESS-related scores
  - Socio-economic: income, years in location/management, education, employment, intercropping, management motivations, and responses to nature-value questions (rankings and open-text notes)

- Data integration and quality considerations:
  - Multiple datasets are designed to be joined on common keys (e.g., PlantationCode, SamplePoint, GPSCode, and Date/Time fields) to build plot-level and time-series views.
  - Spatial linking relies on GPS codes and GPSDataRiau.csv; ensure consistent matching of GPSCode fields across datasets.
  - Some fields contain complex descriptive text and potential formatting inconsistencies (e.g., long descriptive columns and occasional garbled descriptions). Data cleaning may be required to standardize variable names, units, and categories.
  - Scale and granularity differences exist (plot-level environmental data vs. point-level biodiversity observations; hourly temp vs. daily/observation-level counts). Analysts may need to aggregate or align temporally and spatially for specific analyses.
  - The Social_Riau.csv block indicates a multi-location context (SMARTRI sites, Wild Asia sites, Banting; some fields may be location-specific). Consider site-level stratification in analyses.

- Analytic opportunities for data-driven questions:
  - How do microclimatic conditions (temperature, humidity, canopy openness, soil moisture) relate to arthropod abundance and pollinator activity?
  - What is the relationship between inflorescence traits (flowers open/closed, stage, palm height) and observed pollinator assemblages across two observation days?
  - Do ground- and canopy-level environmental factors (ground cover, leaf litter, soil pH/moisture, horizon depth) predict arthropod community structure captured by pitfall and sticky traps?
  - How do environmental and habitat features correlate with wildlife presence and interspecific interactions on plantations?
  - What socio-economic factors and management motivations drive responses in herbicide use, intercropping, and management intensity, and how do these relate to perceived nature value and wildlife observations?
  - Cross-dataset analysis enabling plots to be evaluated for biodiversity outcomes alongside plantation management practices and economic performance

- Data access, metadata, and next steps for analysts:
  - Core linking keys: PlantationCode, SamplePoint, GPSCode, and GPSCodeCorner fields, plus Date/Time fields for temporal alignment
  - GPS and spatial data are linked to a central GPSDataRiau.csv resource for precise geolocations
  - Metadata and variable definitions are provided within each dataset description; expect some formatting inconsistencies in text descriptions that may require data cleaning
  - Recommended workflow:
    - Compile a master dataset by joining on PlantationCode and SamplePoint across relevant datasets
    - Normalize units and categorical encodings (e.g., canopy openness, health scores)
    - Align temporal data (hourly temperatures from DataLoggers_Riau with day-level observations in Inflorescences_Riau and Transects_Riau)
    - Perform exploratory data analysis to assess data completeness by plot and by day
    - Build multivariate models to link environmental predictors with biodiversity and management outcomes
    - Document data provenance, transformations, and any assumptions to support reproducibility

- Quick reference: what each dataset offers at a glance
  - DataLoggers_Riau.csv: hourly temperature records by data logger within plots
  - Inflorescences_Riau.csv: inflorescence-level pollinator observations, flower status, ground/canopy metrics, palm attributes, and two-day pollinator counts
  - Pitfalls_Riau.csv: pitfall trap counts by broad arthropod groups and orders
  - Transects_Riau.csv: butterfly, orb-weaving spider, and assassin bug observations with weather and microhabitat context
  - Traps_Riau.csv: deployment and collection timing for traps, loggers, and bait cards; event-level metadata
  - StickyTraps_Riau.csv: sticky-trap arthropod abundances by taxon and total counts
  - Environmental_Riau.csv: environmental, vegetation, microclimate, and soil measurements per plantation plot
  - Social_Riau.csv: plantation managers’ socio-economic data, management motivations, nature-value rankings, intercropping, and related factors across multiple study locations

- Bottom line for analysts:
  - A rich, multi-faceted data package enabling integrated analyses of microclimate, plant-pollinator interactions, arthropod diversity, habitat variables, environmental conditions, and socio-economic drivers within oil palm plantations in Riau. Thoughtful data harmonization and careful linking across datasets will unlock insights into how environment, management, and biodiversity interrelate at the plot level.