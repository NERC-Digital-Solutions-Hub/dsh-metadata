# Frame Modelling

- Objective and scope
  - FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to estimate the annual mean deposition of reduced and oxidised nitrogen and sulphur over the United Kingdom.
  - Domain covers the British Isles on a 5 km grid (172 x 144).

- Model inputs and emissions data
  - Emissions originate from the UK National Atmospheric Emissions Inventory (NAEI), split into 160 sub-sector categories, including 22 major point sources and background emissions across 11 SNAP sectors, plus international shipping and European imports.
  - Ammonia inputs come from the National Ammonia Reduction Strategy Evaluation System (NARSES), with 5 sectors (e.g., livestock, fertiliser, non-agricultural sources).
  - Regional land masks assign emissions to England, Scotland, Wales, and Northern Ireland for regulators’ clarity.

- Running framework and footprint computation
  - A base scenario (all sources) is run, followed by runs with 25% abatement of each emission source to manage non-linear chemical interactions.
  - Footprints are derived by difference: footprint = baseline deposition − deposition with the source abated.
  - To stabilize results, footprints are scaled by a factor of 4.
  - Outputs cover dry and wet deposition for SOx, NOy, and NHx across all 5 km grid cells, plus a short/long-range attribution to identify short vs. long-range inputs.

- Detailed deposition categorisation and habitats
  - The short/long-range split includes multiple components (e.g., wet/dry NH3, NH4+, HNO3, NO2, SO2, SO4) across short and long-range pathways.
  - Deposition data are produced for three ecosystem types to reflect habitat-dependent deposition:
    - Forests (higher deposition due to roughness)
    - Moorland (representing semi-natural vegetation)
    - Grid average (arable, grassland, urban, forest, moorland)

- Post-processing, calibration and quality control
  - Individual footprints are normalised so their sum matches the baseline to correct potential non-linearities.
  - A calibration step aligns FRAME deposition with the official CBED (Concentration Based Estimated Deposition) dataset (2011–2013 average) to improve year-specific robustness.
  - Calibrated footprints ensure that, when aggregated, they reproduce the official CBED total deposition for 2012.
  - Quality control includes cross-year budget checks and producing a JPG per footprint to aid error detection.

- Spatial mapping to UK protected sites
  - FRAME outputs consist of 160 files per footprint type per pollutant; these are aggregated to 90 footprint files for processing efficiency.
  - Python scripts merge footprint data with a gridded UK protected-site shapefile (SAC, SPA, SSSI) to compute:
    - Minimum, maximum, and grid-average deposition for each site and pollutant.
    - Separate outputs for forest, moorland, and grid-average deposition.
  - Site-level deposition calculations account for site area and footprint contributions (area-weighted sums).

- Nature, units, and interpretation of results
  - Deposition values are expressed as kilo-equivalents per hectare per year (keq ha−1 y−1).
  - Conversion to conventional units:
    - Sulphur deposition: keq ha−1 y−1 × 16 = kg S ha−1 y−1
    - Nitrogen deposition: keq ha−1 y−1 × 14 = kg N ha−1 y−1
  - Total nitrogen deposition is the sum of NO2/NO3 and NH3/NH4 contributions.

- Data structure and datasets
  - Datasets 1–3 provide three-year means (2013–2015) of ecosystem-specific source attribution and deposition for nitrogen and sulfur, with:
    - Minimum, maximum, and area-weighted values at each site (SAC, SPA, SSSI) and for habitats ‘moorland’, ‘forest/woodland’, or ‘grid average’.
    - Resolution: 5 x 5 km grid squares.
  - Example file naming and fields indicate site-level metadata (SITECODE, SITENAME, X, Y, SITE_AREA) and deposition components (SOD, SOW, NOD, NOW, NHD, NHW, etc.) split into local (short-range) and long-range (long-range) contributions across multiple species and forms.

- Implications for monitoring and policy
  - FRAME provides a transparent, source-attribution-based method to understand how different emissions sources contribute to nitrogen and sulphur deposition at site- and habitat-level scales.
  - The calibration to CBED and site-specific mapping to protected areas supports policy evaluation, compliance checks, and targeted mitigation by identifying major contributing sources and spatial hot spots.
  - The approach emphasizes data provenance, metadata clarity, and reproducibility through explicit processing steps, quality checks, and public dissemination of datasets.