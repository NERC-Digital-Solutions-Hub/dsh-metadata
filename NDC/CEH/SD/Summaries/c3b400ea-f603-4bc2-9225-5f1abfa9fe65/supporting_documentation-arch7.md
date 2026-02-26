# Supporting documentation for data: Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

- Purpose
  - Provides ensemble-derived statistics of topsoil organic carbon (SOC) for Great Britain (GB) at 1 km resolution.
  - Enables understanding of spatial agreement and variability across eight published SOC maps and supports use in GIS analyses and land-surface modelling.

- Data sources and harmonisation
  - Eight primary SOC maps (cover GB; top 15 cm, except LUCAS 20 cm and OCTOP 30 cm):
    - CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF (Countryside Survey-derived)
    - ISRIC-2017, ISRIC-2020 (SoilGrids)
    - LUCAS (Europe-wide survey)
    - OCTOP (Europe-wide)
  - Maps were harmonised to:
    - GB extent, 1 km grid resolution, CRS EPSG:27700 (OSGB)
    - Snapping/resampling used to align ISRIC, LUCAS, OCTOP to the GB 1 km OS grid
  - Depth and unit conversions
    - Depth handling for ISRIC maps to obtain 0–15 cm values using depth-specific rules
    - Unit conversions to g kg-1 where needed; corrections for values outside plausible ranges
  - Data cleaning
    - Negative SOC values in CSGB-AIC reset to no-data
    - Values exceeding ~55% SOC capped at 550 g kg-1
    - Cells with any map missing are set to no-data for ensemble statistics

- Processing, metrics, and interpretation
  - For each 1 km grid cell with complete data from all eight maps (n = 208,752):
    - Band 1: Mean SOC (g kg-1) across eight maps
    - Band 2: Standard deviation (SD) of SOC
    - Band 3: Coefficient of variation (CoV = SD/Mean)
    - Band 4: Signal-to-noise ratio (SNR = Mean/SD)
    - Band 5: Most deviant map from the mean (coded 1–13; ties possible)
      - Codes map to specific primary maps or tied groups
    - Band 6: Greatest deviation from the mean expressed as a percentage
    - Band 7: Greatest deviation from the mean expressed as the number of SDs exceeded
  - Notes on variability
    - Higher CoV (>1) indicates substantial disagreement between maps at a location
    - SNR much greater than 1 indicates stronger agreement
  - Purpose of band 5–7
    - Help users identify which map(s) drive disagreements and quantify the scale and direction of deviations

- Data structure and access
  - File: SOC_map_summaries.tif (geotiff)
  - 7 bands, GB-wide (excluding Northern Ireland), 1 km resolution
  - Band descriptions
    - Band 1: Mean SOC (g kg-1) across all eight maps; no-data where any map missing
    - Band 2: SD of SOC across eight maps
    - Band 3: CoV (SD/Mean)
    - Band 4: SNR (Mean/SD)
    - Band 5: Most deviant map from mean (1–13, with mapping to maps)
    - Band 6: Greatest percentage deviation from mean
    - Band 7: Greatest deviation from mean in standard deviations
  - Geographic scope
    - GB land area; excludes urban/built-up and rocky inland/coastal areas in predictions

- Quality control and validation
  - Checks performed prior to submission (19 Oct 2022):
    - All layers share identical spatial resolution, extent, and CRS (EPSG:27700)
    - Bands stacked into a single raster; inspected in ArcMap and R
    - Cell size: 1000 m; extent and grid alignment verified
    - All grid cells with complete eight-map data identified; no unintended no-data masking
    - SOC value ranges verified and corrected as needed
    - Documented ranges for mean, SD, and band values; confirmed there are 205 ties across map combinations
  - Rationale for data handling
    - Some maps include zeros that are valid predictions rather than no-data
    - Negative values and implausible SOC values addressed to maintain data integrity

- Third-party datasets and usage notes
  - Source mappings and access details provided for each of the eight maps, including DOIs and project references
  - Some data (e.g., CSGB-KRGS) may have access restrictions due to safeguarding sampling point locations
  - When using the ensemble data, proper citations include the eight source maps (specific references listed in the document)

- Practical considerations for GIS work
  - The dataset is suitable for overlay with other 1 km-resolution layers in GB GIS analyses
  - Band 1–4 provide core ensemble statistics for mapping and modelling SOC distribution and uncertainty
  - Band 5–7 support diagnostic analysis to identify maps driving discrepancies and quantify uncertainty
  - Built-up, rocky, and some coastal/interior non-soil areas are excluded from SOC predictions; consider complementary data if analysing such areas
  - Use the included citations to reference original SOC maps and methods in publications or data releases

- Data use and citation
  - Derived dataset should be cited with the eight primary map sources:
    - CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF
    - ISRIC-2017, ISRIC-2020
    - LUCAS, OCTOP
  - Supporting papers and data portals are listed for detailed methodology and map descriptions
  - Specific citations are provided in the document for each source map and related methodology

- Funding and affiliation
  - Part of the UK-SCAPE SOC-D project delivering National Capability
  - Funded by the Natural Environment Research Council (Grant NE/R016429/1)
  - Authors affiliated with UKCEH and collaborating institutions

- End note
  - The accompanying Sci. Rep. reference provides comprehensive background and methodological details for the eight-map comparison underpinning this ensemble analysis.