# Environmental_Selangor_perimeter_centre.csv; Environmental_Selangor_SamplePoints.csv; Social_Selangor.csv

## Overview
- Three linked datasets describing oil palm plantations in Banting, Peninsular Malaysia, plus related social survey data.
- Environmental and vegetation measurements alongside plantation characteristics, management inputs, and socio-demographic factors.
- Data collected to enable understanding of how environmental conditions, vegetation structure, and management decisions relate to plantation performance and biodiversity.

## Datasets and key variables

- Environmental_Selangor_perimeter_centre.csv
  - Transect-based environmental data: five spatially reproducible transects per study plantation.
  - Key fields: PlantationCode, Description (Plot ID), PlantationType (Immature Poly/Mono, Mature Mono), WeatherDay1, DateDay1, SurveyStartTime, SurveyFinishTime, PlantationZone (Central or PSide1–4), GPSCode, PlotWidth, PlotLength, TotalNumberOfPalms, ModalPalmAge.
  - Vegetation and land-use context: TotalOtherCropCover and multiple OtherCropXCover fields (e.g., BananaCover, CassavaCover, CoconutCover, etc.), Neighbouring land-use percentages (OPMono/Poly, Housing, Road, Grassland, NonOPCrop, OtherSum), NeighbouringHabitatTypesNotes.
  - Additional variables: canopy and habitat indicators, habitat notes, and other survey descriptors.

- Environmental_Selangor_SamplePoints.csv
  - Four spatially reproducible sample points per plantation; second visit (48 hours after initial visit).
  - Key fields: PlantationCode, DateDay2, SamplePoint (1–4), GPSCode.
  - Soil and microclimate metrics: SoilMoisture, Light, CanopyOpennessN/S/E/W (each 0–96 dots from spherical densiometer).
  - Vegetation and palm context: VegetationCoverBare, PalmCover, OtherCropCover, LeafLitter, VegetationHeight1–3, AverageVegetationHeight, DistanceFromNearestPalm, PalmAge, PlamHeight, TotalEpiphyteCover/Richness, EpiphyteSpecies, PalmHerbivoryScore, PalmFungalScore, PalmRhinoBeetleScore, Notes.
  - Epiphytes and palm health signals around the nearest palm to each sample point.

- Social_Selangor.csv
  - Social-technical survey data replicated across three locations (SMARTRI in Indonesia, Wild Asia in Perak, Malaysia, and Banting in Malaysia) describing plantation management and household characteristics.
  - Plantation and farm context: PlantationCode, Description, PlantationArea, TotalNoPlantationsOwned, TotalPlantationAreaOwned, NoPalms, PalmsPerHectare.
  - Respondent demographics and residence: FarmerAge, MaritalStatus, HouseholdSize, Nationality, Ethnicity, Birthplace, YearsInLocation, Gender.
  - Education and employment: FurthestEducation, OtherEmployment, FormOfEmployment, YearsInManagement.
  - Economic indicators: TotalMonthlyIncome, OPMonthlyIncome, PercentageIncomeFromAgriculture, AgriculturalPreference, LandownerStatus.
  - Management motivation and practices: YearsOnLand, YearsLandOP, PreOPLandUse, RecentLandConversion, ReasonForConversion, WhyOP, DefinitionOfNature, RankedImportanceNature_* (economic, food, wildlife, beauty, culture, health, none), HoursFarmingDaily/Weekly/PerHA, SoilType, OpinionOnSoil, UseOfHerbicide, HerbicideType, HerbicideApplicationsAnnual, HerbicideCostAnnual/PerHAAnnual, HerbicideLitresAnnual/PerHAAnnual, Intercropping, CropTypes, MostProfitableCrop, IncomeOtherCrop, TimeCommitmentOP, OrganicManureUse, FertilizerUse/Type/Motivation, FertilizerCostAnnual/PerHAAnnual, FertilizerAmountAnnual/PerHAAnnual, FertilizerApplicationMethod, FertilizerMotivation_* (Season, Neighbour, Advice, Manager, PalmCondition, etc.), OrganicManureUse, Intercropping, MostProfitableCrop, WildlifePresence, AnimalsSeenDaily, Favorite/Second Favorite/Least Favorite animals and reasons, ManagementInfluenceRank_* (Neighbours, Scientific, Cost, Effort, Consistency, Yields), Harvests and yield/price data (NoOPHarvestsMonthly, AmountOPYieldMonthly/PerHAMonthly, PriceOPYieldMonthly/PerHAMonthly, OPBuyer), NonOPHarvestsMonthly, NonOPBuyer, OtherComments.

