# Frame Modelling

- Purpose and domain
  - FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to estimate annual mean deposition of reduced and oxidised nitrogen and sulphur over the United Kingdom.
  - Domain covers the British Isles on a 5 km grid (172 x 144).

- Emissions and input data
  - Emissions for input come from the UK National Atmospheric Emissions Inventory (NAEI), split into 160 sub-sectoral categories.
  - Includes 22 major point sources and background 'area' emissions of SO2, NOx, and NH3 across 11 SNAP sectors; accounts for international shipping and European emissions.
  - Ammonia inputs synthesized from NARSES with 5 sectors (livestock, fertiliser, non-agricultural abatable/non-abatable sources, waste sector).
  - Regional land masks separate sources by England, Scotland, Wales, and Northern Ireland for regulator clarity.

- Model runs and footprint calculation
  - FRAME run performed for a base scenario (all sources) and then repeated with each emission source abated.
  - A 25% emissions reduction is applied to each source to minimize non-linear atmospheric chemistry effects; final footprints are scaled by a factor of 4.
  - Footprint for a given source is derived from the difference between the base deposition and the deposition with the source abated: FP(id=n) = DEP(id=0) − DEP(id=n).
  - For every 5 km grid square, deposition of SOx, NOy, and NHx is computed for all footprints, with a detailed short/long-range source attribution (short/long range split across 11 categories) and three habitat types.

- Spatial detail and habitat considerations
  - Output includes deposition by three ecosystem types: forest, moorland, and grid average (averaged over arable, grassland, urban, forest, and moorland) to reflect surface roughness effects on deposition velocity.
  - Noted that dry deposition of ammonia is higher to forests/moorland due to canopy resistance; ammonia deposition to agricultural fields is lower.

- Post-processing and calibration
  - Footprints are normalised so the sum matches the baseline deposition to account for model non-linearities.
  - Calibration uses CBED (Concentration Based Estimated Deposition) data for 2011–2013 to provide a more robust annual average deposition.
  - Calibration equations adjust both grid-based deposition and footprints to align with official CBED totals for 2012, ensuring consistency.

- Spatial mapping to UK protected sites
  - FRAME outputs consist of 160 footprint files per footprint type and pollutant; these are aggregated to 90 footprint files to speed processing.
  - Python is used to merge footprint data with a gridded UK protected site shapefile (SAC, SPA, SSSI) to produce site-specific deposition data.
  - For each site, min, max, and grid-average deposition values are computed for forest, moorland, and grid-average outputs using area-weighting across grid squares.

- Data outputs and structure
  - Outputs three datasets for deposition and attribution:
    - Dataset 1-3: 3-year mean (2013–2015) source attribution and deposition by site, for nitrogen and sulphur, at 5 x 5 km resolution with min, max, and area-weighted values.
    - Forest-focused: APIS_source_attribution_nitrogen_sulphur_to_forest_bysite.csv
    - Moorland-focused: APIS_source_attribution_nitrogen_sulphur_to_moorland_bysite.csv
    - Grid-average: APIS_source_attribution_nitrogen_sulphur_to_gridaverage_bysite.csv
  - File contents include site identifiers, coordinates, country, designation, footprint details, and deposition values broken down into local (short-range) and long-range components for each pollutant and habitat.
  - Recorded values are expressed as kilo-equivalents per hectare per year (keq ha^-1 year^-1) with conversions to kilograms per hectare per year provided (multiply by 16 for sulphur, 14 for nitrogen).
  - Total nitrogen deposition can be derived by summing NO2/NO3 and NH3/NH4 components.
  - Additional quality controls include exporting each footprint as a jpg for error checking and cross-year budget checks against previous results.

- Quality control
  - Normalisation of footprints to match baseline sums.
  - National budgets of total deposition cross-checked against previous years.
  - Individual footprint outputs produced as images (jpg) to aid error detection.

- Notes on data structure and access
  - Datasets are delivered as 3-year means (2013–2015) for each habitat type (forest, moorland, grid average) and by site for SAC, SPA, and SSSI.
  - Data are provided at a 5 km x 5 km grid resolution with site-level summaries and numerous fields describing site, footprint, and deposition values.