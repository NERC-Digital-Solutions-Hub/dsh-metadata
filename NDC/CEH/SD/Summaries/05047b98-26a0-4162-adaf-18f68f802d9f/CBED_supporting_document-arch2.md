# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Produces 5x5 km gridded data of wet and dry deposition for sulphur, oxidised nitrogen, reduced nitrogen, and base cations.
- Derived from measured gas/PM concentrations in air and ion concentrations in precipitation, collected via the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Interpolates site measurements to UK concentration maps and combines with precipitation and land-cover-specific deposition processes to estimate grid-average deposition.

## How deposition is calculated
- Wet deposition
  - Combines precipitation maps with ion concentrations in precipitation to estimate wet deposition.
  - Includes direct deposition of cloud droplets to vegetation (occult deposition).
  - Separates anthropogenic (non-seasalt) and total components using sea-salt relationships.
  - Applies an orographic enhancement factor for upland regions (seeder-feeder effect).
- Dry deposition
  - Uses gas and PM concentration maps plus habitat-specific deposition velocities for five land cover categories: forest, moorland, grassland, arable, urban.
  - Deposition to each land cover category is weighted by its proportion within each 5x5 km grid square to yield grid-average values.
  - For critical-load calculations, moorland deposition is applied to non-woodland habitats, and forest deposition to woodland habitats.
- Pollutant specifics
  - Dry deposition includes SO2, HNO3, NO2, NH3, and particulate matter (sulphate, nitrate, ammonium, calcium, magnesium).

## Temporal and ecosystem outputs
- Inter-annual variability acknowledged; deposition can vary with weather patterns.
- Values are averaged over a 3-year period to smooth variability.
- Outputs are provided as annual calculations but reported as rolling 3-year means.
- Ecosystem-specific outputs:
  - Moorland deposition
  - Forest/woodland deposition
  - Grid-average deposition
- Two ecosystem-assumption scenarios are supplied:
  - Moorland everywhere
  - Forest everywhere

## Data structure and formats
- 3-year mean, ecosystem-specific deposition data for 2014–2016 (example filenames):
  - CBED-deposition-moorland-2014-2016.csv
  - CBED-deposition-forest-2014-2016.csv
  - CBED-deposition-gridaverage-2014-2016.csv
- Common fields per file:
  - easting: centre of 5x5 km grid square (metres)
  - northing: centre of 5x5 km grid square (metres)
  - Deposition values (keq ha-1 year-1):
    - nox (oxidised nitrogen) for the relevant ecosystem
    - nhx (reduced nitrogen) for the relevant ecosystem
    - nms (non-marine sulphur) for the relevant ecosystem
    - nm_ca (non-marine base cations; Ca+Mg) for the relevant ecosystem
- Units and conversions
  - All deposition values are keq ha-1 year-1.
  - Convert to kg per ha per year:
    - Sulphur: keq × 16 = kg S ha-1 year-1
    - Nitrogen (oxidised/reduced): keq × 14 = kg N ha-1 year-1
    - Base cations: keq × 20 = kg Ca ha-1 year-1
- Data availability formats include explicit documentation of fields and grid references.

## Data quality and validation
- Methods align with QA procedures for government analytical models and have undergone extensive peer review.
- Participated in Defra model inter-comparison exercises and documented in related literature.
- Includes: version control, documentation of method developments, mass-balance checks, and comparisons to previous years.

## Access, sources, and documentation
- Data and supporting information available via:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
- Fieldwork and laboratory instrumentation: not applicable (N/A)
- Calibration steps and values: N/A

## Relevance for environmental analysts
- Provides standardized, reproducible, and time-aggregated deposition data suitable for monitoring environmental health and policy performance over time.
- Facilitates comparisons across ecosystems (moorland vs forest) and spatially across the UK.
- Enables integration with other datasets to enhance interpretation and policy assessment, addressing needs to increase dataset value and improve data accessibility.