# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Aim
- Present modelled topsoil pH estimates (0–15 cm depth) at 1 km² resolution across Great Britain for 2007.
- Enable environmental monitoring and policy scrutiny by providing standardized, comparable outputs.

## Data and method overview
- Based on Countryside Survey data from 2007, using 2446 sampling locations across GB.
- Spatial resolution: 1 km²; depth: 0–15 cm.
- Previous estimates used a simpler model; the current approach uses a Generalized Additive Mixed Model (GAMM) that incorporates climate, atmospheric deposition, habitat, soil, and spatial variables.
- Random effects account for nesting of samples within 1 km² survey squares.
- Non-linear smoothing for climate and deposition variables; two-dimensional tensor product smooths for latitude/longitude to capture large-scale spatial variation.
- Distribution: Tweedie (variance power = 1.01), since Gaussian was inappropriate.
- Model fitting implemented in R using mgcv's gamm function.
- Full methodological details are provided in Thomas et al. 2020.

## Model details
- Response: soil pH (mean value for 2007).
- Key components: s(5-year mean winter temperature); s(5-year mean spring temperature); s(5-year mean summer temperature); s(5-year mean autumn temperature); smoothed precipitation terms; three-year deposition terms for NO3, NH4, and SO4; spatial te(Easting, Northing) with multiple resolutions; and various parametric terms for habitat and soil characterizations.
- Variables include climate (seasonal temperatures and precipitations), deposition metrics, Easting/Northing coordinates, Broad Habitat, CACO3 Rank, and Soil Group (and related material models).
- Data attributes described in the dataset: CS_topsoil_ph_gam.nc with soil_pH (mean 2007 modelled value), VAR (standard error ratio), x/y coordinates (OSGB 27700), and a transverse_mercator reference.

## Dataset and attributes
- Dataset: CS_topsoil_ph_gam.nc
- Soil_pH: mean pH value for 2007 modelled via GAM; units = pH units.
- VAR: standard error associated with Soil_pH divided by the predicted mean; units = ratio.
- x, y: Easting/Northing coordinates (OSGB 1936 / British National Grid; EPSG:27700); units = metres.
- transverse_mercator: coordinate reference system indicator; unitless.

## Variables used
- Climate: 5-year mean winter, spring, summer, and autumn temperatures (degrees C) and 5-year mean winter, spring, summer, autumn precipitations (mm).
- Atmospheric deposition: 3-year mean NO3, NH4, and SO4 deposition (kg ha⁻¹ yr⁻¹).
- Spatial: Easting/Northing at multiple resolutions; te(Easting, Northing) terms.
- Habitat and soil predictors: Broad Habitat, CACO3 Rank, Soil Group, plus related classifications (e.g., Land Cover Map 2007; soil parent material models).

## Data quality, sampling, and QA
- Sampling protocol used a 15 cm long by 5 cm diameter core.
- Field measurements: 10 g soil with 25 ml deionised water (soil:water ratio 1:2.5 by weight).
- Quality control followed Defra/NERC Joint Codes of Practice.
- Technical references include CS soils manuals and 2007 soils report (Emmett et al. 2008, 2010) and Reynolds et al. 2013 for soil change context.

## Application and references
- Supports monitoring of environmental health, showing how topsoil pH relates to climate, deposition, and land-use factors.
- Key supporting documents: Reynolds et al. (2013); Emmett et al. (2008, 2010); Henrys et al. (2012); Morton et al. (2014); Thomas et al. (2020); Dore et al. (2015).
- Thomas et al. (2020) provides the detailed patterns and trends analysis that underpins the modelling approach.

## Access and reuse
- The resulting dataset is stored and uploaded to appropriate data portals for broader accessibility and reuse by researchers and policy analysts.
- Data are designed to be combined with other environmental datasets to enhance value and support broader monitoring objectives.