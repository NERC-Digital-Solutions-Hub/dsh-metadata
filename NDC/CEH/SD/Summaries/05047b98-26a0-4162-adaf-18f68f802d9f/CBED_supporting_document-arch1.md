# Methods

- The Concentration Based Estimated Deposition (CBED) methodology creates 5x5 km gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations, derived from measured gas/particle concentrations and precipitation-derived ion concentrations at UK sites within the UKEAP network.
- Wet deposition: combines precipitation concentrations with an annual precipitation map; accounts for occult deposition (direct deposition of cloud droplets) and uses an orographic enhancement factor to reflect upland precipitation effects.
- Dry deposition: uses concentration maps of gases/PM and habitat-specific deposition velocities to generate deposition for five land cover categories (forest, moorland, grassland, arable, urban). For the critical load calculations, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.

- Data sources and models:
  - Gas/PM concentration maps for oxidised nitrogen, reduced nitrogen, sulphur, and base cations.
  - Ammonia concentrations from FRAME model and UKEAP measurements; NO2 from PCM model; sulphur/sea-salt separations using sodium-based ratios.
  - NO2/NO3 and nitric acid interpolations; ammonium/nitrate from observed data and models; sulphur from SO2 and non-marine components separated via sea-salt proxies.
  - Interannual variability driven by weather and atmospheric transport; CBED values are averaged to three-year periods to smooth fluctuations.

- Temporal and ecosystem specificity:
  - Deposition values are calculated annually but provided as rolling 3-year means.
  - Two ecosystem-specific datasets are provided: moorland everywhere and forest everywhere.
  - A grid-average dataset is also provided (grid average across all habitats).

- Data products and structure:
  - Three main CSV datasets (2014–2016 rolling means):
    - CBED-deposition-moorland-2014-2016.csv: deposition to moorland (keq ha-1 y-1) for oxidised nitrogen (nox_m), reduced nitrogen (nhx_m), non-marine sulphur (nms_m), non-marine base cations (nm_ca_mg_m); plus easting/northing positions.
    - CBED-deposition-forest-2014-2016.csv: deposition to forest (keq ha-1 y-1) for the same components (nox_f, nhx_f, nms_f, nm_ca_mg_f) and positions.
    - CBED-deposition-gridaverage-2014-2016.csv: grid-average deposition (keq ha-1 y-1) for oxidised nitrogen (nox_ga), reduced nitrogen (nhx_ga), non-marine sulphur (nms_ga), non-marine base cations (nm_ca_mg_ga) and positions.
  - Each file includes easting and northing (metres) for the centre of each 5x5 km grid square.

- Units and conversions:
  - Deposition values are in keq ha-1 year-1.
  - Conversions to kilograms per hectare per year:
    - Sulphur (S): keq ha-1 year-1 × 16 = kg S ha-1 year-1
    - Oxidised/reduced nitrogen (N): keq ha-1 year-1 × 14 = kg N ha-1 year-1
    - Base cations (Ca+Mg): keq ha-1 year-1 × 20 = kg Ca ha-1 year-1

- Quality assurance and provenance:
  - CBED methods align with government QA practices; extensive peer review and participation in Defra model inter-comparison.
  - Version control, documentation, and mass-balance checks ensure numerical consistency with prior years.
  - Results and method developments are published in peer-reviewed literature and managed by senior responsible officers.

- Data access and references:
  - Primary information and supporting materials are provided via the UK pollutant deposition resources and related Defra/UK-AIR portals.
  - Key references underpinning the methodology include works by Carslaw, Dore, Sutton, Fowler, Stedman, Singles, and RoTAP reports, among others.