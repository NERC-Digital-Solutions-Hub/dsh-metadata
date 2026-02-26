# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Produces 5x5 km resolution gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Data derived from measured concentrations of gases and particulate matter in air and ions in precipitation, collected at the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Deposition values are provided as rolling 3-year means, with ecosystem-specific values and grid-wide averages.

## Data generation and processing
- Site-based measurements are interpolated to create UK-wide concentration maps.
- Wet deposition combines precipitation concentrations with annual precipitation maps (from the UK Met Office) and includes direct deposition of cloud droplets to vegetation (occult deposition).
- Dry deposition uses gas and PM concentration maps with habitat-specific deposition velocities to estimate deposition to five land cover categories: forest, moorland, grassland, arable, and urban.
- Deposition to land cover categories is combined in each 5x5 km grid square based on the relative proportions of land cover.
- Critical load calculations apply deposition for moorland to all non-woodland habitats and deposition for forest to all woodland habitats.

## Wet vs Dry deposition details
- Dry deposition components include:
  - Gases: Sulphur Dioxide (SO2), Nitric Acid (HNO3), Nitrogen Dioxide (NO2), Ammonia (NH3).
  - Particulate matter: sulphate, nitrate, ammonium, calcium, magnesium.
- Wet deposition includes deposition from precipitation and occult deposition for sulphate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion).
- Anthropogenic vs. total deposition is separated for sulphur and calcium using sea-salt ion ratios.
- Orographic enhancement accounts for increased precipitation ion concentrations in upland regions, based on observations from Great Dun Fell and Holme Moss.

## Temporal and ecosystem-specific data
- Inter-annual variability influenced by weather patterns; CBED deposition is averaged over a three-year period to smooth fluctuations.
- Data are calculated annually but provided as rolling 3-year means.
- Two ecosystem-specific datasets:
  - Moorland deposition (assuming moorland/short vegetation everywhere).
  - Forest deposition (assuming forest/woodland everywhere).
- Grid-average deposition values are also provided as 3-year rolling means.

## Data structure and formats
- Three 3-year mean CSV files:
  - CBED-deposition-moorland-2015-2017.csv
  - CBED-deposition-forest-2015-2017.csv
  - CBED-deposition-gridaverage-2015-2017.csv
- Common columns:
  - easting: centre of the 5x5 km grid square (metres)
  - northing: centre of the 5x5 km grid square (metres)
  - deposition values for each pollutant (units: keq ha-1 year-1)
- Example pollutant columns:
  - Moorland: nox_m (oxidised nitrogen), nhx_m (reduced nitrogen), nms_m (non-marine sulphur), nm_ca_mg_m (non-marine base cations)
  - Forest: nox_f, nhx_f, nms_f, nm_ca_mg_f
  - Grid average: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga
- Unit conversions:
  - keq ha-1 year-1 to kg S ha-1 year-1: multiply by 16 (for sulphur)
  - keq ha-1 year-1 to kg N ha-1 year-1: multiply by 14 (for nitrogen)
  - keq ha-1 year-1 to kg Ca ha-1 year-1: multiply by 20 (for base cations)
- Data structure is designed for straightforward integration into exposure and ecosystem impact analyses.

## Quality control and validation
- Methods align with Government QA standards for analytical models.
- Subject to extensive peer review and part of Defra model inter-comparison exercises (e.g., Carslaw 2011).
- Documentation practices include version control, central storage of code, and longstanding publication in peer-reviewed literature.
- Mass balance checks are routinely performed to ensure numerical consistency with historical years.

## Usage notes and caveats
- Values represent 3-year rolling means to mitigate inter-annual variability due to weather and atmospheric processes.
- Distinct ecosystem assumptions (moorland vs forest) influence deposition estimates; grid averages provide a general baseline.
- Interannual variations can still occur due to natural climate variability and atmospheric transport.

## Access and resources
- Primary resource page: http://www.pollutantdeposition.ceh.ac.uk/ukeap
- Supporting information: https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
- Fieldwork and instrumentation: N/A; Calibration: N/A
- Related literature and model documentation (peer-reviewed): Carslaw 2011 and additional CBED references
- Notes on units, conversions, and methodological details are included within the data files and accompanying metadata.