# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

## Brief description
- CEH-GEAR provides 1-km gridded estimates of daily and monthly rainfall for Great Britain, Northern Ireland, and a ~3000 km2 catchment in the Republic of Ireland from 1890 onwards; updates annually as new raingauge data become available.
- Rainfall estimates are derived from the Met Office observed precipitation database; monthly estimates use monthly totals and daily data when a full month is available.
- Natural neighbour interpolation with a normalization step based on average annual rainfall (SAAR) is used to generate the grids; daily estimates cover 09:00 on a day to 09:00 GMT the next day.
- Development follows BS7843-4:2012 guidelines; detailed methodology described in Keller et al. (2014).

## Data sources
- Met Office collated daily and monthly UK rainfall observations (MIDAS; data provided to CEH monthly under licence); CEH maintains a synchronized copy in an Oracle database with systematic quality control to discard unrealistic extremes.
- Met Office SAAR 61-90 grid (GB) and Met Eireann 1961-90 SAAR grid (NI) used for normalisation.
- Additional reference sources for QA and methodological context cited in the accompanying documentation.

## Method for deriving the daily and monthly grids
- Interpolation: natural neighbour interpolation with normalization by SAAR (no varying scale factor to keep model simple).
- Daily grids:
  - Use all available daily raingauges; generate provisional grids.
  - Apply a monthly correction factor so the sum of daily grids matches the monthly grids, incorporating information from monthly data (use monthly gauges when daily and monthly gauges share coordinates).
- Monthly grids:
  - Generated from the monthly network; for months with a complete set of daily gauges, daily totals are summed to obtain the monthly value.
- Output: rainfall depth in millimetres (mm) for daily and monthly grids.

## Minimum distance grids
- Each grid point records the distance to the closest gauge used; a 100 km threshold is applied, beyond which rainfall estimates are not produced to avoid low representativeness.
- Acknowledges sparser network in pre-1961 data, leading to gaps in Scotland, Wales, and parts of southwest England.
- Ancillary grids (updated yearly) provide:
  - Year of first missing data for each grid point
  - Year of last missing data for each grid point
  - Total number of missing days for each grid point (separately for monthly and daily data)

## Quality control
- A four-step QC protocol identifies and rejects unrealistically high values by comparing daily observations with a 200-year return period rainfall derived from the Flood Estimation Handbook.
  - Step 1: Identify days/gauges exceeding reference rainfall.
  - Step 2: Cross-check against major rainfall event databases if a match is found.
  - Step 3: Visually assess using daily rainfall maps (post-1961 GB) to confirm plausibility.
  - Step 4: Time-series comparison with up to ten nearest gauges to verify consistency; many high values are due to multiday accumulations, inconsistent reporting, or data flag issues.
- Multiday accumulations and inconsistent data are rejected, and affected data are removed from the rainfall database used for grid generation.

## Format of the CEH-GEAR dataset
- Stored in NetCDF4 format following CEH gridded dataset conventions.
- Organized by year; separate folders for Great Britain and Northern Ireland; daily and monthly grids stored separately.
- Core variables: rainfall amount and minimum distance (to closest gauge).
- Includes yearly missing-record NetCDF4 files and three ancillary grids (monthly and daily): first missing year, last missing year, and total missing days for each grid point.

## References
- Collier, C. G., Fox, N. I., and Hand, W. H. (2002) Extreme Rainfall and Flood Event Recognition.
- Keller, V. D. J. et al. (2015) CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
- Spackman (1993); Stewart et al. (2011); Svensson et al. (2009); Walsh (2012) and related works cited in the supporting information.