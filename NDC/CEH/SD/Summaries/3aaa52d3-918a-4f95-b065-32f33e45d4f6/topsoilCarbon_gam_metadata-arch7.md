# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Modelled estimates of topsoil carbon concentration (0–15 cm) across Great Britain for 2007 at 1 km2 resolution.
- Outputs derived from Countryside Survey data using a Generalized Additive Mixed Model (GAMM) with climate, deposition, habitat, soil, and spatial predictors.
- Data presented as gridded GIS-ready values with associated uncertainty.

## Data and modelling approach
- Data sources and scope
  - Based on soil carbon measurements from 2,446 field locations across GB (Countryside Survey).
  - Samples collected with a standardized core method; carbon concentration estimated from loss-on-ignition (LOI) adjusted with a factor of 0.55 (CEH method SOP3102).
  - For modelling, includes nesting of samples within 1 km2 survey squares.
- Modelling framework
  - Generalized Additive Mixed Model (GAMM) with a Tweedie distribution (variance power = 1.99).
  - Non-linear smooth terms for climate and atmospheric deposition; two-dimensional tensor product smooths for spatial location (Easting, Northing) to capture large-scale spatial variation.
  - Random effects account for the 1 km2 survey square structure.
  - Predictors include: climate (temperature, precipitation), atmospheric deposition (SO4, NH4, NO3), Broad Habitat and Soil factors, and Soil Parent Material.
- Output and references
  - The dataset CS_topsoil_carbon_gam.nc contains mean soil carbon concentration (Soil_OrgC_Conc) in g kg-1 and a VAR metric (standard error divided by the mean).
  - Full methodological details described in Thomas et al. (2020); supporting sampling and QA details in Emmett et al. (2008, 2010) and Reynolds et al. (2013).

## Data structure and attributes
- Dataset: CS_topsoil_carbon_gam.nc
- Key variables
  - Soil_OrgC_Conc: Mean soil carbon concentration (g kg-1) for 2007 model.
  - VAR: Standard error associated with Soil_OrgC_Conc divided by the predicted mean (dimensionless ratio).
  - x: Easting in metres (OSGB 1936/British National Grid, EPSG:27700).
  - y: Northing in metres (OSGB 1936/British National Grid, EPSG:27700).
  - transverse_mercator: Defines the mapping CRS (unitless in this context).
- Spatial context
  - Coordinate reference system: OSGB 1936 / British National Grid (EPSG:27700).
  - Mapping supports 1 km2 gridded representation across Great Britain.

## Spatial characteristics and mapping
- Resolution and extent
  - Modelled estimates across Great Britain at 1 km2 grid resolution.
- Predictor scales used in modelling
  - Climate and deposition predictors at specified resolutions (e.g., 5 km for some climatic variables; 1 km for spatial smooths).
- Map-ready data
  - NetCDF format suitable for GIS workflows; can be regridded or reprojected to other coordinate systems as needed.

## Data quality, limitations, and assumptions
- Sampling and methods
  - Soil carbon measured via LOI and converted to carbon concentration using a calibration factor; CEH UKAS-accredited SOP3102.
  - QA procedures follow Defra/NERC Codes of Practice.
- Modelling considerations
  - A Tweedie distribution was used because a Gaussian model was inappropriate for the data.
  - Spatial variation captured with 2D tensor product smooths; random effects account for sample nesting within 1 km2 squares.
- Limitations
  - Modelled estimates reflect 2007 conditions; extrapolation beyond observed data or to non-GB contexts should be treated cautiously.
  - Uncertainty represented by VAR; users should consider spatial and temporal scope when applying results to local decisions.

## How GIS specialists can use this data
- Integration and visualization
  - Load CS_topsoil_carbon_gam.nc into GIS for choropleth or gridded maps of topsoil carbon concentration (g kg-1) at 1 km2 resolution.
  - Use VAR to assess uncertainty and prioritize areas with higher model uncertainty for ground-truthing or targeted sampling.
- Data fusion and analysis
  - Join with other GB GIS layers (land cover, soil type, climate data, deposition maps) to explore relationships between soil carbon and spatial predictors.
  - Reproject or resample to alternative grid sizes or coordinate systems as needed for specific analyses.
- Practical considerations
  - Coordinate values are in OSGB 27700; plan CRS transformations accordingly.
  - The dataset is suitable for policy, planning, and public-facing map products where spatial patterns of soil carbon are of interest.

## References and supporting documents
- Thomas, A., Cosby, B.J., Henrys, P., Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment, 729, 138330.
- Reynolds, B., Chamberlain, P.M., et al. (2013). Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain—Acidity, Carbon, and Total Nitrogen Status. Vadose Zone Journal, 12(2).
- Emmett, B.A., Frogbrook, Z.L., Chamberlain, P.M., et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Emmett, B.A., Reynolds, B., Chamberlain, P.M., et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Henrys, P.A., Keith, A.M., Robinson, D.A., Emmett, B.A. (2012). Model estimates of topsoil carbon [Countryside Survey]. NERC EIDC.