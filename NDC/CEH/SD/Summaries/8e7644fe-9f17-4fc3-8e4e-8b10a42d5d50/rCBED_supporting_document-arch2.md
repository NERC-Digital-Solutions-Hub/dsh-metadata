# Methods

## Overview
- CBED (Concentration-Based Estimation of Deposition) generates 5x5 km resolution gridded estimates of deposition flux for nitrogen, sulfur, and base cations across the UK.
- Uses measured concentrations of gases and particulates in air, plus ion concentrations in precipitation; observations from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Outputs include both air/droplet deposition estimates and grid-square deposition disaggregated by land cover categories.

## Deposition components and data sources
- Dry deposition: combines gas/PM concentration maps with land-cover-specific deposition velocities for five land-cover types (forest, moorland, grassland, arable, urban).
- Wet deposition: derived from precipitation ions plus direct deposition to vegetation (occult deposition); accounts for sulphate, ammonium, nitrate, calcium, magnesium, and hydrogen ions.
- Specific inputs:
  - NO2: Pollution Concentration Mapping (PCM) model (rural measurements plus point/line source modeling).
  - NH3: FRAME atmospheric transport model plus annual UKEAP measurements; FRAME adds local variability not captured by network alone.
  - SO2: rural measurements with an urban enhancement factor.
- Separation of anthropogenic vs. total sulphur and calcium uses sea-salt ion ratios; includes an orographic enhancement factor for upland precipitation.

## Temporal approach and uncertainty
- Inter-annual variability is substantial; to reduce noise, estimates are averaged over three-year periods (current year and two preceding years).
- Earlier years have more uncertainty due to incomplete measurements (e.g., aerosols); retrospective estimates rely on long-term mean fractions, increasing uncertainty mainly before 1996.
- The 3-year averaging smooths natural weather-related fluctuations and provides more stable long-term trends.

## Modelling implementation and versioning
- Original CBED model written in Genstat; re-implemented in R.
- Differences between R and Genstat versions arise from raster interpolation (kriging) and whether the long-term mean/orographic enhancement is recalculated annually.
- Some components (notably aerosols) were not measured in earlier years, affecting retrospective totals for total nitrogen and sulfur.

## Outputs and data structure
- Data exported as raster-derived CSV in xyz format.
- Values are 3-year means (e.g., 2012 represents 2010–2012) and cover 1986–2012.
- Deposition calculated for five land-cover categories; grid-square deposition is a weighted mean by land-cover fractions.
- Three output files:
  - rCBED_Fdep_gm2y_1986-2012_gridavg.csv — mean deposition weighted by land-cover fractions.
  - rCBED_Fdep_gm2y_1986-2012_forest.csv — deposition to forest (assuming full forest cover per grid cell).
  - rCBED_Fdep_gm2y_1986-2012_moor.csv — deposition to moorland (assuming full moorland cover per grid cell).
- File schema includes: year (end-year of the 3-year period), grid coordinates (easting/northing), and deposition fluxes for H+, NOx, NHx, Ntot, SOx, xSOx, Ca, Mg, CaMg, Cl, with units such as g m^-2 year^-1 (note: units per component are specified in the files).

## Quality control and validation
- Underpins procedures aligned with government QA standards for environmental models.
- CBED data and calculations have undergone extensive peer review and participated in Defra model inter-comparison exercises.
- Documentation, version control, and centralized code storage are maintained; mass-balance checks ensure numerical consistency and are compared against previous years.

## Access and references
- Data and supporting information available via:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - UK-AIR Defra network information: https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
- Foundational references include work by Smith, Fowler, Sutton, and colleagues on CBED, UKEAP, PCM, FRAME, and related deposition modelling and uncertainty analyses.

## Limitations and considerations for use
- Uncertainty is higher in years with sparse measurements or where retrospective estimation was necessary (pre-1996).
- Interpolation across the UK from a relatively sparse network introduces additional uncertainty.
- Temporal resolution is constrained by the 3-year averaging approach; year-to-year trends should be interpreted with caution.
- Outputs are provided for specific grid- and land-cover aggregations; users may need to reweight or regrid for other analyses.