# Environmental_Selangor_perimeter_centre.csv

- What it is: Data collected from five spatially reproducible transects within each study plantation in Banting, Peninsular Malaysia, capturing environmental variables, understory vegetation, and oil palms during the initial site visit.
- Coverage and structure:
  - Plantation-level metadata (Plot/PlantationCode, Description, Type, Zone such as Central or PSide1–4).
  - Spatial and geometric data (PlotWidth in metres, PlotLength in metres, GPSCode for transect center or corners).
  - Palm and plantation characteristics (TotalNumberOfPalms, ModalPalmAge, TotalOtherCropCover, various crop/land-use cover metrics, neighbouring land-use data for PSides).
  - Environmental and canopy context (WeatherDay1, DateDay1, Canopy openness metrics, VegetationCover metrics, DominantCoverSpecies, DistanceFromNearestPalm, PalmAge/PlamHeight, Epiphyte data, Herbivory and Fungal scores).
  - Biotic interactions and landscape context (NeighbouringOPMono/Poly, NeighbouringHousing, NeighbouringRoad, NeighbouringGrassland, etc.).
  - Notes on management and observations (Notes, various free-text fields).
- Data characteristics:
  - Variables with numeric, integer, character, and date types; many fields include explicit units (e.g., PlotWidth/PlotLength in metres, DistanceFromNearestPalm in feet, % cover for vegetation).
  - Some fields contain free-text descriptions (e.g., WeatherDay1) and require standardization for quantitative analyses.
- Spatial scale and scope: Five transects per plantation within Banting; zone designation across central and four perimeter sides.

# Environmental_Selangor_SamplePoints.csv

- What it is: Data collected at four spatially reproducible sample points within each study plantation in Banting, collected on the second visit (48 hours after the initial visit), including environmental measurements, understory vegetation, and palm-related data.
- Coverage and structure:
  - Plantation-level identifiers (Plot/PlantationCode, Description, PlantationType).
  - Temporal markers (DateDay2).
  - Sample metadata (SamplePoint 1–4, GPSCode per sample point).
  - Environmental measurements (SoilMoisture, SoilPH, Light, CanopyOpennessN/S/E/W).
  - Vegetation/surface cover (VegetationCoverBare, Palm, OtherCrop, LeafLitter, CutFrond, Fern, OtherVeg, Other).
  - Species and palm context (DominantCoverSpecies, PalmAge, PlamHeight).
  - Palm health and biota (TotalEpiphyteCover, TotalEpiphyteRichness, EpiphyteSpecies, PalmHerbivoryScore, PalmFungalScore, PalmRhinoBeetleScore).
  - Free-text notes for additional relevance (Notes).
- Data characteristics:
  - Mixed data types (numeric, integer, character, and some NA placeholders).
  - Units include centimetres for vegetation height, feet for distance, percentages for cover, kilograms for yield-related metrics, and degrees/indices for canopy openness.
- Spatial/temporal context: Second visit at fixed sample points within Banting plantations; designed to pair with initial transect data for fine-grained, point-level environmental context.

# Social_Selangor.csv

