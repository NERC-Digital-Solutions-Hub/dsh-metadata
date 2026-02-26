# Methods

- Purpose
  - Describe the Concentration Based Estimated Deposition (CBED) methodology used to generate 5x5 km gridded deposition data for sulfur, nitrogen (oxidised and reduced), and base cations from air concentrations and precipitation data.

- Data sources
  - Measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
  - Interpolated site data to UK concentration maps.
  - Wet deposition derived by combining precipitation data with precipitation chemistry and cloud/occult deposition.
  - Dry deposition derived from gas/PM concentrations and habitat-specific deposition velocities.

- Deposition components and habitats
  - Dry deposition: includes sulfur dioxide (SO2), nitric acid (HNO3), nitrogen dioxide (NO2), ammonia (NH3), and particulate matter to vegetation.
  - Land cover categories used for dry deposition: forest, moorland, grassland, arable, urban.
  - Critical load calculations apply moorland values to non-woodland habitats and forest values to woodland habitats.

- Temporal and spatial aggregation
  - Data are annual but provided as rolling 3-year means to smooth inter-annual variability.
  - Ecosystem-specific outputs: moorland-only, forest-only, and grid-average across each 5x5 km grid square.
  - Inter-annual variability influenced by weather patterns; 3-year window recommended for stability.

- Data products (outputs and formats)
  - Three 2014–2016 3-year mean deposition datasets:
    - CBED-deposition-moorland-2014-2016.csv
    - CBED-deposition-forest-2014-2016.csv
    - CBED-deposition-gridaverage-2014-2016.csv
  - Each file includes:
    - easting and northing (grid center coordinates in metres)
    - deposition values in keq ha-1 year-1 for the relevant category (nox for oxidised N, nhx for reduced N, nms for non-marine sulfur, nm_ca_mg for non-marine base cations)
  - Specific column codes per file:
    - Moorland: nox_m, nhx_m, nms_m, nm_ca_mg_m
    - Forest: nox_f, nhx_f, nms_f, nm_ca_mg_f
    - Grid average: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga

- Data structure and unit details
  - All deposition values expressed as keq ha-1 year-1.
  - Conversion to kilograms per hectare per year:
    - SOx and nitrogen conversions: keq ha-1 year-1 × 16 (kg S) or ×14 (kg N)
    - Base cations: keq ha-1 year-1 × 20 (kg Ca)
  - Documented in the dataset with guidance for converting to standard units.

- Data quality and provenance
  - Methods and results have undergone extensive peer review and participation in Defra model inter-comparison (e.g., Carslaw 2011).
  - Documentation practices include version control, central storage of code, and mass-balance checks for numerical consistency.
  - Outputs widely published in peer-reviewed literature.

- Accessibility and references
  - Supporting information and network details available via:
    - http://www.pollutantdeposition.ceh.ac.uk/ukeap
    - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
  - Data context and methods referenced in multiple peer-reviewed sources (e.g., Beswick et al., Dore et al., Fowler et al., Stedman et al.).

- Additional notes
  - Fieldwork and/or laboratory instrumentation: N/A
  - Calibration steps and values: N/A
  - Nature and units of recorded values clearly stated; data are designed to support deposition and impact assessments, including exceedance analyses for critical loads.