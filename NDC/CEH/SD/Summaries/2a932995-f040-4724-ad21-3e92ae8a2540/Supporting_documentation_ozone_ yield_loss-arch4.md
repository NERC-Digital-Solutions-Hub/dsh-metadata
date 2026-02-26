# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2

- Objective: Provide modelled estimates of annual average yield loss due to ozone for four global staple crops (maize, rice, soybean, wheat) for 2010–2012, using a standardized approach that combines ozone flux data with crop-specific dose–response relationships.

- Data inputs and grid structure:
  - Spatial framework: 1° by 1° grid cells; each cell classified as irrigated or non-irrigated and assigned to a hemisphere (Northern/Southern) and a climate zone (ESDAC/JRC layer).
  - Crop production and filtering: FAO Global Agro-Ecological Zones (GAEZ) data (2000) used to estimate total production per grid cell; 2010–2012 average production derived via a conversion factor from national production data; only cells with >500 tonnes are included in mapping.
  - Growing period: For each climate-hemisphere combination, a 90-day main growing period is defined per crop, with specific start/end days provided for each climate zone and hemisphere.

- Yield loss calculation methodology:
  - Wheat (reference crop):
    - Ozone uptake metric: POD3IAM (phytotoxic ozone dose above 3 nmol m-2 s-1) computed from the EMEP MSC-W model (v4.16) using hourly ozone concentration, temperature, VPD, irradiance, and soil moisture.
    - Baseline subtraction: 0.1 mmol/m2 subtracted to represent pre-industrial ozone levels.
    - Dose–response: yield loss = (POD3IAM − 0.1) × 0.64.
  - Other crops (maize, rice, soybean):
    - Approach: compute wheat-based yield loss, then adjust by crop-specific relative ozone sensitivity using M7 (7-hour mean ozone) response functions.
    - Relative sensitivity: crop-specific M7 response functions (slope-based) relative to wheat are used. The functions are:
      - Soybean: RY = −0.0050x + 1.001
      - Wheat: RY = −0.0048x + 0.960
      - Rice: RY = −0.0021x + 0.987
      - Maize: RY = −0.0031x + 1.030
    - Final crop yield loss per grid cell = wheat-based yield loss × crop’s relative ozone sensitivity (as defined by the M7 functions).
  - Outputs: Four yield-loss rasters/files, one per crop, stored as GIS shapefiles with 1°×1° grid cells.

- Data products and structure:
  - Outputs: 4 GIS shapefiles (one per crop) containing gridded yield loss data.
  - Attributes in each shapefile (per grid cell):
    - ID: Unique grid cell identifier
    - Zone: Climate zone
    - Long_Lat: Center coordinates of the grid cell
    - Hemisphere: Northern, Southern, or Far South (for Cool temperate)
    - Yloss: Annual average percentage yield loss due to ozone (2010–2012)

- Quality control and validation:
  - Model validation for the EMEP model against Global Atmosphere Watch (GAW) observations shows good alignment of daily maximum ozone (Dmax) and 90-day mean M7 values (r2 between 0.88 and 0.93) across sites.
  - Additional checks include correlation between modeled POD3IAM-derived estimates (normalized by M7) and satellite-derived Actual Evapotranspiration (AET)/Potential Evapotranspiration (PET) as a proxy for stomatal conductance (r2 = 0.63).
  - The approach is innovative in using ozone flux (POD3IAM) rather than concentration alone to assess global crop yield impacts. Caveats noted include:
    - Lack of crop-specific flux–response data for maize, rice, and soybean; the method uses wheat flux data scaled by crop-specific M7 sensitivities.
    - Greater uncertainty for maize due to limited variety data.
    - In some climates, multiple cropping seasons exist; the study selects only the most important growing period per climate.

- Data provenance and references:
  - EMEP/MSC-W chemical transport model (v4.16) and associated documentation.
  - CLRTAP dose–response guidance (2017).
  - FAO GAEZ dataset for crop production data.
  - European Soil Data Centre (ESDAC) climatic zone layer (JRC).
  - Key related studies: Mills et al. (2018a, 2018b) on ozone yield impacts and model validation.

- Usage notes for data leaders and data-driven teams:
  - Clear, reproducible workflow tying ozone flux (POD3IAM) to crop yield loss through crop-specific sensitivity scaling.
  - Structured data outputs facilitate cross-crop comparisons and integration with other data systems (e.g., policy analyses, risk assessments).
  - Documented quality checks and limitations support cautious interpretation, especially where species-specific flux data are lacking or where multi-season cropping exists.