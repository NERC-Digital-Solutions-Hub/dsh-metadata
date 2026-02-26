# Ozone flux POD 1 IAM dataset for grasslands in the UK and USA, 2018

- Purpose and context
  - Provides modeled ozone flux data (POD 1 IAM) for semi-natural grasslands, enabling assessment of ozone uptake by vegetation and potential impacts on crops and plant communities.
  - Derived from the EMEP-WRF modelling chain to support exposure and risk assessment using CLRTAP methodologies.

- Data lineage and production
  - Model framework: EMEP-WRF global model, version 4.45, driven by hourly 3D meteorology from WRF (2018) and nudged with GFS-FNL data; emissions from IIASA GAINS v6a.
  - Core ozone uptake calculation: DO 3 SE stomatal flux model with inputs including hourly ozone, temperature, vapour pressure deficit, irradiance, and soil moisture; parameterised by vegetation type (e.g., crops, trees, grasslands).
  - Output metric: POD 1 IAM (Integrated Aerosol/Atmosphere Model) flux for grasslands, with units of mmol m^-2.
  - Spatial and temporal scope: global grid at 1° x 1° resolution; daily POD 1 IAM values aggregated over the grassland growing season. For the current dataset, daily POD 1 IAM values were summed for the grassland growing season in 2018 for the UK and USA (mid-April to mid-July focus in description; overall season guidance follows April–September with season start/end chosen to maximize flux).

- Dataset content and structure
  - Spatial coverage: gridded 1° x 1° cells; coordinate system WGS 84.
  - Primary output: POD1 IAM per grid cell for grassland growing season in 2018 (UK and USA).
  - Shapefile attributes (5 columns):
    - FID: Unique grid cell identifier.
    - Lon: Longitude of grid cell center (decimal degrees).
    - Lat: Latitude of grid cell center (decimal degrees).
    - NAME: Country (USA or UK).
    - POD1: Accumulated POD 1 IAM for grassland growing season (in mmol m^-2).
  - Data usage note: POD 1 IAM values can be linked to crop yield and vegetation response through CLRTAP-derived dose–response relationships (e.g., Flower number, biomass) and ozone critical level assessments.

- Quality assurance and validation
  - Model validation against GAW network observations shows the EMEP model captures spatial and temporal ozone variations, including peak episodes.
  - Stomatal uptake proxy validation: strong correlation (r^2 ≈ 0.63) between AET/PET and model-estimated POD 3 IAM divided by 7-h ozone (M7), indicating reasonable estimation of stomatal uptake.
  - Documentation and figures available in Mills et al. (2018) and supplementary information; additional references provide background on model description and parameterisations.

- Parameterisation and time window guidance
  - Parameter sets follow CLRTAP Mapping Manual guidance for semi-natural vegetation POD IAM calculations (Table 1 in the source), including canopy length, stomatal conductance parameters, and phenology considerations.
  - Time window guidance: select a 3-month accumulation period within 1 April–30 September that yields the highest flux or best represents the local growing season; for the dataset, a grassland growing-season window was used (mid-April to mid-July) for 2018 UK/USA.

- Potential uses and relevance for data users
  - Baseline exposure assessment for ozone effects on grasslands and semi-natural vegetation.
  - Calculation of yield/biomass/flower-number impacts using CLRTAP response functions and the POD 1 IAM metric.
  - Integration into larger exposure–impact assessments and policy-relevant risk analyses (e.g., ozone critical levels for grasslands).

- Access to background and related resources
  - CLRTAP Mapping Manual and related vegetation ozone impact references for dose–response functions.
  - Model and methodological references: EMEP MSC-W model descriptions, WRF-driven emissions, and associated validation studies.
  - Useful links:
    - EMEP: https://www.emep.int/
    - ICP Vegetation: https://icpvegetation.ceh.ac.uk/

- Summary of key takeaways for data work
  - This dataset provides a standardized, model-derived measure (POD 1 IAM) of ozone flux to grasslands at 1° resolution for UK and USA in 2018.
  - It is suited for downstream analyses linking ozone flux to vegetation responses, with clear QA/validation context and established regulatory-methodology alignment (CLRTAP).
  - The data are organized as a shapefile with a compact attribute table, facilitating integration into GIS and data products for end users.