- What it is: A unified survey dataset used across three locations (SMARTRI in Riau, Indonesia; Wild Asia in Perak, Malaysia; Banting in Malaysia) to capture plantation characteristics, management inputs, and socio-demographic and attitudinal factors of smallholder oil palm plantations.
- Coverage and structure:
  - Plantation-level and owner/manager metadata (PlantationCode, Description, PlantationArea, TotalNoPlantationsOwned, NoPalms, PalmsPerHectare, etc.).
  - Socio-demographic factors (FarmerAge, MaritalStatus, HouseholdSize, Nationality, Ethnicity, Birthplace, YearsInLocation, Gender).
  - Economic indicators (TotalMonthlyIncome, OPMonthlyIncome, PercentageIncomeFromAgriculture, LandownerStatus, YearsInManagement, ManagementSalary).
  - Management and motivation factors (ManagementMotivation, YearsOnLand, YearsLandOP, PreOPLandUse, RecentLandConversion, ReasonForConversion, DefinitionOfNature, RankedImportanceNature_* items, HoursFarmingDaily/Weekly).
  - Agricultural practices and inputs (FertilizerUse, FertilizerType, FertilizerCostAnnual/PerHA, FertilizerAmountAnnual/PerHA, FertilizerApplicationAnnual, OrganicManureUse, Intercropping, CropTypes, MostProfitableCrop, IncomeOtherCrop, TimeCommitmentOP, UseOfHerbicide, HerbicideType, HerbicideApplicationsAnnual, HerbicideCostAnnual/PerHA, HerbicideLitresAnnual/PerHA, HerbicideLocation_*).
  - Vegetation and pest/animal context (WildlifePresence, AnimalsSeenDaily, Favorite/Least Favorite Animals, ManagementInfluenceRank_Neighbors/Scientific/Cost/Effort/Consistency/Yields, NoOPHarvestsMonthly, AmountOPYieldMonthly/PerHAMonthly, PriceOPYieldMonthly/PerHAMonthly, OPBuyer, NonOPBuyer, etc.).
  - Intercropping and crop diversification (Intercropping, CropTypes, MostProfitableCrop, MotivationIntercropping, MotivationCropTypes).
  - Miscellaneous and open-ended fields (CommentsOnFarming, DefinitionOfNature, OtherComments, Reasons for various attitudes).
- Cross-location design:
  - Data schema accommodates multiple sites with site-specific codes for plantation type and agricultural context.
  - Currency fields vary by site (Malaysian ringgit; Indonesian rupiah).
- Data characteristics:
  - Numerous categorical (Yes/No, Character) and numeric fields, with many open-ended or free-text components.
  - Large, multi-domain dataset linking economic, social, and management dimensions with plantation biology/environment data.

# Key takeaways for data-analysis workflows

- Central key linking variable: PlantationCode serves as the primary key to join environmental datasets (perimeter and sample points) with social/management data.
- Multi-scale integration: Combines landscape-level context (transects and perimeter zones), fine-scale micro-environment around sample points, and human factors (ownership, management incentives, demographics) for holistic analyses.
- Potential analyses to enable:
  - Relationships between canopy openness, understory vegetation, soil moisture, and palm health/yield indicators.
  - Influence of neighboring land use and landscape context on palm performance and pest/disease indicators.
  - Social-ecological models linking farmer characteristics, management inputs (fertilizer, herbicide, intercropping), and economic outcomes (yield, income, costs).
  - Cross-site comparisons to explore how different governance or land-use histories affect plantation outcomes.
- Data preparation notes:
  - Standardize date formats, units, and currency across datasets.
  - Harmonize categorical coding (e.g., PlantationType and Zone descriptors) and resolve free-text fields (WeatherDay, Notes) into structured variables where possible.
  - Handle missing values and NA codes consistently across datasets.
- Caveats and considerations:
  - Some fields use free text or contain inconsistencies in descriptions (e.g., ambiguous soil or weather fields) requiring cleaning or sensor-driven proxies.
  - The Social_Selangor.csv dataset spans multiple locations with site-specific economic contexts; ensure site-level controls when modeling cross-site data.
  - Data at plantation level may require aggregation or spatial weighting if local-scale analyses demand finer resolution.

# Temporal, spatial, and data-management considerations

- Temporal: Day 1 (initial visit) and Day 2 (second visit) data collection cycles; date fields follow year-month-day conventions in multiple formats.
- Spatial: Banting, Peninsular Malaysia as the primary study area with transects organized by PlantationZone (Central, PSide1–4) and GPS coordinates for transects and sample points.
- Provenance and accessibility: The datasets appear to be designed for integration and reuse in research or policy contexts; attention to metadata and dataset provenance (source, collection dates, units) will support reproducibility.
- Practical starting points for analysts:
  - Begin with a master plantation-level dataset merged on PlantationCode to align perimeter, sample-point environmental data with social/management variables.
  - Extract core variables for initial models: palm density (PalmsPerHectare), total palms, canopy openness, soil moisture/PH, vegetation cover metrics, herbivore/disease scores, fertilizer/herbicide inputs, intercropping presence, and key socio-economic factors (farmer age, income, management motivation).