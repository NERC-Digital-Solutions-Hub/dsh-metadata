# Supporting information

## Overview
- Monthly global methane emissions from natural wetlands at 0.5° x 0.5° resolution.
- Model output from the JULES land surface model driven with WFDEI meteorological data.

## Variables included
- fwetl: Fraction of wetland in each gridbox.
- fch4_wetl: Gridbox methane flux from natural wetland (mg CH4 m-2 day-1), scaled so total global wetlands emissions equal 180 Tg CH4/year.
- cs: Gridbox soil carbon in each pool (decomposable plant material, resistant plant material, microbial biomass, humus).
- t_soil: Gridbox sub-surface temperature of each soil layer.

## JULES Model and configuration
- Joint UK Land Environment Simulator (JULES) v4.5 with dynamic vegetation (TRIFFID) but competition disabled; vegetation cover prescribed from IGBP.
- Uses Van Genuchten soil properties; topography and soil aspects integrated via specified parameters.
- Methane emission scheme uses dynamic soil carbon with a temperature-dependent component (Q10) and a parameterized pool-structure sum.

## Methane emission scheme details
- fch4_wetl = k * fwetl * Q10(t_soil1m)^(t_soil1m / T0) * Σi κ_i * cs_i
- Pool-specific κ values: DPM, RPM, BIO, HUM with defined constants.
- Global scaling k = 7.034e-10 chosen to yield 180 Tg CH4/year globally (in year 2000).
- fwetl is computed via TOPMODEL hydrology within JULES.

## Outputs and flexibility
- All variables included to allow users to disentangle outputs and apply their own inputs.
- Example: to apply a user-observed wetland area map, use (fch4_wetl / fwetl) * observed_wetland_dataset.

## Input data and sources
- Meteorological driving data: WFDEI (WATCH Forcing Data for ERA-Interim).
- Hydrological and thermal soil properties: Harmonised World Soil Database (FAO, 1995); regridded with CAP software.
- Topographic index: HydroSHEDS data (produced by Toby Marthews, CEH).
- Vegetation map: IGBP land cover map (IGBP, 1992); regridded with CAP software.

## File format and accessibility
- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Data stored in yearly files with all variables in a single file.

## References (key sources)
- JULES model descriptions and related methodological papers (Best et al., Clark et al., 2011; 2010).
- Gedney et al. (2004) on wetland methane emissions scheme.
- IGBP (1992) vegetation data; FAO (1995) soil map; Marthews et al. (2014, 2015) topographic and soil parameter products.
- Parker et al. (2018), McNorton et al. (2016), Weedon et al. (2011) supporting data and forcing datasets.