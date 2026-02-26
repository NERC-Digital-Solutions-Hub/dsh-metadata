# Frame Modelling

- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model for estimating annual mean deposition of reduced and oxidised nitrogen and sulphur over the UK.
- Domain and resolution: British Isles domain with a 5 km grid (172 x 144 grid cells).
- Emissions inputs: UK National Atmospheric Emissions Inventory (NAEI) with 160 sub-sector categories, including 22 point sources and background area emissions split into 11 SNAP sectors, plus international shipping and European emissions.
- Ammonia inputs: from NARSES model (5 sectors) to represent agricultural and non-agricultural sources, including waste sector contributions.

- Regional attribution: Emissions are regionalised by country (England, Scotland, Wales, Northern Ireland) to help regulators understand source locations affecting sites.

- Emissions and sources (highlights):
  - Top 22 point sources: power stations, refineries, steel works, etc.
  - Distinction between sulfur (SOx), nitrogen (NOy, NHx) species and their deposition.
  - Separate treatment for international shipping and European imports.

- Model runs and footprints:
  - Base run includes all sources; subsequent runs abate each source individually (25% reduction per run to reduce non-linearities), then footprints are calculated as the difference from the baseline.
  - Final footprints are scaled by a factor of 4.
  - Footprint for a source i is FP(id=n) = DEP(id=0) – DEP(id=n), with DEP being FRAME-deposited data.
  - Outputs include deposition for SOx, NOy, NHx in 5 km grid squares, plus splits into short-range and long-range contributions.

- Deposition splits and habitat context:
  - Output includes detailed short/long-range splits for each species (e.g., NH3, NH4+, HNO3, NO3-, NO2, SO2, SO4) and separate outputs for three ecosystem types: forest, moorland, and grid average (reflecting surface roughness and deposition velocity differences).
  - Forests and moorland have higher deposition for ammonia due to lower canopy resistance; agricultural fields show lower deposition velocities.

- Post-processing and calibration:
  - Normalisation: individual source footprints are normalised so their sum matches the baseline total, mitigating model non-linearities.
  - Calibration to CBED: FRAME results are calibrated against the Concentration Based Estimated Deposition (CBED) dataset for 2011–2013 to align modelled deposition with measurements, using:
    - DEP(CAL,2012) = DEP(UNC,2012) × (DEP(CBED,2011–2013) / DEP(UNC,2012))
  - Calibration can also be applied to footprints using a similar approach to ensure calibrated footprints sum to official CBED totals for 2012.

- Spatial mapping to UK protected sites:
  - FRAME outputs 160 footprint files per pollutant/footprint type; these are aggregated to 90 footprints to speed processing.
  - Python-based workflow merges the 90 footprints with a protected sites shapefile (SAC, SPA, SSSI) to compute, per site, minimum, maximum, and grid-average deposition for each pollutant and footprint type.
  - Grid-average deposition is area-weighted by site area; results are produced for forest, moorland, and grid-average scenarios.

- Units and interpretation:
  - Deposition values are in kilo-equivalents per hectare per year (keq ha^-1 yr^-1).
  - Conversion to kilograms per hectare per year:
    - Sulphur: keq ha^-1 yr^-1 × 16 = kg S ha^-1 yr^-1
    - Nitrogen: keq ha^-1 yr^-1 × 14 = kg N ha^-1 yr^-1
  - Total nitrogen deposition is the sum of NO2 + NO3 and NH3 + NH4.

- Quality control:
  - Normalisation ensures the sum of footprints equals the baseline, reducing potential attribution errors.
  - National budgets of total deposition are checked against previous years.
  - Each footprint output is produced as a JPG to aid error detection.

- Data structure and content (datasets):
  - Datasets 1–3: Three-year mean (2013–2015) attribution and deposition data, at 5 x 5 km resolution, for three ecosystem types (forest, moorland, grid average), summarized as minimum, maximum, and area-weighted values per site (SAC/SPA/SSSI).
  - Example filenames: APIS_source_attribution_nitrogen_sulphur_to_forest_bysite.csv, APIS_source_attribution_nitrogen_sulphur_to_moorland_bysite.csv, APIS_source_attribution_nitrogen_sulphur_to_gridaverage_bysite.csv.
  - Site-level fields include SITECODE, SITENAME, grid coordinates (X, Y), SITE_AREA, COUNTRY, DESIGNATION, FOOTPRINT_ID/NAME, AREA_POINT, SOURCE_LOCATION, and deposition values for multiple components (e.g., SOD/SOW/NOD/NOW/NHD/NHW) across local (short-range) and long-range categories, for both forest and moorland, and grid average.
  - Each row represents a site footprint attribution for a given deposition component, with area-weighted, minimum, and maximum values.