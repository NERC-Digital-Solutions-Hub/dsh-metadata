# Data on the locations of and temperatures (in deg C) recorded by dataloggers deployed in the soil during surveys at 24 oil palm smallholder farms in Perak, Malaysia, over approximately a 24-hour period.

## Purpose and scope
- Comprehensive environmental and biodiversity data collected from 24 oil palm smallholder farms in Perak, Malaysia (May 2022–July 2022).
- Four sampling locations per farm (T1–T4), totaling 96 sampling points; dataloggers buried at 5 cm depth to record soil temperatures.
- Three collaborative contexts with Wild Asia (WAGS-BIO, WAGS, Independent) reflecting varying levels of farmer support and certification status (RSPO/MSPO).
- Data cover soil temperatures, insect biodiversity, predator/arthropod sampling, vegetation/microclimate/soil conditions, and plantation-scale social/socioeconomic information.
- Data were curated for a standard format and quality-checked by field teams and the University of Cambridge; some data are self-reported and may include uncertainties.

## Data collection and processing

- Datalogger temperatures
  - 96 soil sampling points across four plots per farm; Thermochron iButton dataloggers buried at 5 cm.
  - Temperature readings recorded hourly for up to 26 hours; data downloaded, checked for realism, and standardized.
  - Variables include PlantationCode, SamplePoint (T1–T4), and TempHr1–TempHr26 (in °C).

- Insect biodiversity and observational data
  - Standard transect walks (100 m) within plantation centers; insect activity recorded in 5 m × 5 m boxes.
  - Data include SpeciesID (binomial name), WeatherCond, Date, TimeSeenCaught, Microhabitat, and counts for Flying, Resting, Sunning, Interacting, Nectaring.
  - Weather and habitat context recorded; field photos used for taxonomic verification; data quality checked by Cambridge.

- Biodiversity sampling with traps and predation cards
  - Sticky traps (30 cm × 30 cm, 40 cm above ground) and 24-hour collection windows; 6 mealworms mounted on predator cards to measure predation.
  - Data include setup/collection times, trap locations (T1–T4), datalogger IDs, and mealworm counts remaining per palm.
  - Insect identifications from trap images performed to order level; data checked and standardized.

- Arthropod abundance on sticky traps
  - Abundance by taxonomic groups (ants, termites, wasps, etc.) with totals and order-level categories; some NA where traps not recovered.

- vegetation, microclimate, and soil environment
  - Environmental mapping across plantations with GPS coordinates, plot dimensions, canopy and vegetation metrics, and neighboring habitat types.
  - Microclimate measurements at sampling points: air temperature and humidity; canopy openness (dots and visual estimates); vegetation height; leaf litter depth.
  - Palm-level measurements: age, height, epiphyte cover, herbivory, health scores.
  - Soil measurements: litter depth, moisture, pH, A-horizon depth, soil sample weights (wet/dry), soil structure via Visual Evaluation of Soil Structure (VESS), soil depth layers, and soil quality scores.
  - Data include extensive tabular fields for CropType, GPS corners, side lengths, neighboring habitats, vegetation cover (cover crops, bare ground, ferns, other vegetation, leaf litter, palm fronds, etc.), and sub-sampling vegetation heights.

- Plantation mapping and social survey
  - Plantation-level characteristics, management inputs, and sociodemographic factors collected from 49 plantations (with broader scope including sites in Indonesia and other Malaysian locations as part of the wider project).
  - Variables cover district, coordinates, plantation area, palm density, landowner status, farmer demographics (age, gender, education, ethnicity, nationality), income, employment, and attitudes toward nature and farming decisions.
  - Ethical approval obtained; interviews conducted in local language, with anonymization and caveats about potential reporting errors acknowledged.
  - Data include numerous variables on management motivation, fertilizer and herbicide use, intercropping, weed control, livestock, and economic factors.

## Datasets and core variables (summary)

- Soil temperature dataset
  - Key fields: PlantationCode, SamplePoint (T1–T4), TempHr1…TempHr26 (°C).

- Insect observations dataset
  - Key fields: SpeciesID (binomial), PlantationCode, WeatherCond, Date, TimeSeenCaught, Microhabitat, Flying, Resting, Sunning, Interacting, Nectaring, FloweringPlantID (if nectaring).

- Sticky traps, datalogger, and bait cards dataset
  - Key fields: PlantationCode, StickyTrapSetupTimeT1–T4, DataLoggerSetupTimeT1–T4, BaitSetupTimePalm1–Palm4, DataLoggerNumberT1–T4, WeatherCondSetup, DateSetup, DateCollection, StartTime/EndTime, collection times, MealwormsRemainingPalm1–Palm4, Notes.

- Arthropod abundance dataset
  - Key fields: Ants, Termites, Wasp, NonAntHymenoptera, Coleoptera, Dermaptera, Diptera, Hemiptera, Lepidoptera, Odonata, Orthoptera, Araneae, TotalSpecimenNumber, OrdinalAbundance, FurtherNotes.

