# DataLoggers_Riau.csv

- This document describes a collection of biodiversity, environmental, and agronomic data from biodiversity surveys in Riau, Sumatra, Indonesia, linked to oil palm plantations.

## Overview of dataset collection

- Focus: biodiversity monitoring in oil palm plantations using multiple data collection methods (dataloggers, inflorescence surveys, pitfall and sticky traps, transect observations), plus environmental and social context data.
- Geography: Riau, Sumatra, Indonesia; ties to multiple field plots (PlantationCode) and sampling points (e.g., T1–T4).
- Linkages: many datasets reference GPS coordinates via GPSCode(s) and links to GPSDataRiau.csv; temporal data include dates and times for setup, collection, and observations.

## Datasets included and what they cover

- DataLoggers_Riau.csv
  - Location and temperature measurements from data loggers deployed during biodiversity surveys.
  - Key fields: PlantationCode, SamplePoint (T1–T4), TempHr1–TempHr25 (hour-by-hour air temperature), plot identifiers.
- Inflorescences_Riau.csv
  - Observations of oil palm inflorescences, including flower opening status and pollinator observations.
  - Key fields: InflorescenceID, PlantationCode, DateDay1, WeatherConditionDay1, pollinator counts on Day 1 and Day 2, floral openness percentages, ground cover around palms, canopy openness, and associated pollinators.
- Pitfalls_Riau.csv
  - Abundance data for arthropods captured in pitfall traps.
  - Key fields: PitfallTrapSetupDate/Time, PitfallTrapCollectionDate/Time, counts by taxa (e.g., Ants, Termites, Coleoptera, etc.), TotalSpecimenNumber, OrdinalAbundance.
- Transects_Riau.csv
  - Observational data for butterflies, orb-weaving spiders, and assassin bugs, with weather and microhabitat notes.
  - Key fields: SpeciesID, Date, TimeSeenCaught, Microhabitat, Flying/Resting/Sunning/Interacting/Nectaring counts, FloweringPlantID.
- Traps_Riau.csv
  - Setup and collection times for various traps and devices (pitfall traps, sticky traps, dataloggers, bait cards); includes GPS and weather notes.
  - Key fields: Setup/Collection dates and times, GPS/link codes, WeatherCondSetup/WeatherCondCollection, multiple per-point timing details (e.g., PitfallTrapSetupTimeT1…T4, BaitSetupTimePalm1…Palm4, DataLoggerSetupTime, etc.).
- StickyTraps_Riau.csv
  - Abundance data for arthropods captured on sticky traps; counts by taxa and total.
  - Key fields: StickyTrapSamplePoint, Setup/Collection dates and times, counts by major taxa (Ants, Termites, Wasp, Coleoptera, etc.), TotalSpecimenNumber.
- Environmental_Riau.csv
  - Vegetation, microclimate, and soil conditions across plantations; includes plantation dimensions and neighboring environments.
  - Key fields: CropTypeName1–4 and percentages, CanopyOpenness, CanopyOpennessDots/Visual, AirTemp/AirHumidity, SoilMoisture/SoilpH, Horizon depths, VESS-related soil layer data, litter and ground cover metrics, GPS corners and plantation geometry, and several habitat context indicators.
- Social_Riau.csv
  - Socio-economic and management data from plantation managers across Indonesia and Malaysia; captures plantation characteristics, management practices, demographics, perceptions of nature, and economic variables.
  - Key fields: PlantationType/Area, NoPalms/PalmsPerHA, farmer demographics (Age, Gender, Ethnicity, Education), management factors (YearsInManagement, ManagementSalary, ManagementMotivation), financials (Income, OPIncome), intercropping and crop types, herbicide/fertilizer use and motivations, wildlife observations on plantations, and perceived influences on management decisions.

## Data structure and integration notes

- Common keys and linkages:
  - PlantationCode serves as a primary plot identifier across several datasets.
  - Sampling points T1–T4 (and subpoints in Environmental_Riau.csv) provide consistent spatial references within plots.
  - GPSCode and GPSCodeCorners/T1/T2/etc. link records to GPSDataRiau.csv for geospatial context.
- Data types and units:
  - Temperature, humidity, soil properties, and canopy metrics are numeric with explicit units (e.g., °C, %, cm, m).
  - Dates and times are captured in standard formats (YYYY-MM-DD, HH:MM, or Time).
  - Some field descriptions include detailed measurement protocols (e.g., densiometer-based canopy openness, VESS soil structure scoring).
- Scope and granularity:
  - High-resolution, multi-method biodiversity and environmental monitoring at plantation level.
  - Datasets capture short-term (hourly/daily) metrics and longer-term plantation-level context (management practices, land-use history).

## Data quality and management considerations

- Metadata depth is strong for cross-dataset integration, enabling multi-omic or multi-model analyses (biodiversity, habitat condition, and plantation management).
- Some field descriptions show formatting irregularities and truncations (e.g., occasional typos or multi-line artifacts) that may require data cleaning and standardization during ingestion.
- Inter-dataset consistency relies on shared keys (PlantationCode, GPS codes, T1–T4 sampling points), facilitating joint analyses but necessitating careful join rules and data provenance tracking.
- Timelines and events are captured with setup and collection timestamps across traps and sensors, enabling temporal alignment but requiring careful time zone and daylight-saving considerations if integrating beyond the study area.
- The Social_Riau.csv dataset spans multiple locations with a unified survey instrument, enabling comparative analyses while accounting for site-level heterogeneity.

## Relevance for Data Leaders

- Data landscape clarity: The collection provides a comprehensive, multi-method view of biodiversity, plantation environment, and management context in oil palm landscapes, with explicit cross-dataset linking keys.
- User needs and co-ownership: Rich, plot-level data support researchers and policy colleagues seeking integrated analyses of habitat condition, pollinator dynamics, and management practices; potential for co-ownership of data products through shared identifiers.
- Data availability and gaps: High granularity and breadth are strengths, but harmonization across datasets (especially field descriptions with formatting inconsistencies) will be necessary for scalable reuse.
- Data stewardship: Clear references to data formats, units, and metadata enable improved discoverability, discoverability is aided by common identifiers (PlantationCode, GPSCode), and updates appear feasible given hourly/date-time fields.

## Potential uses for Data Leaders

- Develop a holistic data strategy that centers on core plantation-level keys (PlantationCode, GPS links) to enable cross-dataset analytics (biodiversity metrics, vegetation structure, soil health, and management practices).
- Build data products that combine environmental and socio-economic dimensions to assess how plantation management influences biodiversity and ecosystem services.
- Establish data standards and quality checks across files to improve interoperability and reduce the need for repeated data cleaning.
- Facilitate collaboration with partner networks by defining standardized data schemas and shared discovery mechanisms for these Riau datasets.