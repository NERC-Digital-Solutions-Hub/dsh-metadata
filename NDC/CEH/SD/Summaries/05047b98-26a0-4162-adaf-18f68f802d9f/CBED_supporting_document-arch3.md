# UK Acidifying and Eutrophying Atmospheric Pollutants

## Purpose and scope
- Presents the Concentration Based Estimated Deposition (CBED) methodology to produce 5x5 km gridded annual deposition data for wet and dry deposition of sulphur, oxidised nitrogen, reduced nitrogen, and base cations.
- Data are derived from air concentrations, precipitation ion concentrations, and land-cover weighted deposition processes, to support assessment of critical load exceedance.

## Methodology overview
- Site measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network are interpolated to generate UK-wide concentration maps.
- Wet deposition:
  - Combines precipitation deposition with occult (cloud) deposition to vegetation.
  - Uses an annual precipitation map and an orographic enhancement factor for upland regions.
  - Separates anthropogenic and total components for certain species via ion ratios relative to seawater.
- Dry deposition:
  - Uses gas and PM concentrations with habitat-specific deposition velocities.
  - Deposits are allocated to five land-cover categories: forest, moorland, grassland, arable, urban.
  - For critical loads, deposition values for moorland are applied to non-woodland habitats and forest values to woodland habitats.
- Specific inputs:
  - Sulphur: SO2 concentration from rural measurements with urban enhancement.
  - Oxidised nitrogen: nitric acid interpolated from ~30 sites; NO2 from the PCM model (rural plus point/line sources).
  - Ammonia: combination of the FRAME model and annual UKEAP measurements.
- Temporal context:
  - Inter-annual variations due to weather and atmospheric processes acknowledged.
  - Deposition values averaged over a 3-year period to smooth variability; results provided as rolling 3-year means.

## Data products and structure
- Outputs are ecosystem-specific 3-year means with two scenarios plus a grid-average:
  - Moorland-specific deposition (nox_m, nhx_m, nms_m, nm_ca_mg_m)
  - Forest/woodland-specific deposition (nox_f, nhx_f, nms_f, nm_ca_mg_f)
  - Grid-average deposition (nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga)
- Data are provided for each 5x5 km grid square with:
  - easting and northing (centre coordinates in metres)
  - deposition components expressed as keq ha^-1 year^-1
- Three CSV files per period (2014–2016):
  - CBED-deposition-moorland-2014-2016.csv
  - CBED-deposition-forest-2014-2016.csv
  - CBED-deposition-gridaverage-2014-2016.csv
- Unit conversions and interpretation:
  - 1 keq ha^-1 year^-1 can be converted to kg S ha^-1 year^-1 by multiplying by 16 (for sulphur).
  - 1 keq ha^-1 year^-1 can be converted to kg N ha^-1 year^-1 by multiplying by 14 (for nitrogen).
  - 1 keq ha^-1 year^-1 for base cations (Ca+Mg) corresponds to kg Ca ha^-1 year^-1 by multiplying by 20.

## Temporal and spatial considerations
- Values are calculated annually but reported as rolling 3-year means to smooth inter-annual variability.
- Outputs are provided as grid-specific values and as grid-average values, under two ecosystem-assumption scenarios (moorland vs forest) and a grid-wide average.

## Data sources, inputs, and modelling components
- Ground measurements:
  - UKEAP network data for calibration and validation.
- Modelling components:
  - NO2 and oxidised nitrogen: PCM model, rural measurements, and interpolation.
  - Ammonia: FRAME model plus measured UKEAP data for local variability.
- Wet deposition components:
  - Occult deposition (cloud interception) and precipitation-based deposition.
  - Orographic enhancement factor for upland precipitation concentrations.
- Deposition separation:
  - Anthropogenic vs total deposition components estimated using sea-salt proxies for sulphur and calcium.

## Quality assurance and governance
- Methods align with official QA practices for government analytical models.
- CBED data and calculations subjected to extensive peer review and participate in Defra model inter-comparison exercises.
- Version control, central storage, and documentation procedures in place; mass-balance checks ensure numerical consistency; results published in peer-reviewed literature.

## Metadata, documentation, and accessibility
- Data structured with explicit field names, units, and descriptions for reproducibility.
- Detailed documentation accompanies the datasets, including data structure and field definitions (easting, northing, deposition components, and units).

## Implications for monitoring frameworks
- Demonstrates an end-to-end workflow from site measurements to gridded deposition estimates suitable for policy evaluation and critical-load exceedance analyses.
- Shows integration of multiple data streams (air concentrations, precipitation chemistry, and land-cover routing) with explicit uncertainty and inter-annual variability considerations.
- Provides clear data governance practices, metadata, and reproducible file formats to facilitate transparency and reuse in monitoring programs.