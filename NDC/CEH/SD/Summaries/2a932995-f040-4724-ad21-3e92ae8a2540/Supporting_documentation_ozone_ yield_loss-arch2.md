# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2.

## Purpose and scope
- Quantifies annual average yield loss due to ozone for maize, rice, soybean, and wheat during 2010–2012.
- Produces a standardized, GIS-ready dataset on a 1° by 1° global grid to support environmental health and policy monitoring.

## Data collection and inputs
- Grid creation: 1° × 1° grid using ArcMap (v10.3).
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000) with irrigated and non-irrigated classifications.
- Data processing: sum production per grid cell; estimate 2010–2012 average production per cell using a conversion factor from FAO national data (1999–2001 vs 2010–2012).
- Inclusion criteria: only grid cells with >500 tonnes total production included.
- Spatial classification: assign hemispheres (Northern/Southern) and climate zones using ESDAC JRC GIS layer; determine 90-day growing periods per climate zone and hemisphere (Table S1 from Mills et al. 2018a).
- Crop-specific growing periods and zonation are detailed for maize, rice, soybean, and wheat.

## Model and methodology
- Ozone exposure metric: POD3 IAM (phytotoxic ozone dose above 3 nmol m^-2 s^-1) calculated from the EMEP MSC-W model (version 4.16) using hourly ozone concentration, temperature, VPD, irradiance, and soil moisture.
- Growing-period uptake: accumulate 90-day POD3IAM per grid cell based on climate- and hemisphere-specific growing periods.
- Baseline subtraction: subtract a reference POD3IAM of 0.1 mmol/m^2 (pre-industrial levels) before yield loss calculation.
- Yield-loss relationship:
  - Wheat: Percent Yield Loss = (POD3IAM - 0.1) × 0.64.
  - Other crops (maize, rice, soybean): compute relative ozone sensitivity by dividing each crop’s M7 (7-hour mean ozone concentration) slope by the wheat slope; apply wheat yield loss to obtain the crop yield loss via multiplication by this relative sensitivity.
- Outputs per grid cell: final estimated percentage yield loss for each crop, stored in 1° × 1° GIS cells.

## Output data and structure
- Four GIS shapefiles (one per crop): maize, rice, soybean, wheat.
- Each shapefile contains grid cells with five attributes:
  - ID: unique grid cell identifier
  - Zone: climate zone for the grid cell
  - Long_Lat: center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South (where applicable)
  - Yloss: annual average percentage yield loss (2010–2012)

## Quality control and validation
- Model validation: comparison of EMEP model outputs with Global Atmosphere Watch (GAW) observations shows good alignment for peak ozone periods.
- Key metrics:
  - Dmax and M7 (model vs observed) across multiple GAW sites in 2012 with r^2 between 0.88 and 0.93 after outlier adjustments.
  - AET/PET-based proxy analysis (using POD3IAM/M7) indicates strong correlation (r^2 = 0.63) with stomatal conductance, supporting treatment of ozone uptake.
- Overall conclusion: first-use of ozone flux (POD3IAM) rather than concentration for global crop yield impact; caveats acknowledged (notably limited flux data for maize, rice, soybean).

## Uncertainties and caveats
- No comprehensive flux–response data for maize, rice, or soybean; relative sensitivities are based on wheat flux with M7-based scaling.
- Maize yield-loss data relies on a small set of older cultivars, increasing uncertainty for maize.
- Some regions have multiple growing seasons per year (e.g., India); only the most important growing period was used.
- Physiological differences among crops and environments may affect uptake beyond concentration differences captured by M7.

## Data provenance and references
- Primary methodology and model validation described in Mills et al. (2018a) and Mills et al. (2018b).
- Data sources include FAO GAEZ for production, ESDAC/JRC climate zones, and EMEP MSC-W for ozone flux modeling.
- Related technical descriptions and modelling updates cited (EMEP model documentation, CLRTAP references).

## How this supports monitoring and policy analysis
- Provides standardized, transparent, and spatially explicit estimates of ozone-related yield losses that can be integrated into environmental health dashboards and policy performance assessments.
- The standardized 1° grid and clear data structure facilitate cross-dataset comparisons and reproducibility.
- Emphasizes data quality assurance, model validation, and explicit caveats to inform interpretation and further improvement (e.g., incorporation of species-specific flux data when available).