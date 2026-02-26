# Environmental_Selangor_perimeter_centre.csv

- Purpose and scope
  - Data collected from five spatially reproducible transects within each study plantation in Banting, Peninsular Malaysia.
  - Captures environmental variables, understory vegetation, and oil palms.
  - Collected on the initial site visit.

- Key perimeter-level variables
  - Plot and plantation identifiers: PlantationCode, PlotWidth, PlotLength, TotalNumberOfPalms, ModalPalmAge.
  - Plantation characteristics: PlantationType (Immature Poly, Immature Mono, Mature Mono), PlantationZone (Central, PSide1–PSide4), Neighbouring land-use percentages (e.g., NeighbouringOPMono, NeighbouringOPPoly, NeighbouringHousing, NeighbouringRoad, NeighbouringUnusedLand, NeighbouringGrassland, NeighbouringNonOPCrop, NeighbouringOtherSum), and NeighbouringHabitatTypesNotes.
  - Weather, date, and time: WeatherDay1, DateDay1, SurveyStartTime, SurveyFinishTime.
  - Location and spatial data: GPSCode (central transect mid-point or plantation corners for PSides).
  - Plantation size and crop cover: TotalOtherCropCover, OtherCropBambooCover, OtherCropBananaCover, OtherCropCassavaCover, OtherCropCoconutCover, OtherCropGalangalCover, OtherCropYamCover, OtherCropJackfruitCover, OtherCropPineappleCover, OtherCropTorchGingerCover.
  - Surrounding land-use context: Distinct percentages for various land-use categories around the perimeter.
  - Planting density and structure: PalmsPerHectare, Height/age metrics (ModalPalmAge, TotalNumberOfPalms).

- Environmental and habitat indicators
  - Understory and habitat context: Data fields describing surrounding habitat types, extent of non-oil palm crops, and notes on neighbouring habitat.

- Data quality and formatting notes
  - Several fields include free text, long field names, and some typographical inconsistencies (e.g., date formats, unit descriptors).
  - Metadata expectations imply data cleaning, transformation, and verification against originators when used for monitoring.

- Relevance for monitoring
  - Provides baseline environmental health indicators at plantation perimeters, useful for assessing edge effects, habitat context, and landscape-level pressures on oil palm systems.
  - Supports analyses of how neighbouring land use and plantation characteristics relate to environment and biodiversity at the plot level.

---

# Environmental_Selangor_SamplePoints.csv

- Purpose and scope
  - Data collected at four spatially reproducible sample points within each study plantation in Banting, collected on the second visit (48 hours after initial visit).
  - Includes environmental variables, understory vegetation, and oil palms.

- Key sample-point variables
  - Core identifiers: PlantationCode, SamplePoint.
  - Weather and timing: WeatherDay2, DateDay2, SurveyStartTime.
  - Environmental measurements: SoilMoisture, SoilPH (noted as "Soil PH" in several fields), Light.
  - Canopy and light context: CanopyOpennessN, CanopyOpennessS, CanopyOpennessE, CanopyOpennessW (measured with a spherical densiometer; openness out of 96 dots).
  - Vegetation structure and cover: VegetationCoverBare, VegetationCoverPalm, VegetationCoverOtherCrop, VegetationCoverLeafLitter, VegetationCoverCutFrond, VegetationCoverFern, VegetationCoverOtherVeg, VegetationCoverOther.
  - Species and habitat: DominantCoverSpecies, Epiphyte metrics (TotalEpiphyteCover, TotalEpiphyteRichness, EpiphyteSpecies), PalmAge, PalmHeight, DistanceFromNearestPalm, TotalEpiphyteRichness, PalmHerbivoryScore, PalmFungalScore, PalmRhinoBeetleScore, Notes.
  - Sub-point specifics: Height measurements (VegetationHeight1-3), AverageVegetationHeight, Epiphyte-related lists, herbivory/fungal scores, and free-text Notes.

- Biodiversity and health indicators
  - Epiphyte communities on nearest palm; herbivory, fungal damage, and Rhino Beetle scores as indicators of palm health and pest/disease pressure.
  - Vegetation structure and microhabitat data (cover percentages, height metrics).

- Data quality and formatting notes
  - Some fields have descriptive text embedded (e.g., "Soil PH reading at sample point" and similar), with several NA placeholders.
  - Wide variety of units and data types (numeric, integer, character, free text).

- Relevance for monitoring
  - Enables fine-scale environmental health assessment around palms, including canopy structure, light environment, soil moisture, and understory vegetation.
  - Supports linkage of microhabitat conditions with palm health indicators and potential pest/disease pressures.
  - Facilitates temporal comparison between first and second visit measurements.

---

# Social_Selangor.csv

- Purpose and scope
  - The same survey instrument was used for three locations: SMARTRI (Riau, Indonesia), Wild Asia (Perak, Malaysia), and Banting (Malaysia).
  - Captures plantation characteristics, management inputs, and socio-demographic factors of smallholder oil palm plantations, including managers’ attitudes toward nature and management motivations.