- Vegetation, microclimate, and soil dataset
  - Key fields: GPSCodeCorner1–12, GPSCodeCentre, GPSCodeT1–T4, SideLengthA–L, SideHabitatA–L, CanopyOpennessDotsT1–T4, CanopyOpennessVisualT1–T4, AirTempT1–T4, AirHumidityT1–T4, PalmAgeYrT1–T4, PalmHeightT1–T4, PalmEpiphyteCoverT1–T4, PalmHerbivoryT1–T4, PalmHealthT1–T4, LeafLitterDepthT1–T4, SoilMoistureT1–T4, SoilpHT1–T4, AHorizonDepthT1–T4, SoilSampleWetWeightT1–T4, SoilSampleDryWeightT1–T4, SoilDepthT1Layer1–4, SoilDepthT2Layer1–4, SoilDepthT3Layer1–4, SoilDepthT4Layer1–4, SoilSqScoreT1Layer1–4, SoilSqScoreT2Layer1–4, SoilSqScoreT3Layer1–4, SoilSqScoreT4Layer1–4, ZiplockBagWeight, SoilType, etc.

- Plantation survey (social/economic) dataset
  - Key fields: OldPlotCode, District, Lat, Long, PlantationArea, PalmsPerHectare, FarmerAge, MaritalStatus, HouseholdSize, Nationality, Ethnicity, Birthplace, YearsInLocation, Gender, FurthestEducation, OtherEmployment, PercentageIncomeFromAgriculture, TotalMonthlyIncome, OPMonthlyIncome, LandownerStatus, YearsInManagement, ManagementSalary, ManagementMotivation, YearsOnLand, YearsLandOP, PreOPLandUse, RecentLandConversion, ConversionLocation, ReasonForConversion, SocialOpinionsOnNature, Rankings of Nature values (Health, Economic, Wildlife, Beauty, Culture, etc.), HoursFarmingDaily/Weekly/PerHA, SoilType, OpinionOnSoil, UseOfHerbicide, HerbicideType, HerbicideApplicationsAnnual, HerbicideCostAnnual, HerbicideLitresAnnual, FertilizerUse, FertilizerType, FertilizerCostAnnual, FertilizerAmountAnnual, Intercropping, CropTypes, IncomeOtherCrop, WildlifePresence, AnimalsSeenDaily, Favourite/Second/Least Favourite Animal, ManagementInfluenceRank_Neighbours/Scientific/Cost/Effort/Consistency/Yields, Harvests/Prices, OPBuyer, NonOPBuyer, and other open-ended fields.

## Data governance, quality, and provenance

- Data management and standardization
  - Data were downloaded/entered by field teams and subjected to quality checks at the University of Cambridge to ensure realism and alignment with field timing.
  - Standard data formats and a centralized schema were applied to enable cross-dataset integration.
  - Comprehensive variable-level metadata and units are provided for each dataset.

- Data provenance and documentation
  - Field campaigns conducted by Wild Asia; data linked to precise sampling locations, timestamps, and equipment IDs (e.g., DataLoggerNumber).
  - Observational and measurement methods documented, including handling of uncertain specimens (verification via photos) and self-reported social data caveats.

- Data access and sharing
  - Data were uploaded to the University of Cambridge systems and catalogued for discovery, with potential publication in relevant portals; documentation exists for data processing steps.
  - Collaboration level information (WAGS-BIO, WAGS, Independent) informs data context and reuse considerations.

- Ethics and privacy
  - Social survey data obtained with ethics approval; participant anonymity maintained; some fields are NA to protect privacy where necessary.

## Practical considerations for Data Stewards

- Data model alignment
  - Large, multi-table dataset with many long, domain-specific variables; ensure consistent naming, units, and coding across datasets.
  - Cross-dataset references (e.g., PlantationCode, GPS codes) require robust key management and linkage documentation.

- Data quality and gaps
  - Some NA values due to non-applicability or non-recovery (e.g., trap not recovered; self-reported data with possible inaccuracies).
  - Self-reported social data may require validation or caveats in analyses.

- Data update and lifecycle
  - Datasets reflect field campaigns (Dec 2021–Feb 2022 for environmental mapping; May 2022–Jul 2022 for temperature/biological data); coordinate any future updates with Cambridge repository practices.
  - Document any reprocessing steps or corrections to preserve data lineage.

- Reuse and governance
  - Clear dataset descriptions and variable dictionaries support reuse for agronomic, ecological, and governance-focused inquiries.
  - Respect for collaboration context (WAGS-BIO, WAGS, Independent) when interpreting management practices and farmer responses.

## Endnotes and caveats

- Some datasets rely on self-reported information; acknowledged potential inaccuracies.
- One sticky trap site data missing (NA for that location) due to non-recovery.
- Data are anchored to a specific geographic and organizational context (Perak, Malaysia; Wild Asia partnerships); consider contextual factors when generalizing findings.