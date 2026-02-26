Data on the set-up and collection times for sticky traps, dataloggers and bait cards deployed during biodiversity surveys at 24 oil palm smallholder farms in Perak, Malaysia, with details on the number of mealworms remaining on the bait cards at collection.

# Overview

- Study context: Biodiversity and environmental monitoring at 24 oil palm smallholders in Perak, Malaysia, during 2022 (May–July) with additional environmental data from Dec 2021–Feb 2022.
- Collaborations: Smallholders categorized as 1) WAGS-BIO (trained for sustainable methods; RSPO/MSPO-certified), 2) WAGS (information on RSPO/MSPO; potential RSPO assessments), 3) Independent farmers (no Wild Asia involvement).
- Goals: Assess effects of plantation management on soil, insect communities, predation, vegetation structure, and microclimate; support environmental health and policy monitoring with standardized data formats.
- Data flow: Field teams collect in the field; data and images uploaded/verified by researchers at the University of Cambridge for quality control and standardization.

# Dataset A: Set-up and collection times, dataloggers, sticky traps, and bait cards

- Scope: Setup and collection events for traps, dataloggers, and bait cards at 24 farms, across four sampling points per farm (T1–T4), using 96 locations total.
- Methods:
  - Sticky traps: 30 cm x 30 cm, transparent, glue-coated, suspended 40 cm above ground; collected after 24 hours and photographed for later counting.
  - Dataloggers: Thermochron iButton devices, buried at 5 cm depth; set and collected in field campaigns; data logged hourly.
  - Bait cards: Mealworms attached to 10 cm x 6 cards placed on palm trunks; collected after 24 hours to assess remaining mealworms.
- Data captured (examples of fields):
  - Setup/collection times: Start/End times for traps, dataloggers, bait cards at each sampling point (T1–T4).
  - Unique IDs: DataLoggerNumberT1–T4 identifying each datalogger.
  - Weather and conditions: Weather during setup/collection; free-text notes.
  - Mealworms: MealwormsRemainingPalm 1–4 (0–6 per card, measured to nearest 0.25).
  - Palm/trap specifics: Palm IDs, sampling point, and notes on setup.
- Data handling: Field data entered/uploaded, then quality-checked and standardized at Cambridge; field images of sticky traps used for insect identification.
- Key variables (examples):
  - PlantationCode, StickyTrapSamplePoint (T1–T4), StickyTrapSetupDate/Time, StickyTrapCollectionDate/Time, WeatherCondSetup/Collection, DataLoggerSetupTime, DataLoggerNumberT1–T4, BaitSetupTimePalm1–Palm4, MealwormsRemainingPalm1–Palm4, Notes.

# Dataset B: Insect and microhabitat observations

- Scope: Observations of butterflies, Nephila orb-weaving spiders, assassin bugs, and associated microhabitats across the same 24 farms; includes weather and air temperature during surveys.
- Methods: Standard transect walks (100 m) across plantation centers, recording insect activities within a 5 m x 5 m box; species identified with local guides and photos for verification.
- Data captured (examples of fields):
  - SpeciesID, Microhabitat, Date, TimeSeenCaught, WeatherCond, AirTemp.
  - Behavioral categories: Flying, Resting, Sunning, Interacting, Nectaring (for butterflies/dragonflies) with plant species recorded for nectaring.
- Data handling: Data entries quality-checked and standardized; field images identified to order level; weather and temperature logged at time of survey.
- Key variables (examples):
  - PlantationCode, SpeciesID, WeatherCond, Date, TimeSeenCaught, Microhabitat, Flying/Resting/Sunning/Interacting/Nectaring, FloweringPlantID.

# Dataset C: Arthropod abundance from sticky traps

- Scope: Abundance data from sticky traps at 24 farms; counts recorded by order, with emphasis on ants and termites; some sites missing data (NA for unrecovered traps).
- Methods: 24-hour trap exposure; images photographed in-field; insect identifications performed to order level with standard guides.
- Data captured (examples of fields):
  - StickyTrapSamplePoint, Date/Time, Ants, Termites, Wasp, NonAntHymenoptera, Coleoptera, Dermaptera, Diptera, Hemiptera, Lepidoptera, Odonata, Orthoptera, Araneae, TotalSpecimenNumber, OrdinalAbundance, FurtherNotes.
- Data handling: Data uploaded to Cambridge for QA and standardization; counts aggregated by trap and taxonomic group.
- Key variables (examples):
  - Ants, Termites, Wasp, TotalSpecimenNumber, OrdinalAbundance, Taxon-specific counts.

# Dataset D: Vegetation, microclimate, and soil environmental data (47 plantations)

