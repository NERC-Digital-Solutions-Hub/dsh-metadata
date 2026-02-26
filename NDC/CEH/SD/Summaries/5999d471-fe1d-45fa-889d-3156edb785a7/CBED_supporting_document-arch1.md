# Methods

- Purpose
  - Produces 5x5 km gridded deposition data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations, derived from gas/particulate air concentrations and precipitation ion concentrations.

- Data sources
  - Measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
  - Nitric acid concentrations interpolated from ~30 sites; NO2 and SO2 from the PCM model; ammonia from FRAME model plus UKEAP measurements.

- Wet and dry deposition modeling
  - Wet deposition: combines ion concentrations in precipitation with annual precipitation maps; includes occult (cloud) deposition to vegetation and an orographic enhancement factor for uplands.
  - Dry deposition: uses gas/PM concentration maps and habitat-specific deposition velocities to generate deposition for five land cover categories (forest, moorland, grassland, arable, urban); dry deposition to vegetation includes SO2, HNO3, NO2, NH3 and sulfate, nitrate, ammonium, calcium, magnesium.

- Habitat and critical-load considerations
  - Deposition to moorland applied to all non-woodland habitats; deposition to forest applied to woodland habitats.

- Temporal framework
  - Inter-annual variability acknowledged; results averaged over a three-year period to smooth fluctuations.
  - Calculations are annual but provided as rolling 3-year means.

- Ecosystem-specific data structure
  - Two ecosystem-specific sets: moorland/short vegetation everywhere and forest/woodland everywhere.
  - Also provided as a grid average across the UK.

- Data files and structure
  - 3-year mean deposition data for:
    - CBED-deposition-moorland-2016-2018.csv
    - CBED-deposition-forest-2016-2018.csv
    - CBED-deposition-gridaverage-2016-2018.csv
  - Grid average file has fewer rows because it requires all nitrogen forms to be present.
  - Each file includes:
    - easting and northing (metres) for grid cell centre
    - deposition columns (e.g., nox_m, nhx_m, nms_m, ca_mg_m for moorland; nox_f, nhx_f, nms_f, ca_mg_f for forest; nox_ga, nhx_ga, nms_ga, ca_mg_ga for grid average)

- Units and conversion
  - Recorded values are in keq ha-1 year-1.
  - Conversions:
    - Sulphur deposition (keq) × 16 = kg S ha-1 year-1
    - Oxidised/reduced nitrogen deposition (keq) × 14 = kg N ha-1 year-1
    - Base cations (Ca+Mg) deposition (keq) × 20 = kg Ca ha-1 year-1

- Quality control and provenance
  - Extensive peer review and inclusion in Defra model inter-comparison (Carslaw 2011).
  - Documentation, versioning, and central repository with metadata.
  - Mass balance checks and consistency comparisons with previous years.
  - Methodologies published in peer-reviewed literature; approvals by senior responsible officers.

- Data access and references
  - Supporting information and networks:
    - URL: http://www.pollutantdeposition.ceh.ac.uk/ukeap
    - URL: https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
  - Key references include Beswick et al. (2003), Dore et al. (2001, 2007), Fournier et al. (2003), Fowler et al. (1988), RoTAP (2012), Singles et al. (1998), Smith et al. (2000), Stedman et al. (2007).