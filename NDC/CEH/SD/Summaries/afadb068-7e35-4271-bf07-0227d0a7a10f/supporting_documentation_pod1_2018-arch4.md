# Ozone flux dataset from EMEP-WRF model for grasslands in the UK and USA (2018)

- Overview
  - Purpose: provides accumulated ozone flux data (POD1 IAM) for semi-natural grasslands during the growing season, for the UK and USA in 2018.
  - Modeling chain:
    - EMEP-WRF global model (v4.45) driving emissions from IIASA GAINS v6a for 2015 and using meteorology from WRF (v4.2.2) forced by GFS-FNL data.
    - DO3SE stomatal flux model calculates ozone uptake (POD) with inputs: hourly ozone concentration, temperature, vapour pressure deficit, irradiance, and soil moisture; parameterisations by vegetation type (e.g., crops, trees, grasslands) including g max.
    - Output POD values are reported as POD1 IAM or POD1 SPEC; POD1 IAM used for the current dataset.
  - Spatial and temporal scope:
    - Global grid at 1° x 1° resolution; 21 vertical layers in the model.
    - Time window: 90-day grassland growing season (mid-April to mid-July) in 2018, with the season start/end chosen to maximize flux locally.
  - Data products:
    - Daily POD1 IAM values summed over the defined 90-day grassland season for each grid cell in the UK and USA (2018).
    - Output units: mmol m^-2; coordinate system: WGS84 (decimal degrees).
    - Data format: shapefile with 5 attributes per grid cell: FID, Lon, Lat, NAME (USA or UK), POD1 (mmol m^-2).

- Data content and structure
  - Shapefile specification:
    - 1° x 1° gridded data.
    - Attributes:
      - FID: unique grid cell identifier.
      - Lon: longitude of grid cell centre (decimal degrees).
      - Lat: latitude of grid cell centre (decimal degrees).
      - NAME: country designation (USA or UK).
      - POD1: accumulated POD1 IAM over the grassland season (mmol m^-2) for 2018.
  - Coordinate system and units:
    - Geographic Coordinate System: WGS 1984.
    - POD1 units: mmol m^-2.

- Methodology and parameterisation
  - Seasonal and data aggregation:
    - POD1 IAM values are summed over the 90-day grassland growing season (as defined per local guidance) within 2018 for each grid cell.
  - DO3SE model parameterisation:
    - Uses vegetation-type specific parameters (e.g., canopy conductance) including VPD, irradiance, soil moisture, and phenology considerations.
    - References for parameter values and methodology are provided (CLRTAP Mapping Manual, 2017), with specific parameterisation values listed in Table 1 of the document.
  - Background processing:
    - Ozone flux data are intended to support assessments of crop yield, tree biomass, and flower number via CLRTAP response functions.

- Quality control and validation
  - Model validation:
    - EMEP model outputs were compared with observations from the Global Atmosphere Watch (GAW) network to assess spatial and temporal accuracy, particularly during peak ozone periods.
    - Overall, the model captured seasonal patterns and regional variations, including higher ozone episodes.
  - Proxy validation for stomatal uptake:
    - A strong correlation (r^2 ≈ 0.63) was found between a proxy for growing-season stomatal conductance (POD3 IAM divided by M7 ozone) and ET/PET-based metrics, supporting the model’s ability to estimate stomatal uptake.

- Use cases and applicability
  - Potential analyses:
    - Estimating impacts on crop yield, tree biomass, and flowering via CLRTAP response functions (e.g., grassland responses to POD1 IAM).
    - Informing regional assessments of ozone-related vegetation stress and informing policy and management decisions.
  - Background and references:
    - CLRTAP Mapping Manual (2017) for dose-response relationships and critical levels.
    - Related studies on ozone impacts and model validation (e.g., Mills et al., 2018; Hayes et al., 2021; Emberson et al., 2000; Simpson et al., 2012; Vieno et al., 2016).

- Practical considerations for data leaders
  - Data provenance and governance:
    - Clear lineage: EMEP-WRF model chain, DO3SE parameterisations, and 2018 UK/USA focus; 1° x 1° grid with standardized units and CRS (WGS84).
  - Metadata and discoverability:
    - Shapefile with explicit fields and unit definitions; documented seasonal aggregation method and parameterisation references to aid reproducibility.
  - Timeframe and scope:
    - Limited to 2018 and to grassland-dominated vegetation in the UK and USA; may require re-running for other years or regions to support broader analyses.
  - Limitations and caveats:
    - Parameter values in Table 1 are model-specific and may require local calibration for other vegetation types or regions.
    - The 90-day season is selected to maximize flux in each grid cell, which may affect comparability across areas with different growth patterns.

- Useful background and references
  - EMEP and modeling framework: EMEP MSC-W, WRF-based ozone flux modeling framework.
  - Data sources and tools: CLRTAP Mapping Manual (2017); GAW observational validation (Mills et al., 2018); DO3SE ozone flux modeling (Emberson et al., 2000).
  - Related literature: Mills et al. (2018); Hayes et al. (2021); Simpson et al. (2012); Vieno et al. (2016).

- Access and further information
  - Useful websites:
    - EMEP: https://www.emep.int/
    - ICP Vegetation: https://icpvegetation.ceh.ac.uk/
  - Application context:
    - Ozone flux data can be linked to vegetation impact assessments using CLRTAP modelling and mapping guidelines.