## Study design and geography
- Location: Banting, Peninsular Malaysia; cross-location elements include three sites in the social dataset (Indonesia and Malaysia) to support comparative analyses.
- Data collection structure:
  - Environmental perimeter data from 5 transects per plantation.
  - Sample-point environmental data collected on a second visit (4 points per plantation) 48 hours after the first visit.
  - Social survey capturing plantation characteristics, management inputs, and respondent demographics and attitudes toward nature.

## Data collection timeline
- Environmental perimeter data: initial site visit.
- Sample-point environmental data: second visit, 48 hours after the initial visit.
- Social survey: concurrent across three locations, with consistent survey instrument.

## Data quality and formatting notes
- Wide variety of data types: Characters, Integers, Numerics, Dates, Times.
- Some fields contain NA values; currencies span Malaysian Ringgit and Indonesian Rupiah.
- Units: Plot dimensions in metres; palm counts; canopy openness scores; distances in feet; yields in kilograms; area in hectares.
- Data are descriptive metadata for schema fields; actual data values would require parsing and cleaning for integration.

## Potential data products and use cases (Data Support perspective)
- Environmental dashboards:
  - Transect-level environmental indicators (temperature, weather notes, canopy openness, soil moisture where available).
  - Vegetation and land-use context around plantations, including neighboring land use and habitat notes.
- Plantation health and ecology:
  - Palm density, age class, and health proxies (epiphyte load, herbivory and fungal scores) linked to sample-point data.
  - Canopy openness and light availability related to understory vegetation and palm performance.
- Management and socio-economic insights:
  - Relationships between management motivations, inputs (herbicide/fertilizer), intercropping, income, and productivity.
  - Attitudes toward nature and regulatory or market influences on management decisions; influence rankings (Neighbours, Scientific, Cost, Effort, Consistency, Yields).
  - Wildlife presence and attitudes, plus observed animals, to explore human–nature interactions on plantations.
- Cross-dataset analyses:
  - Linking environmental conditions (transects and sample points) with social factors (management decisions, inputs, income) via PlantationCode as the join key.
  - Comparative analyses across locations in the social dataset to identify cultural or economic drivers of management practices.

## Data preparation and integration tips (Data Support actions)
- Key identifiers for merges:
  - PlantationCode serves as primary key across environmental datasets; SamplePoint adds granularity within plantations.
- Data cleaning considerations:
  - Standardize units (metres, hectares, kilograms, currency), parse dates (DateDay1, DateDay2) and times (SurveyStartTime, SurveyFinishTime).
  - Harmonize categorical fields (e.g., PlantationType, Gender, Yes/No flags) and handle NA values appropriately.
- Data quality enhancements:
  - Create a data dictionary and data provenance notes to document field meanings and any transformations.
  - Validate geographic coordinates and GPS codes; assess missing transect or sample-point data to identify coverage gaps.
- Analytical readiness:
  - Prepare derived metrics (e.g., palm density per hectare, average canopy openness, total herbicide cost per hectare) to facilitate dashboards.
  - Establish join pipelines to combine environmental and social data via PlantationCode, and where needed, link to spatial context (PlotWidth/PlotLength, Neighbouring land-use variables).

## Challenges and considerations for Data Support
- Time spent understanding the ask due to data being collected for multiple topics and in patchy formats.
- Accessing and reconciling data across different systems and locations.
- Communicating complex, multi-variable environmental and social data succinctly.
- Ensuring outputs are promoted and reused; managing versioning and feedback to iterate on data products.

## Recommendations for data work moving forward
- Build a centralized data dictionary and data integration plan for the three datasets.
- Develop a set of starter dashboards (environmental fidelity, palm health indicators, and management inputs vs. productivity) to enable self-serve exploration.
- Prioritize data quality improvements (unit consistency, missing-value handling, and documentation) to reduce integration friction.
- Establish a routine for sharing early prototypes and gathering user feedback to broaden reuse and improve data products.