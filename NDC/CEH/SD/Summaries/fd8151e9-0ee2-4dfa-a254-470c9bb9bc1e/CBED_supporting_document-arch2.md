# Methods

- Purpose and scope
  - The Concentration Based Estimated Deposition (CBED) methodology generates 5x5 km resolution gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
  - Deposition is derived from measured concentrations of gases, particulate matter in air, and ions in precipitation, using data from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
  - Outputs support assessment of environmental health and policy performance over time.

- Data sources and processing
  - Site measurements from UKEAP are interpolated to produce UK-wide concentration maps.
  - Wet deposition is calculated by combining precipitation concentration maps with an annual precipitation map from the UK Met Office.
  - Dry deposition is derived by combining gas/PM concentration maps with habitat-specific deposition velocities across five land-cover categories: forest, moorland, grassland, arable, and urban.
  - Deposition to land-cover categories is weighted by their proportions within each 5x5 km grid cell to yield grid-square averaged deposition.
  - Critical load calculations apply moorland deposition to all non-woodland habitats and forest deposition to woodland habitats.

- Components and data sources
  - Sulphur dioxide (SO2) concentrations are from rural measurements with an urban enhancement factor.
  - Oxidised nitrogen dry deposition uses interpolated nitric acid concentrations; NO2 concentrations come from the Pollution Concentration Mapping (PCM) model.
  - Ammonia concentrations are from FRAME (atmospheric chemical transport model) plus annual UKEAP measurements.
  - Wet deposition includes both precipitation deposition and occult deposition (direct deposition of cloud droplets) for sulphate, ammonium, nitrate, calcium, magnesium, and acidity (H+).
  - Anthropogenic vs total components for sulphur and calcium are separated using sea-salt ion ratios (relative to sodium).

- Orographic and temporal considerations
  - An orographic enhancement factor accounts for upland precipitation concentration (seeder–feeder effect), based on observations from Great Dun Fell and Holme Moss.
  - Inter-annual variability (weather, emissions, chemistry, transport) is acknowledged; deposition values are averaged over a three-year period to smooth variability.
  - CBED data are produced as annual values but supplied as rolling 3-year means; ecosystem-specific outputs include “moorland everywhere” and “forest everywhere” assumptions, plus grid-average values.

- Temporal and ecosystem data outputs
  - 3-year mean deposition data are provided for three ecosystem specifications: moorland, forest/woodland, and grid average.
  - Examples of data files (2013–2015):
    - CBED-deposition-moorland-2013-2015.csv
    - CBED-deposition-forest-2013-2015.csv
    - CBED-deposition-gridaverage-2013-2015.csv
  - Each file includes:
    - easting and northing (centre of the 5x5 km grid square)
    - deposition values for specific components (in keq ha-1 year-1):
      - Moorland: nox_m (oxidised nitrogen), nhx_m (reduced nitrogen), nms_m (non-marine sulphur), nm_ca_mg_m (non-marine base cations)
      - Forest: nox_f, nhx_f, nms_f, nm_ca_mg_f
      - Grid average: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga

- Units and data interpretation
  - All deposition values are expressed as kilo-equivalents per hectare per year (keq ha-1 year-1).
  - Conversions:
    - Sulphur deposition to kg S ha-1 year-1: keq ha-1 year-1 × 16
    - Oxidised/reduced nitrogen deposition to kg N ha-1 year-1: keq ha-1 year-1 × 14
    - Non-marine base cations (Ca+Mg) deposition to kg Ca ha-1 year-1: keq ha-1 year-1 × 20

- Quality control and transparency
  - Methods align with QA standards for government analytical models; extensive peer review and participation in Defra model inter-comparison (Carslaw 2011).
  - Version control, central storage, and documentation of method developments; mass-balance checks against previous years.
  - Deposition results are published in peer-reviewed literature and supported by multiple source documents and models.

- Access and supporting information
  - Primary information and supporting materials:
    - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) data portal: http://www.pollutantdeposition.ceh.ac.uk/ukeap
    - UK-Air Defra network information on UKEAP: https://uk-air.defra.gov.uk/networks/network-info?view=ukeap

- Fieldwork and calibration
  - Fieldwork/lab instrumentation: not applicable (N/A) for these method descriptions.
  - Calibration steps and values: not applicable (N/A) for these method descriptions.