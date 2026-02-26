# Environmental_Riau.csv

- A collection of datasets documenting biodiversity surveys, environmental conditions, and social-technical aspects of oil palm plantations in Riau, Sumatra, Indonesia. Data are organized into multiple CSV files covering datalogger temperatures, inflorescences, pitfall traps, transects, traps, sticky traps, environmental measurements, and social management surveys.

## Dataset Descriptions and Key Content

- DataLoggers_Riau.csv
  - Location and hourly air temperature data from data loggers deployed during biodiversity surveys.
  - Key fields: PlantationCode, SamplePoint (T1–T4), TempHr1–TempHr25 (air temperatures for each hour after deployment).
  - Purpose: sites-level temperature profiles within plots to relate to biodiversity observations.

- Inflorescences_Riau.csv
  - Observations of oil palm inflorescences, including pollinator activity and floral openness.
  - Key fields: InflorescenceID, PlantationCode, WeatherConditionDay1, DateDay1, SurveyStartTimeDay1, Pollinator counts (African Oil Palm Weevil, Yellow Crazy Ant, Weaver Ant, Bees, etc.), Flower status (FlowersFullyOpen, FlowersPartiallyClosed, FlowersClosed), canopy/open ground cover metrics, ground cover and vegetation metrics around palms, CanopyOpenness, observation times, and pollinator counts on both day 1 and day 2.
  - Purpose: quantify inflorescence phenology, pollinator assemblages, and microhabitat context during flowering periods.

- Pitfalls_Riau.csv
  - Abundance data for arthropods captured in pitfall traps, with major taxa counted (ants, termites, beetles, etc.) and totals by order.
  - Key fields: PitfallTrapSetupDate/Time, PitfallTrapCollectionDate/Time, SamplePoint (T1–T4), counts by taxonomic groups, TotalSpecimenNumber, OrdinalAbundance, notes.
  - Purpose: ground-dwelling arthropod community sampling to assess biodiversity and habitat quality within plots.

- Transects_Riau.csv
  - Observational data for butterflies, orb-weaving spiders, and assassin bugs along transects, including activity and microhabitat context.
  - Key fields: SpeciesID, PlantationCode, WeatherCond, Date, TimeSeenCaught, Microhabitat, counts for Flying, Resting, Sunning, Interacting, Nectaring, and associated flowering plant IDs when applicable.
  - Purpose: species presence/activity and microhabitat associations during transect surveys.

- Traps_Riau.csv
  - Setup and collection data for diverse trap types (pitfall, sticky, datalogger, bait cards), plus notes on trap outcomes.
  - Key fields: WeatherCondSetup, DateSetup, StartTimeSetup, EndTimeSetup, trap-specific setup times (PitfallTrapSetupTimeT1…T4, StickyTrapSetupTimeT1…T4, DataLoggerSetupTimeT1…T4), Datalogger numbers, BaitSetupTimePalm1…Palm4, MealwormsRemainingPalm1…Palm4, Notes.
  - Purpose: track deployment and retrieval timing, identification codes, and bait-card/mep residuals for lifecycle of sampling effort.

- StickyTraps_Riau.csv
  - Abundance data for arthropods captured on sticky traps, with counts by major groups and total specimens.
  - Key fields: StickyTrapSamplePoint (T1–T4), StickyTrapSetupTime/Date, StickyTrapCollectionTime/Date, counts for Ants, Termites, Wasp, NonAntHymenoptera, Coleoptera, Dermaptera, Diptera, Hemiptera, Lepidoptera, Odonata, Orthoptera, Araneae, TotalSpecimenNumber, OrdinalAbundance, FurtherNotes.
  - Purpose: complementary arthropod sampling to pitfall data, emphasizing surface-dwelling taxa.

- Environmental_Riau.csv
  - Vegetation structure, microclimate, and soil condition data from environmental surveys in smallholder plantations.
  - Key fields: plantation geometry, dates/times, weather during mapping, crop types and percent cover, GPS references for plantation corners/centers/sampling points, side length measurements, neighboring habitat categories, canopy openness, various vegetation cover types (crop, bare ground, ferns, other vegetation, leaf litter, palm fronds), vegetation height measures, soil moisture/pH, horizon depth, soil block evaluations (VESS) with depth layers and Sq scores, leaf litter depth, soil weights.
  - Purpose: comprehensive environmental baseline characterizing plantation context, soil health, microclimate, and adjacent landscapes.

