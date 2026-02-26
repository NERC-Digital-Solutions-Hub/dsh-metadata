# Enhanced Future FLows and Groundwater (eFLaG): Gridded simulations of available precipitation for Great Britain Supporting Information Document

- A national dataset of available precipitation (rainfall + snowmelt) for Great Britain at 1 km resolution, covering observational period 1961–2018 and climate-projection period 1980–2080.
- Purpose: provide consistent driving data for eFLaG hydrological projections across river flow, groundwater levels, and groundwater recharge, supporting drought and climate resilience assessments.

## Overview of the eFLaG dataset
- Observational data are derived from HadUK-Grid precipitation and temperature (1 km daily), aligned to UKCP18 frameworks.
- Climate projections come from UKCP18 regional climate model ensembles (RCM PPE) for 12 members at 12 km resolution, spanning 1980–2080, based on a single high-emissions scenario (RCP8.5).
- Both observational and projection data are converted to available precipitation by applying a snow module that accounts for snowmelt processes.

## Observational data
- HadUK-Grid used as the baseline observational dataset; interpolated UK land-surface observations to a uniform UK grid.
- Purpose: support monitoring of UK climate and calibration of climate-change impact analyses; products used at 1 km resolution in this study.

## Climate projections (UKCP18 RCM PPE)
- Ensemble: 12 high-resolution projections (12 km) from HadGEM3-GC3.05 and HadREM3-GA705, with 360-day calendar (12 months of 30 days).
- Bias correction: monthly correction factors derived by comparing 1981–2010 RCM outputs to HadUK-Grid observations; factors are smoothed to reduce discontinuities.
- Downscaling: bias-corrected 12 km data downscaled to 1 km using SAAR-based weighting.
- Temperature: daily min/max temperatures downscaled to 1 km using lapse rates and elevation data.

## Methodology for generating available precipitation
- Snow module converts precipitation to available precipitation (rainfall + snowmelt) based on daily temperature thresholds and snow-melt parameters.
- Applied separately to observational-based and bias-corrected/downscaled RCM-based simulations.
- Snow module parameters (Table 1 in the document) include lapse rate, snow threshold temperatures, melt factor, drainage and storage characteristics, and snow fraction adjustments.

## Data structure and products
- Total: 264 NetCDF files.
- Observational simulations: 12 NetCDF files (1961–2018, split into 5-year periods; final file covers 2016–2018).
- RCM simulations: 252 NetCDF files (21 periods × 12 ensemble members; ensemble members numbered 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15).
- Time coverage: RCM data Dec 1980–Nov 2080; first file covers 1980–1984, last file covers 2080 (Jan–Nov); intermediate files generally cover five-year blocks.
- Spatial framework: British National Grid, 1 km resolution; units: kg m^-2 (equivalent to mm day^-1).
- File naming conventions (examples):
  - avail_precip_obs_196101_196512.nc (observational period Jan 1961 to Dec 1965)
  - avail_precip_rcm01_198012_198412.nc (RCM ensemble member 01, Dec 1980 to Dec 1984)
- Data management: organized to keep file sizes manageable; includes quality control and provenance notes.

## Quality control and governance
- Visual quality assurance performed to verify data plausibility across the grid.
- Documentation provides clear provenance, processing steps, and references to underpin transparency and reproducibility.

## Use within the eFLaG project
- Provides a common driving data source for hydrological models used in eFLaG (Grid-to-Grid, PDM, GR4J, GR6J) and groundwater models (Aquimod for groundwater levels; ZOODRM for groundwater recharge).
- Ensures standardized, quality-assured inputs for future drought and climate-resilience projections.

## Key limitations and considerations
- Calendar alignment: RCM data use a 360-day year; no calendar adjustment was applied to match the 365/366-day observed sequence to avoid introducing artificial data.
- Climate uncertainty representation: PPE members share the same high-emissions scenario (RCP8.5) and underlying model structure, which means the dataset does not fully span the broader climate-uncertainty space.
- Bias correction caveat: correction factors are derived from historical comparisons (1981–2010) and may not fully capture all future biases or regional non-stationarities.
- Snow and parameter sensitivity: snow module parameters influence available precipitation estimates and carry inherent uncertainties related to snow processes and meteorological inputs.

## References (selected)
- Bell, V.A. et al. 2016; 2007
- Guillod, B.P. et al. 2018
- Hannaford, J. et al. 2022 (eFLaG core publication)
- Hollis, D. et al. 2019 (HadUK-Grid)
- Kay, A.L. & Crooks, S.M. 2014
- Lowe, J.A. et al. 2019 (UKCP18 science overview)
- Murphy, J.M. et al. 2018 (UKCP18 land projections)
- Prudhomme, C. et al. 2012
- Teutschbein, C. & Seibert, J. 2012