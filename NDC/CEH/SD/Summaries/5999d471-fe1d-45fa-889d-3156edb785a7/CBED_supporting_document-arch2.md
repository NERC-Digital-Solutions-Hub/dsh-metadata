# Concentration Based Estimated Deposition (CBED) methodology

## What CBED does
- Produces 5x5 km resolution gridded estimates of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Deposition is derived from measured concentrations of gases/particulates in air and ions in precipitation, using data from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.

## How data are produced
- Site measurements are interpolated to create UK concentration maps.
- Wet deposition is computed by combining precipitation data with precipitation-ion concentrations and including cloud (occult) deposition to vegetation.
- Dry deposition uses gas/PM concentration maps and habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
- Deposition to land-cover categories is blended within each 5x5 km grid cell; for critical loads, moorland values apply to non-woodland habitats and forest values to woodland habitats.

## Data inputs and model components
- Nitrogen species: NO2/NO3 via interpolation from ~30 sites; NO2/NO3 and SO2 from the Pollution Concentration Mapping (PCM) model.
- Ammonia: from FRAME atmospheric transport model plus annual UKEAP measurements (FRAME provides local variability; 2017 emissions were used in FRAME).
- Wet deposition includes sulphate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion).
- Orographic enhancement is applied to upland precipitation to reflect seeder-feeder effects; based on Great Dun Fell and Holme Moss observations.

## Temporal aspects
- Deposition is calculated annually but is presented as rolling 3-year means to smooth inter-annual variability due to weather and climate factors.
- Outputs are ecosystem-specific with two scenarios (moorland/short vegetation everywhere; forest everywhere) and grid-average results.

## Data structure and formats
- Provides 3-year mean, ecosystem-specific deposition data in three datasets:
  - CBED-deposition-moorland-2016-2018.csv
  - CBED-deposition-forest-2016-2018.csv
  - CBED-deposition-gridaverage-2016-2018.csv
- Common fields: easting (metres), northing (metres), and deposition values for each pollutant form (e.g., nox_m, nhx_m, nms_m, ca_mg_m for moorland; corresponding forest fields; ga for grid average).
- Grid-average file includes fewer mapped grid squares when all nitrogen forms are not present.

## Calculation details and land cover mixing
- Dry deposition totals per grid square are computed by weighting the five land-cover deposition values by the local land-cover proportions in each 5x5 km cell.
- Moorland deposition is applied to non-woodland habitats; forest deposition to woodland habitats.

## Units, conversions, and interpretation
- All deposition values are in keq ha^-1 year^-1.
- Conversions to standard mass units:
  - Sulphur deposition: keq ha^-1 year^-1 × 16 = kg S ha^-1 year^-1
  - Oxidised/reduced nitrogen deposition: keq ha^-1 year^-1 × 14 = kg N ha^-1 year^-1
  - Base cation deposition (Ca+Mg): keq ha^-1 year^-1 × 20 = kg Ca ha^-1 year^-1

## Quality control and validation
- Methods align with government QA practices for analytical models.
- CBED undergoes extensive peer review and participated in Defra model inter-comparison exercises.
- Version control, documentation, and central storage of code; mass-balance checks and cross-year consistency checks are routinely performed.

## Data accessibility and usage
- CBED results are stored and uploaded to appropriate data portals.
- Data rely on inputs from UKEAP, PCM, and FRAME models, with supporting literature and monitoring datasets referenced in the methodology.