- Plantation and management characteristics
  - Plantation identifiers and area: PlantationCode, PlantationArea, TotalNoPlantationsOwned, TotalPlantationAreaOwned, NoPalms, PalmsPerHectare.
  - Management and ownership: LandownerStatus, YearsInManagement, YearsOnLand, PreOPLandUse, RecentLandConversion, ReasonForConversion, CommentsOnFarming, WhyOP, DefinitionOfNature.
  - Intercropping and crop types: Intercropping, CropTypes, MostProfitableCrop, IncomeOtherCrop, TimeCommitmentOP.
  - Inputs and costs: UseOfHerbicide, HerbicideType, HerbicideApplicationsAnnual, HerbicideCostAnnual, HerbicideCostPerHAAnnual, HerbicideLitresAnnual, HerbicideLitresPerHAAnnual, FertilizerUse, FertilizerType, FertilizerApplicationsAnnual, FertilizerCostAnnual, FertilizerCostPerHAAnnual, FertilizerAmountAnnual, FertilizerAmountPerHAAnnual, OrganicManureUse, OrganicManureUse, Intercropping.

- Socio-demographic and economics
  - Respondent demographics: FarmerAge, MaritalStatus, HouseholdSize, Nationality, Ethnicity, Birthplace, YearsInLocation, Gender.
  - Education and employment: FurthestEducation, OtherEmployment, FormOfEmployment.
  - Income and financials: PercentageIncomeFromAgriculture, TotalMonthlyIncome, OPMonthlyIncome.
  - Attitudes, motivations, and policy-relevant perceptions: AgriculturalPreference, TimeCommitment, Opinions on soil and nature definitions, and Ranking of the value nature provides (economic, food, wildlife, beauty, culture, health, none).

- Attitudes and decision-making
  - Management influence and decision drivers: ManagementInfluenceRank_Neighbours, ManagementInfluenceRank_Scientific, ManagementInfluenceRank_Cost, ManagementInfluenceRank_Effort, ManagementInfluenceRank_Consistancy, ManagementInfluenceRank_Yields.

- Harvests, markets, and non-oil palm crops
  - Harvest frequency and yield economics: NoOPHarvestsMonthly, AmountOPYieldMonthly, AmountOPYieldPerHAMonthly, PriceOPYieldMonthly, PriceOPYieldPerHAMonthly, OPBuyer.
  - Non-oil palm crops: NoNonOPHarvestsMonthly, NonOPBuyer, OtherComments.

- Wildlife and natural context
  - Wildlife presence and perceptions: WildlifePresence, AnimalsSeenDaily, UnknownAnimalTypes, OtherAnimalsSeen, FavouriteAnimal, SecondFavouriteAnimal, LeastFavouriteAnimal, SecondLeastFavouriteAnimal, ReasonFavouriteAnimal, ReasonSecondFavouriteAnimal, ReasonLeastFavouriteAnimal, ReasonSecondLeastFavouriteAnimal, AnimalPreventionMethod.

- Data quality and formatting notes
  - Substantial breadth with many open-ended questions and some NA fields; cross-site comparability requires careful harmonization.
  - Some fields include multiple languages or site-specific categorizations (e.g., MM, MM, IP designations for Banting).

- Relevance for monitoring and policy
  - Enables evaluation of management practices, economic viability, and social drivers behind plantation decisions.
  - Supports analysis of how socio-economic factors, education, land ownership, and intercropping relate to environmental outcomes and biodiversity on oil palm plantations.
  - Provides insight into attitudes toward nature and perceptions of ecosystem services, useful for policy framing and stakeholder engagement.

---

# Integrated monitoring and policy implications

- What these datasets collectively offer for environmental health monitoring
  - Comprehensive, multi-layered view: perimeter environmental context, microhabitat conditions at sample points, and socio-economic/managerial drivers affecting management and landscape outcomes.
  - Enables linking ecological indicators (canopy openness, soil moisture, understory vegetation, epiphyte richness, pest/disease indicators) with plantation practices (herbicide/fertilizer use, intercropping, organic amendments) and socio-economic factors (income, land ownership, management motivations).

- Data management and governance considerations (aligned with monitoring framework aims)
  - Data provenance and metadata quality: complex, heterogeneous fields; need rigorous metadata documentation to support reuse and cross-site comparability.
  - Data sharing and openness: some datasets include sensitive socio-economic information; plan for appropriate data governance and access controls while supporting transparency where appropriate.
  - Data standardization and transformation: harmonize units, field naming, and categorical codes across sites (Indonesia, Malaysia) to enable robust cross-location monitoring and policy evaluation.
  - Timeliness and updating: temporal components (initial vs second visit) highlight the value of repeated measures for monitoring change; ensure processes exist to update datasets and maintain versioning.
  - Stakeholder engagement: the breadth of variables facilitates stakeholder-informed reporting (government bodies, environmental agencies, smallholders), but requires clear communication of complex results.

- Potential applications for policy and decision-making
  - Evaluate edge effects and landscape-level environmental health in oil palm-dominated regions.
  - Assess effectiveness of management interventions (intercropping, herbicide/fertilizer usage, organic amendments) on environmental indicators and palm health.
  - Understand socio-economic drivers of land-use change, management intensity, and attitudes toward nature to inform policy design, farmer support programs, and conservation planning.
  - Support cross-site comparisons to identify best practices and scale successful approaches across locations.