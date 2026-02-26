# Supporting information

## Overview
- Provides monthly global methane emissions from natural wetlands at 0.5° x 0.5° resolution.
- Model output produced by the Joint UK Land Environment Simulator (JULES) driven with WFDEI meteorological data.
- Outputs include: fwetl (fraction of wetland in gridbox), fch4_wetl (gridbox methane flux from natural wetland, scaled to total global wetlands emissions of 180 Tg CH4), cs (soil carbon per pool), and t_soil (sub-surface temperature).

## Data and variables
- fwetl: fraction of wetland in each grid cell.
- fch4_wetl: gridbox methane flux from natural wetlands (mg CH4 m^-2 day^-1), scaled so global wetlands emit 180 Tg CH4/year (2000 baseline).
- cs: soil carbon per pool (kg m^-2) for decomposable plant material, resistant plant material, microbial biomass, and humus.
- t_soil: mean bulk temperature of the top 1 m soil column (K).

## Model and methane emission scheme
- JULES version 4.5 with dynamic vegetation model TRIFFID (competition disabled) and prescribed vegetation cover from IGBP.
- Emission calculation: fch4_wetl = k * fwetl * Q10(t_soil 1m)^(t_soil 1m / T0) * Σ_i (κ_i * cs_i)
  - κ values: DPM = 3.22e-7, RPM = 9.65e-9, BIO = 2.12e-8, HUM = 6.43e-10.
  - Q10 baseline: T0 = 273.15 K.
  - k = 7.034 x 10^-10 (global scaling to yield 180 Tg CH4/year in 2000).
  - t_soil 1m: mean bulk temperature of the top 1 m soil column.
- fwetl (wetland fraction) and water-soil interactions computed using TOPMODEL hydrology within JULES.
- The dataset enables users to disentangle output and apply their own wetland field (e.g., by dividing fch4_wetl by fwetl and multiplying by a user-provided wetland map).

## Input data and sources
- Meteorology: WFDEI (WATCH Forcing Data applied to ERA-Interim).
- Hydrological and thermal soil properties: Harmonised World Soil Database (FAO, 1995), regridded with CAP software.
- Topographic index: HydroSHEDS-derived data, produced by Toby Marthews (Marthews et al., 2015).
- Vegetation: IGBP land cover map, regridded with CAP software.

## File format and access
- Format: netCDF, CF-compliant, following CEH gridded dataset conventions.
- Organization: yearly files, with all variables contained in each file.

## How to use and interpret
- The dataset provides full transparency of the methane emission calculation, allowing re-use or adaptation:
  - To apply an observed wetland map, compute fch4_wetl / fwetl and multiply by the observed wetland dataset.
- Useful for analysts seeking to understand wetland methane contributions, perform sensitivity analyses, or integrate with other regional or global datasets.
- Noted limitations include reliance on model structure (JULES) and parameter choices to represent wetland emissions; scale is 0.5° with top-down modeling assumptions.

## References
- Key sources include: Gedney et al. (2004) for TOPMODEL-based emission formulation; Best et al. (2010), Clark et al. (2010, 2011) for JULES model descriptions; Parker et al. (2018); McNorton et al. (2016); Weedon et al. (2011) for WFDEI and forcing data; IGBP (1992) vegetation data; FAO (1995) soil database; Marthews et al. (2014, 2015) for high-resolution soil and topographic parameter maps.