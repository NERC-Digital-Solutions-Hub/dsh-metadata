# Methods

- Purpose and output
  - CBED (Concentration Based Estimated Deposition) generates 5x5 km resolution gridded data for wet and dry deposition of sulfur, oxidised and reduced nitrogen, and base cations.
  - Based on measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network; data are prepared for ecosystem-level deposition assessments and critical load exceedance analyses.

- Data construction process
  - Site-based measurements are interpolated to create UK-wide concentration maps.
  - Wet deposition: combine ion concentrations in precipitation with an annual precipitation map to produce deposition values.
  - Dry deposition: combine gas/particulate concentration maps with habitat-specific deposition velocities across five land cover types (forest, moorland, grassland, arable, urban).
  - Deposition to 5 land cover categories is weighted by their proportions within each 5x5 km grid square.
  - For critical loads, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.

- Temporal and ecosystem considerations
  - Annual calculations, but deposition values are averaged over a rolling 3-year period to smooth inter-annual variability.
  - Outputs include two ecosystem-specific sets per grid cell: moorland/short vegetation everywhere and forest/everywhere, plus a grid-average.

- Key data components and modeling details
  - SO2 concentrations use rural measurements with an urban enhancement factor.
  - Oxidised nitrogen dry deposition uses interpolated nitric acid data and NO2 from the PCM model.
  - Ammonia deposition combines FRAME model outputs with UKEAP measurements for local variability.
  - Wet deposition includes direct cloud deposition to vegetation (occult deposition) and separated anthropogenic vs total components using sea-salt ratios; an orographic enhancement factor accounts for upland precipitation patterns.

- Data structure and files
  - CBED-deposition-moorland-2013-2015.csv: easting, northing, and moorland deposition components for oxidised nitrogen (nox_m), reduced nitrogen (nhx_m), non-marine sulphur (nms_m), non-marine base cations (nm_ca_mg_m).
  - CBED-deposition-forest-2013-2015.csv: easting, northing, and forest deposition components for oxidised nitrogen (nox_f), reduced nitrogen (nhx_f), non-marine sulphur (nms_f), non-marine base cations (nm_ca_mg_f).
  - CBED-deposition-gridaverage-2013-2015.csv: easting, northing, and grid-average deposition components for oxidised nitrogen (nox_ga), reduced nitrogen (nhx_ga), non-marine sulphur (nms_ga), non-marine base cations (nm_ca_mg_ga).

- Units and conversions
  - All deposition values are in keq ha-1 year-1.
  - Conversions to common units:
    - Sulfur deposition (keq → kg S): multiply by 16.
    - Oxidised/reduced nitrogen deposition (keq → kg N): multiply by 14.
    - Base cations (keq; Ca+Mg) deposition: multiply by 20 to obtain kg Ca ha-1 year-1.

- Quality control and provenance
  - Methods align with government QA practices for analytical models; extensive peer review and participation in Defra model inter-comparison.
  - Documentation, version control, and central storage of code; mass balance checks against previous years.

- Access and references
  - Data and information: 
    - http://www.pollutantdeposition.ceh.ac.uk/ukeap
    - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
  - Fieldwork and calibration notes: not applicable (N/A).