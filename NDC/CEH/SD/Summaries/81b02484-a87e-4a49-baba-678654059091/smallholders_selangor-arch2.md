# Environmental_Selangor_perimeter_centre.csv

- The dataset comprises five spatially reproducible transects within each study plantation in Banting, Peninsular Malaysia, collecting data on environmental variables, understory vegetation, and oil palms during the initial site visit.
- Key data categories and example fields:
  - Plantation metadata: Plot/PlantationCode, Description, PlantationType (Immature Poly, Immature Mono, Mature Mono), PlotWidth, PlotLength, TotalNumberOfPalms, ModalPalmAge.
  - Site and weather context: WeatherDay1, DateDay1, SurveyStartTime, SurveyFinishTime.
  - Spatial and management context: PlantationZone (Central, PSide1–PSide4), GPSCode.
  - Vegetation and land use: TotalOtherCropCover, OtherCropCover subfields (Banana, Cassava, Coconut, Galangal, Yam, Jackfruit, Pineapple, Torch Ginger), Neighbouring OP (Mono/Poly), NeighbouringHabitatTypesNotes.
  - Environmental and habitat indicators: Soil-type notes, Canopy-related indicators, Wildlife-related notes (implicit in surrounding variables), various neighbouring land-use metrics.
  - Data transformation and storage: Dataset designed to be verified/QA’ed, cleaned, transformed, and stored/uploaded to appropriate portals.

- Overall purpose: To standardise and document environmental monitoring data from palm plantations for assessing environmental health and policy performance over time, enabling cross-site comparison and longitudinal analyses.

# Environmental_Selangor_SamplePoints.csv

- Four spatially reproducible sample points per plantation collected on the second visit to the site (48 hours after the initial visit), capturing a more detailed snapshot of environmental conditions around palms.
- Key data categories and example fields:
  - Plantation context: PlantationCode, Description (Plot ID), PlantationType, WeatherDay2, DateDay2.
  - Sampling design: SamplePoint (1–4), GPSCode.
  - Physical and soil measurements: SoilMoisture, Light, CanopyOpennessN/S/E/W (densiometer-based), VegetationCoverBare, VegetationCoverPalm, VegetationCoverOtherCrop, VegetationCoverLeafLitter, VegetationCoverCutFrond, VegetationCoverFern, VegetationCoverOtherVeg, DominantCoverSpecies, VegetationHeight1–3, AverageVegetationHeight, DistanceFromNearestPalm, PalmAge, PalmHeight, TotalEpiphyteCover, TotalEpiphyteRichness, EpiphyteSpecies, PalmHerbivoryScore, PalmFungalScore, PalmRhinoBeetleScore, Notes.
  - Additional qualitative data: Canopy/opening notes, epiphyte and herbivory context, free-text Notes.

- Overall purpose: To provide a detailed, point-level environmental and biophysical profile around selected sample points within each plantation, enriching the environmental health assessment with microhabitat information.

# Social_Selangor.csv

