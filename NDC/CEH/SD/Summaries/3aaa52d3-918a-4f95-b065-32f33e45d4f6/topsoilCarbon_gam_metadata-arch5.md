# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Purpose and scope
- Provides modelled topsoil carbon concentration (0-15 cm) across Great Britain at 1 km2 resolution for 2007.
- Based on Countryside Survey data from 2446 locations; uses a Generalized Additive Mixed Model (GAMM) framework to generate spatially explicit estimates.
- Article describes the modelling approach and variables, and references Thomas et al. (2020) for full methodological details.

## Modelling approach
- Generalized Additive Mixed Model (GAMM) using a Tweedie distribution (variance power = 1.99) via the mgcv R package.
- Includes a random effect to account for nesting of samples within 1 km2 survey squares.
- Non-linear smooth functions applied to climate and atmospheric deposition; two-dimensional tensor product smooths for spatial coordinates (latitude, longitude) to capture large-scale spatial variation.
- Not Gaussian; model fit and structure chosen to suit the data characteristics.

## Data structure and attributes
- Dataset: CS_topsoil_carbon_gam.nc
- Target variable: Soil_OrgC_Conc — mean 2007 modelled soil carbon concentration, units in g kg-1.
- Uncertainty: VAR — standard error ratio (standard error divided by predicted mean).
- Spatial metadata: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); coordinate reference system defined; transverse Mercator description included.
- Modelling terms: includes smoothed terms for climate (e.g., 5-year mean summer temperature and precipitation, spring and winter temperatures), atmospheric deposition (SO4, NH4, NO3), and 2D spatial terms te(Easting, Northing); additional categorical and material variables (Broad Habitat, Soil Group, CACO3 Rank, Soil Parent Material Model) used as factor or mapped covariates.
- Resolution and scope: 1 km2 grid across Great Britain; predictors combine climate, deposition, habitat/soil information, and spatial location.

## Data provenance, sampling, and quality control
- Sampling and analysis follow CS methodologies (15 cm cores, LOI measurement, conversion to carbon concentration using a 0.55 factor with calibration against total elemental analysis).
- Methods aligned with CEH SOP3102 and Defra/NERC Codes of Practice; QA checks implied through calibration and standard protocols.
- Original data and methodology are documented in supporting reports and papers (Reynolds et al. 2013; Emmett et al. 2008, 2010; Henrys et al. 2012; Thomas et al. 2020).

## Availability, updating, and governance
- Modelling outputs are 2007-derived estimates intended for broad inference on topsoil carbon across GB.
- Data and methodological details are supported by multiple sources and can be accessed via the cited data centre references (e.g., NERC Environmental Information Data Centre) and associated technical reports.
- The study notes full methodological details in cited reports (e.g., Emmett et al., Reynolds et al., Thomas et al.) and situates the data within a framework of climate, deposition, habitat, and soil predictors.

## Considerations for data stewardship
- Metadata completeness: clear variable descriptions, units, coordinates, and spatial/temporal context; presence of a dedicated data file (cs_topsoil_carbon_gam.nc) with explicit attributes.
- Data quality and uncertainty: VAR provides a measure of predictive uncertainty; model-based estimates introduce uncertainties dependent on predictor quality and data coverage.
- Interoperability: spatial data in OSGB coordinates facilitates GB-scale integration; model terms are described with sufficient detail to reproduce or audit the analysis.
- Provenance and reproducibility: references to original data sources, field sampling protocols, and statistical methods enable traceability and potential reanalysis.

## References and supporting documents
- Reynolds et al. (2013) Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain.
- Emmett et al. (2008, 2010) Countryside Survey technical reports on soils manual and soils 2007.
- Henrys et al. (2012) Model estimates of topsoil carbon (Countryside Survey).
- Morton et al. (2014) Land Cover Map 2007.
- Thomas et al. (2020) Patterns and trends of topsoil carbon in the UK: complex interactions of land use change, climate and pollution.
- Supporting model documentation and data sources (Met Office, CBED deposition data, British Geological Survey, etc.).