- Social_Riau.csv
  - Management and socio-economic survey data from SMARTRI sites (Indonesia) and other locations (Malaysia), covering plantation characteristics, management inputs, demographics, attitudes toward nature and oil palm, intercropping, and decision-making motivators.
  - Key fields (sampling of broad topics): PlantationType, PlantationArea, NoPalms, PalmsPerHectare, FarmerAge, MaritalStatus, HouseholdSize, Ethnicity/Nationality, YearsInLocation, Gender, Education, OtherEmployment, Income, AgriculturalPreference, Intercropping, CropTypes, Intercropping motivations, wildlife presence, opinions on soils, herbicide use and costs, fertilizer use and motivations, organic manure, non-tree crops, yield-related metrics, management influence rankings (neighbors, scientific, cost, effort, consistency, yields), harvest frequency, prices, buyers, and open-ended questions.
  - Purpose: capture human dimensions of plantation management, socio-economic drivers, and values related to nature and agricultural practices.

## Data Structure and Quality Considerations

- Common data elements aligned across files
  - PlantationCode and SamplePoint frequently used to link site-level observations across data types.
  - Date and Time fields (Date, StartTime, EndTime) enable temporal analyses and alignment with environmental conditions.
  - GPSCode references to GPSDataRiau.csv for spatial linking of coordinates (e.g., plantation corners, center, and sampling points).
  - Units are specified for numeric fields (e.g., °C, m, %), though there are formatting inconsistencies in the text that would require cleaning.
- Data quality and transformation needs
  - Inconsistent column names and typographical errors present (e.g., misformatted descriptors, duplicated sections), requiring standardization and cleaning before analysis.
  - Some fields contain long explanatory notes that would need parsing or documentation as metadata.
  - Cross-dataset linking will benefit from consistent GPS referencing and standardized date-time formats.
- Data governance and storage
  - Outputs are intended to be stored and uploaded to appropriate portals; standard QA, cleaning, and transformation steps should be applied to ensure datasets are ready for sharing and long-term preservation.

## Analytical Perspectives for Analysts Monitoring the Environment

- How these data support monitoring aims
  - Provide time-series (DataLoggers_Riau.csv) and event-based (Inflorescences_Riau.csv, Transects_Riau.csv, Traps_Riau.csv, StickyTraps_Riau.csv) perspectives on biodiversity, habitat quality, and environmental conditions.
  - Offer multi-taxa biodiversity indicators (arthropod communities, pollinators, butterflies, spiders, etc.) alongside habitat structure (Environmental_Riau.csv) and microclimate measurements.
  - Include social-ecological dimensions (Social_Riau.csv) to relate management decisions, economic drivers, and attitudes toward nature to environmental outcomes.
- Standardized outputs and formats
  - The presence of clearly described fields facilitates the production of reports, maps, and charts that show spatial and temporal trends in biodiversity, habitat quality, and management practices.
  - Datasets are designed for integration, enabling correlation analyses between environmental variables (e.g., canopy openness, soil moisture) and biodiversity measures (e.g., insect abundance, pollinator activity).
- Data integration opportunities
  - Link environmental measurements (Environmental_Riau.csv) with biodiversity observations (DataLoggers_Riau.csv, Inflorescences_Riau.csv, Transects_Riau.csv, Pitfalls_Riau.csv, StickyTraps_Riau.csv) to assess how abiotic factors influence biotic communities.
  - Combine social-economic context (Social_Riau.csv) with environmental and biodiversity data to explore drivers of habitat change, management decisions, and potential policy implications.

## Practical Considerations for Use

- Data processing steps for analysts
  - Clean and standardize column names and units across CSVs.
  - Validate and harmonize dates/times; ensure time zones are consistent.
  - Resolve any inconsistencies in SpeciesIDs, GPS references, and sampling point nomenclature to enable reliable cross-dataset joins.
  - Document data provenance and quality checks to support reproducibility.
- Outputs to inform monitoring and policy
  - Temporal trend analyses of temperature, canopy openness, and ground cover.
  - Biodiversity indices by plot and time, related to environmental variables.
  - Spatial maps showing plot locations, sampling points, and habitat features linked to biodiversity metrics.
  - Socio-ecological insights on management practices, costs, and motivations that influence environmental outcomes.

## Challenges and Opportunities

- Challenges
  - Cleaning and standardizing a multi-file, multi-format dataset with inconsistent metadata.
  - Ensuring robust linkage across datasets through common keys (e.g., PlantationCode, GPSCode, SamplePoint).
  - Managing data access and versioning for portals and stakeholders.
- Opportunities
  - Enhancing data value by integrating ecological measurements with socio-economic context to support policy evaluation and targeted conservation or management actions.
  - Enabling broader data sharing and transparency by applying consistent QA/QC and metadata standards.