- A social-ecosystem survey completed using the same instrument across three locations: Banting (Banting, Malaysia); SMARTRI (Riau, Indonesia); Wild Asia (Perak, Malaysia). The Banting sites are designated by age and intercropping status (MM = mature monoculture, IP/IM = immature polyculture/immature monoculture).
- Key data categories and example fields:
  - Plantation and management context: PlantationCode, Description, PlantationArea, TotalNoPlantationsOwned, TotalPlantationAreaOwned, NoPalms, PalmsPerHectare.
  - Respondent demographics: FarmerAge, MaritalStatus, HouseholdSize, Nationality, Ethnicity, Birthplace, YearsInLocation, Gender.
  - Education and employment: FurthestEducation, OtherEmployment, FormOfEmployment, PercentageIncomeFromAgriculture, TotalMonthlyIncome, AgriculturalPreference.
  - Farm ownership and management: LandownerStatus, YearsInManagement, ManagementSalary, ManagementMotivation, YearsOnLand, YearsLandOP, PreOPLandUse, RecentLandConversion, ReasonForConversion, CommentsOnFarming, WhyOP, DefinitionOfNature.
  - Nature values and decision drivers: RankedImportanceNature_Economic, RankedImportanceNature_Food, RankedImportanceNature_Wildlife, RankedImportanceNature_Beauty, RankedImportantanceNature_Culture, RankedImportanceNature_Health, RankedImportanceNature_None, HoursFarmingDaily, HoursFarmingWeekly, HoursFarmingWeeklyPerHA, SoilType, OpinionOnSoil.
  - Agricultural practices and inputs: UseOfHerbicide, HerbicideType, HerbicideApplicationsAnnual, HerbicideCostAnnual, HerbicideCostPerHAAnnual, HerbicideLitresAnnual, HerbicideLitresPerHAAnnual, FertilizerUse, FertilizerType, FertilizerCostAnnual, FertilizerCostPerHAAnnual, FertilizerAmountAnnual, FertilizerAmountPerHAAnnual, OrganicManureUse, Intercropping, CropTypes, MostProfitableCrop, IncomeOtherCrop, TimeCommitmentOP, MotivationIntercropping, MotivationCropTypes, Intercropping-related motivations.
  - Interactions with wildlife and landscape context: WildlifePresence, AnimalsSeenDaily, UnknownAnimalTypes, OtherAnimalsSeen, FavouriteAnimal, SecondFavouriteAnimal, LeastFavouriteAnimal, SecondLeastFavouriteAnimal, ReasonFavouriteAnimal, ReasonSecondFavouriteAnimal, ReasonLeastFavouriteAnimal, ReasonSecondLeastFavouriteAnimal, AnimalPreventionMethod.
  - Social influence and decision drivers: ManagementInfluenceRank_Neighbours, ManagementInfluenceRank_Scientific, ManagementInfluenceRank_Cost, ManagementInfluenceRank_Effort, ManagementInfluenceRank_Consistency, ManagementInfluenceRank_Yields, plus related monthly yield, price, and buyer information for oil palm (OP) and non-OP crops.
  - Economic performance and sales: NoOPHarvestsMonthly, AmountOPYieldMonthly, AmountOPYieldPerHAMonthly, PriceOPYieldMonthly, PriceOPYieldPerHAMonthly, OPBuyer, NoNonOPHarvestsMonthly, NonOPBuyer.
  - Open commentary: OtherComments.

- Cross-location note: The same survey instrument was used across three locations (SMARTRI, Wild Asia, Banting), enabling cross-site comparisons of plantation characteristics, management inputs, socio-demographics, attitudes toward nature, and management motivations.

# How this aligns with the Analysts Monitoring the Environment archetype

- Data products and outputs:
  - Environmental metrics (land-use composition, understory and canopy structure, soil/leaf litter dynamics, epiphyte communities, herbivory/fungal pressures) alongside plantation metadata to assess environmental health and habitat condition.
  - Social and management context metrics (farmer demographics, land ownership, income, intercropping, herbicide/fertilizer usage, motivations) to interpret policy relevance and management decisions.

- Data processes and quality:
  - Data are collected in a standardised, repeatable design (transects, sample points) with clear field definitions; data are intended to be verified, quality-assured, cleaned, and transformed before publication or portal upload.
  - Outputs are designed to be presented in clear formats (reports, maps, charts), supporting monitoring and policy evaluation over time.

- Data integration and accessibility:
  - The inclusion of both environmental measurements and social/management data supports synthesis across ecological health indicators and human factors.
  - Acknowledged challenges include increasing the value of datasets through data fusion (linking with other data sources) and enabling access to underlying data used to generate final outputs, aligning with the aim to improve data interoperability and reuse.

- Geographic and temporal scope:
  - Study focused on Banting, Peninsular Malaysia, with cross-location social data spanning Indonesia and Malaysia, enabling regional comparisons and trend analysis over time as monitoring continues.