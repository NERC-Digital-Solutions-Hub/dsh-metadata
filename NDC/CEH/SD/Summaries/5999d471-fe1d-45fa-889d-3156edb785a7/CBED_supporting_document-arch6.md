# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Produces 5x5 km resolution gridded data of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Data are derived from gas/particle concentrations and precipitation measurements across the UK, using the UKEAP network.
- Outputs are provided as rolling 3-year means, with ecosystem-specific (moorland vs forest) and grid-average datasets.

## How deposition is estimated
- Site-based measurements are interpolated to generate UK concentration maps.
- Wet deposition is calculated by combining precipitation data with precipitation-derived ion concentrations, including direct cloud deposition (occult deposition) and an orographic enhancement factor in uplands.
- Dry deposition uses gas and particulate concentration maps plus habitat-specific deposition velocities to estimate deposition to five land-cover categories: forest, moorland, grassland, arable, and urban.
- For critical load exceedance, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.
- Nitric acid concentrations are interpolated from ~30 sites; NO2 and SO2 concentrations come from the PCM model, which blends rural measurements with point/line source modelling.
- Ammonia concentrations come from FRAME (with 2017 emissions) plus UKEAP measurements to capture local variability.
- Inter-annual variability due to weather is acknowledged; deposition estimates are averaged over a 3-year period to smooth fluctuations.

## Temporal and ecosystem specifics
- Data are calculated annually but published as rolling 3-year means.
- Ecosystem-specific data are produced for two assumptions: moorland/short vegetation everywhere and forest everywhere.
- A grid-average dataset is also provided, representing an overall UK-wide deposition estimate.

## Data outputs and file structure
- 3-year mean, ecosystem-specific deposition data, for each 5x5 km grid square:
  - CBED-deposition-moorland-2016-2018.csv
    - Columns include: easting, northing, nox_m (oxidised nitrogen), nhx_m (reduced nitrogen), nms_m (non-marine sulphur), ca_mg_m (base cations).
  - CBED-deposition-forest-2016-2018.csv
    - Columns include: easting, northing, nox_f, nhx_f, nms_f, ca_mg_f.
  - CBED-deposition-gridaverage-2016-2018.csv
    - Columns include: easting, northing, nox_ga, nhx_ga, nms_ga, ca_mg_ga.
- Grid-average 2015-2017 dataset is also provided (CBED-deposition-gridaverage2015-2017.csv) with the same variable types.
- Units: all deposition values are in keq ha^-1 year^-1 (kiloequivalents per hectare per year).
- Grid-average file has fewer mapped squares (10678 rows) than the forest/moorland files (11172 rows) because it requires all nitrogen forms to be present.
- Conversion to kilograms per hectare per year:
  - Sulphur: multiply keq ha^-1 y^-1 by 16 to obtain kg S ha^-1 y^-1
  - Nitrogen (oxidised/reduced): multiply keq ha^-1 y^-1 by 14 to obtain kg N ha^-1 y^-1
  - Base cations (Ca+Mg): multiply keq ha^-1 y^-1 by 20 to obtain kg Ca ha^-1 y^-1

## Data quality and validation
- CBED data and calculations have undergone extensive peer review and participated in Defra model inter-comparison exercises (e.g., Carslaw 2011).
- Procedures for documenting method developments, version control, and central storage of code are followed.
- Mass balance checks are routinely performed and compared with previous years for consistency.
- Results are widely published in peer-reviewed literature.

## Access, references, and supporting information
- Data and methodology are supported by multiple sources:
  - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP)
  - Pollution Concentration Mapping (PCM) model for NO2 and SO2
  - FRAME model and related atmospheric transport modelling for NH3
- Supporting information and network details are available via the provided URLs:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap

## Notes and limitations
- Inter-annual variability in deposition due to weather and atmospheric conditions is smoothed by using 3-year means.
- Orographic enhancement and occult deposition are important components, particularly in upland regions.
- The grid-average deployment may have fewer squares due to missing data in some 5x5 km grid cells.