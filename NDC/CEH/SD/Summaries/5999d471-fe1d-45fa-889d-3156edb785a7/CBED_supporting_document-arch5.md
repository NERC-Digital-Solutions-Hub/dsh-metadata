# Concentration Based Estimated Deposition (CBED) methodology

- Generates 5x5 km resolution gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Based on measured gas/particulate concentrations in air and measured ion concentrations in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Data are produced for the UK and used for assessments such as critical load exceedance.

## Data sources and deposition modelling

- Site measurements from the UKEAP network are interpolated to create UK-wide concentration maps.
- Wet deposition combines precipitation concentrations with annual precipitation maps from the UK Met Office, including direct cloud deposition (occult deposition) to vegetation.
- Dry deposition uses gas and PM deposition estimates with habitat-specific deposition velocities across five land cover categories: forest, moorland, grassland, arable, and urban; deposition to non-woodland habitats uses moorland values, while woodland habitats use forest values.
- Nitric acid concentrations are interpolated from ~30 sites; NO2 and SO2 concentrations come from the PCM model (interpolated rural measurements plus point/line source modelling).
- Ammonia concentrations come from FRAME (with 2017 emissions) plus annual UKEAP measurements to capture local variability.
- Wet deposition includes an orographic enhancement factor for upland regions due to the seeder-feeder effect.
- Inter-annual variability exists due to weather and atmospheric processes; CBED deposition estimates used for critical loads are averaged over a three-year period to smooth variability.

## Temporal scope and data outputs

- Depositions are calculated annually but provided as rolling 3-year means to reduce year-to-year variability.
- Ecosystem-specific outputs: 
  - Moorland deposition values
  - Forest/woodland deposition values
  - Grid-average deposition values (aggregated across land covers)
- Data are provided as 3-year means for 2016–2018 (for the corresponding files).

## Data structure and files

- Three ecosystem-specific datasets and one grid-average dataset:
  - CBED-deposition-moorland-2016-2018.csv
  - CBED-deposition-forest-2016-2018.csv
  - CBED-deposition-gridaverage-2016-2018.csv
- Common fields:
  - easting: centre of 5x5 km grid square (metres)
  - northing: centre of 5x5 km grid square (metres)
  - deposition components (keq ha-1 year-1):
    - Moorland: nox_m (oxidised nitrogen), nhx_m (reduced nitrogen), nms_m (non-marine sulphur), ca_mg_m (base cations)
    - Forest: nox_f, nhx_f, nms_f, ca_mg_f
    - Grid average: nox_ga, nhx_ga, nms_ga, ca_mg_ga
- Grid-average dataset contains fewer rows (10678) than the forest/moorland datasets (11172) because a complete set of nitrogen forms is required for the grid average.
- All datasets express deposition in keq ha-1 year-1.

## Units and conversions

- Deposition values are in kilo-equivalents per hectare per year (keq ha-1 year-1).
- Conversions to common mass units:
  - Sulphur deposition: multiply by 16 to convert keq ha-1 year-1 to kg S ha-1 year-1
  - Oxidised/reduced nitrogen deposition: multiply by 14 to convert keq ha-1 year-1 to kg N ha-1 year-1
  - Base cations (Ca+Mg) deposition: multiply by 20 to convert keq ha-1 year-1 to kg Ca ha-1 year-1

## Quality control and governance

- CBED methods follow QA procedures aligned with Government analytical model QA (peer reviewed and part of Defra model inter-comparison exercises).
- Version control: method developments are documented, numbered, and stored in a central file system; model updates require approval by senior responsible officers.
- Deposition results are extensively published in peer-reviewed literature; mass-balance checks are routinely performed to ensure numerical consistency and check against previous years.

## Data availability, access, and provenance

- Supporting information and data are accessible via:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
- Data are organized as 3-year mean ecosystem-specific deposition data (moorland, forest, grid average) across 5x5 km grid squares in the UK, with documentation on data structure, units, and file naming.

## Additional notes for data governance

- The CBED outputs rely on multiple models and measurements (FRAME for ammonia; PCM for NO2/SO2; interpolation from primary measurements; precipitation maps; orographic enhancement) and therefore require clear provenance and methodological transparency for reuse.
- Practical considerations for data stewards:
  - Ensure metadata captures data sources, modelling steps, temporal window (rolling 3-year means), and grid mapping specifics.
  - Track dataset versions and file naming conventions for reproducibility.
  - Maintain links to underlying models and measurement campaigns referenced (e.g., FRAME, PCM, Holme Moss, Great Dun Fell) to support audit trails and user understanding.
  - Provide guidance on unit conversions (keq to kg) to support consistent interpretation and interoperability with other datasets.