# This dataset provides monthly global methane emissions from natural wetlands at 0.5 o x 0.5 o resolution (Parker et al., 2018; McNorton et al., 2016)

## Purpose and scope
- Monthly global methane emissions from natural wetlands at 0.5° x 0.5° resolution.
- Model output generated with the JULES land surface model driven by WFDEI meteorological forcing.
- Outputs include fluxes, wetland fraction, soil carbon pools, and soil temperature.

## Key variables and outputs
- fwetl (dimensionless): Fraction of wetland in each grid cell.
- fch4_wetl (mg CH4 m-2 day-1): Gridbox methane flux from natural wetlands; globally scaled so total wetland emissions are 180 Tg CH4.
- cs (kg m-2): Soil carbon in each pool (decomposable plant material, resistant plant material, microbial biomass, humus).
- t_soil (K): Sub-surface temperature of the top soil layer.

## Model and methodology
- Model: Joint UK Land Environment Simulator (JULES) version 4.5 with TRIFFID (dynamic vegetation; competition disabled; vegetation prescribed from IGBP).
- Methane emission scheme: fch4_wetl = k × fwetl × Q10(t_soil1m)^(t_soil1m / T0) × Σ_i (κ_i × cs_i), with pool-specific κ values (DPM, RPM, BIO, HUM) and Q10 functioning as per Clark et al. (2010).
- Global scaling factor k = 7.034×10^-10 to achieve 180 Tg CH4/year in 2000.
- fwetl calculation: TOPMODEL hydrology embedded in JULES; full description in Gedney et al. (2004).

## Input data and drivers
- Meteorological forcing: WFDEI (Watch Forcing Data applied to ERA-Interim).
- Hydrological and soil properties: Harmonised World Soil Database (FAO, 1995); regridded with CAP software.
- Topographic index: HydroSHEDS data (Marthews et al., 2015).
- Vegetation: IGBP land cover map (1992); regridded with CAP software.

## File format and data accessibility
- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Data stored as yearly files with all variables in a single file.

## How to use and re-use
- All variables are included to facilitate user analyses; for example, to apply an observed wetland area map, compute fch4_wetl per unit wetland fraction by fch4_wetl ÷ fwetl and multiply by an external wetland dataset.
- Outputs are suitable for monitoring environmental health and policy performance over time, with standardized formats enabling comparison and integration with other datasets.

## Practical notes for analysts
- Provides a transparent breakdown of methane emissions by wetland fraction and soil pools, enabling scenario testing and data fusion with other environmental indicators.
- Emphasizes standardized data handling, QA, and clear data provenance for reproducibility and broader accessibility.