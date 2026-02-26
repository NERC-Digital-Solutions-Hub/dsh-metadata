# Oil palm smallholder biodiversity and environmental data from Perak, Malaysia

- A multi-component dataset collected across 24 oil palm smallholders in Perak, Malaysia, primarily during 2021–2022, to examine how plantation management practices influence soil conditions, microclimate, arthropod communities, vegetation structure, and socio-economic factors.
- The dataset captures four main data streams per site (T1–T4 sampling points) and includes both ecological measurements and farmer surveys to inform monitoring and policy decisions under sustainability frameworks (e.g., RSPO/MSPO).

## Data streams and key measures

- Soil temperature data (datalogger measurements)
  - 24 farms, 4 locations per farm (96 total), 5 cm soil depth, 24–26 hourly temperature readings after set
  - Variables include: PlantationCode, SamplePoint (T1–T4), TempHr1–TempHr26 (°C)
  - Purpose: assess effects of management on soil thermal regimes under field conditions

- Insect observations (butterflies, spiders, assassin bugs)
  - Standard 100 m transects across plantation centers; 5 m × 5 m observation plots
  - Observations include: SpeciesID, Date, TimeSeenCaught, WeatherCond, AirTemp, Microhabitat
  - Behavioral categories: Flying, Resting, Sunning, Interacting, Nectaring
  - Species identification aided by field guides; field notes and photos for verification
  - Purpose: link insect activity/diversity to habitat characteristics and management

- Biodiversity sampling with sticky traps and predation cards
  - 96 sampling points; 24-hour trap deployment; 30 cm × 30 cm sticky traps; 6 dead mealworms on bait cards to assess predation
  - Data include: StickyTrapSetupTime, StickyTrapCollectionTime, DataLoggerSetup/Collection times, bait preparation and mealworm counts, Visual notes
  - Insect identifications from trap images to order level; counts by taxa (e.g., Ants, Termites, Coleoptera, etc.)
  - Purpose: quantify arthropod abundance and predation pressure under different management contexts

- Vegetation, microclimate, and soil condition data (environmental survey)
  - Data collected at 47 plantations; transects across central plots with 3 × 3 m quadrats
  - Measures cover (Crop, Bare Ground, Fern, Other Vegetation, Leaf Litter, Palm Fronds, etc.), vegetation height (SS1–SS3), canopy density (densiometer and visual), air temperature/humidity, palm metrics (age, height, epiphyte cover, herbivory, health)
  - Soil metrics: leaf litter depth, soil moisture, soil pH, A-horizon depth, soil sampling (wet/dry weights), VESS soil-structure scores
  - GPS coordinates for plantation center and sampling points; corner and side-length measurements across plantation boundaries
  - Vegetation and habitat context captured for each plantation side (SideA–SideL) and central plots
  - Purpose: characterize microsite conditions and potential habitat features influencing biodiversity and crop health

- Plantation survey and management data (social and managerial context)
  - 49 plantations (Perak; broader project includes additional sites in Indonesia and Malaysia)
  - Variables cover: plantation type and Wild Asia collaboration level (BIO, WAGS, Independent), plot identifiers, district, coordinates, plantation size, palm density, farmer demographics, land tenure, prior land use, management motivations, income, harvests, yields, prices, involvement of herbicides/fertilizers, intercropping, wildlife observations
  - Extensive socio-economic and cultural data, including ethical considerations and consent
  - Purpose: link governance, incentives, and socio-economic factors to environmental outcomes and management decisions

## Data quality, metadata, and governance

- Quality assurance
  - Field data quality checks and standardization performed by field teams and the University of Cambridge; cross-verification of timing and realistic values
  - Taxonomic identifications and image-based verifications used where appropriate
- Metadata and data dictionaries
  - Each dataset is accompanied by comprehensive variable descriptions (descriptions, units, data types)
  - Consistent field naming across modules to support cross-dataset integration
- Data sharing and governance considerations
  - Authors note that publicly sharing underlying datasets can be a barrier; governance processes and data standards are important to ensure openness, provenance, and up-to-date datasets
  - Data represent a mix of ecological measurements and sensitive socio-economic information; sharing policies should balance openness with privacy and consent
- Temporal and spatial scope
  - Ecological datasets primarily collected May 2022–July 2022 (soil/insects) and December 2021–February 2022 (environmental survey) with social data collected through 2022
  - Geographic scope centers on Perak, Malaysia, with expansion to select Indonesian and other Malaysian sites within the broader project

## Relevance for monitoring frameworks and policy decisions

- Integrated metrics across soil, microclimate, invertebrate communities, vegetation structure, and farmer socio-economics enable evaluation of management interventions (e.g., Wild Asia schemes, RSPO/MSPO compliance) on environmental health and biodiversity
- Data can inform monitoring indicators such as:
  - Soil temperature regimes and depth profiles under different cultivation practices
  - Invertebrate biodiversity and predation pressure as proxies for ecosystem services
  - Habitat complexity (vegetation cover, canopy openness, leaf litter, soil structure) and its relation to pest/disease dynamics
  - Input use (herbicides, fertilizers), costs, yields, and price signals linked to biodiversity and habitat outcomes
  - Farmer attitudes, motivations, and neighbor influences as drivers of sustainable practices
- Potential policy applications
  - Assess effectiveness of sustainability certifications and private-sector collaborations on on-farm environmental health
  - Guide development of monitoring frameworks that couple ecological indicators with socio-economic governance to promote sustainable oil palm production
  - Inform data governance practices to enhance data sharing, metadata quality, and cross-site comparability

## Key considerations for future monitoring framework work

- Data gaps and access
  - Occurrence of missing data (NA) and the need for robust metadata to assess data quality and completeness
- Silos and interoperability
  - Integration across ecological and social datasets requires standardized variable definitions and harmonized data schemas
- Timeliness and updates
  - Regular updates and versioning are needed to keep datasets current and policy-relevant
- Communication of complex findings
  - Clear visualization and reporting of multi-metric indicators are essential to inform policymakers and stakeholders
- Data governance and openness
  - Establish clear data-sharing agreements, provenance tracking, and responsible handling of sensitive socio-economic information

- Overall, this collection provides a comprehensive, multi-dimensional framework for monitoring environmental health and biodiversity in oil palm landscapes, with direct relevance to policy evaluation, certification schemes, and sustainable management decisions.