- Scope: Environmental data across 47 plantations, focusing on plantation layout, neighboring habitats, crop diversity, vegetation structure, canopy, and microclimate; collected December 2021–February 2022.
- Sampling design: Central plot point mapped; zigzag transect across plantation center with four sampling locations (T1–T4) for environmental measurements; 3x3 m quadrats for vegetation cover.
- Variables collected (highlights):
  - CropTypeName1–7 and CropTypePc1–7 (crop identity and percent cover); GPS coordinates for corners and plantation center; SideLengthA–L (plot dimensions); SideHabitatA–L (neighbouring habitat identity/cover); Canopy openness (visual and convex-densiometer-based); Plant-related metrics (PalmAgeYr, PalmHeight, PalmEpiphyteCover, PalmHerbivory, PalmHealth); AirTemp/AirHumidity; Leaf litter depth; Soil moisture/pH; A horizon depth; Soil samples (wet/dry weights; soil depth layers; VESS soil structure scores).
  - Soil sampling: 10 cm depth cores; soil sample weights (wet/dry) and moisture/pH measurements; VESS structural scoring for soil layers.
  - GPS and plot metrics: Corner GPS codes, GPSCodeCentre, GPSCodeT1–T4; all data standardized for cross-dataset linking.
- Data handling: Field data uploaded to Cambridge for QA and standardization; visual and instrument-based measurements used; NA used where data not applicable or not collected in certain locations.
- Key variables (examples):
  - PlantationCode, CropTypeName1–7, CropTypePc1–7, GPSCodeCorner1–12, GPSCodeCentre, SideLengthA–L, SideHabitatA–L, CanopyOpennessDotsT1–T4, CanopyOpennessVisualT1–T4, AirTempT1–T4, AirHumidityT1–T4, PalmAgeYrT1–T4, PalmHeightT1–T4, PalmHealthT1–T4, LeafLitterDepthT1–T4, SoilMoistureT1–T4, SoilpHT1–T4, AHorizonDepthT1–T4, VESS scores, SoilSampleWetWeightT1–T4, SoilSampleDryWeightT1–T4.

# Dataset E: Plantation characteristics, management, and socio-demographics (49 plantations; broader project scope)

- Scope: Surveys at 49 plantations (across Perak, plus Riau, Indonesia; Selangor) detailing plantation characteristics, management practices, and sociodemographic factors of managers/farmers.
- Collaboration levels: As above (WAGS-BIO, WAGS, Independent).
- Social data: Self-reported plot area, number of palms, demographics, management practices, wildlife attitudes, yield, and income; many fields anonymized for privacy.
- Plantations and geography: District, Lat/Long (decimal degrees), plantation area, number of palms, palms per hectare, farm ownership, years of management, land tenure, recent land conversions, and reasons for conversion.
- Management and inputs: Fertilizer and herbicide use, costs, volumes, application frequency, herbicide types, and motivations; presence of non-herbicide vegetation controls, intercropping, and organic manure use.
- Attitudes and values: Definitions of nature, rankings of nature’s values (economic, food, wildlife, beauty, culture, health, etc.), and daily/weekly time commitments to farming.
- Economic and market data: Oil palm yields, prices, buyers, and non-oil palm crop income; time spent per hectare; economic motivations and supplier influences.
- Data handling: Ethical approval obtained; data collected via telephone and in-person interviews; self-reported information acknowledged as potentially imperfect; NA used where questions were not answered or not applicable.
- Key variables (examples):
  - PlantationCode, District, Lat/Long, PlantationArea, NoPalms, PalmsPerHectare, FarmerAge, Gender, FurthestEducation, IncomeFromAgriculture, OPMonthlyIncome, OPBuyer, FertilizerUse/Type/Cost/Amount, HerbicideUse/Cost/Liters, Intercropping/CropTypes, WildlifePresence, TimeCommitmentOP, DefinitionOfNature, RankedImportanceNature_Health/Economic/Wildlife/Beauty/Culture, ManagementInfluenceRank_Neighbours/Science/Cost/Effort/Consistency/Yields, NoOPHarvestsMonthly, AmountOPYieldMonthly/PerHAMonthly, PriceOPYieldMonthly/PriceOPYieldPerHAMonthly, OtherComments.

# Data Quality, Standardization, and Accessibility

- Standardization: Cambridge team performed quality checks to ensure realism, timing consistency, and a uniform data format across all datasets.
- Linkage: Datasets share PlantationCode and spatial/time contexts to enable cross-dataset analyses (soil temperature, insects, vegetation, management, and socio-economics).
- Documentation: Detailed variable dictionaries accompany each dataset, including unit specifications and data collection protocols.
- Limitations and caveats:
  - Some fields use NA where data were not applicable or not collected; several datasets rely on self-reported information (social surveys) with potential reporting biases.
  - Partial recovery in some traps or field scenarios led to missing values (e.g., NA in trap counts).

# Relevance for Analysts Monitoring the Environment

- This collection provides standardized, multi-faceted environmental monitoring data across crop systems, enabling cross-cutting analyses of soil conditions, microclimate, vegetation structure, arthropod communities, predator-prey dynamics, and human management influences.
- The dataset architecture supports time-series and spatial analyses, with consistent identifiers (PlantationCode, T1–T4 points, GPS coordinates) to integrate environmental indicators with management practices and socio-economic context.
- The explicit categorization of collaboration levels (WAGS-BIO, WAGS, Independent) allows assessment of governance and policy impact on environmental health outcomes.
- Data quality emphasis and transparent documentation support reproducibility and policy monitoring over time.