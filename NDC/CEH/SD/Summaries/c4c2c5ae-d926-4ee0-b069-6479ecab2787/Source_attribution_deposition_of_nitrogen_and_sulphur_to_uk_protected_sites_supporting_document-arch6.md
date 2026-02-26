# Frame Modelling

- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model to assess annual mean deposition of reduced and oxidised nitrogen and sulphur over the UK.
- Domain: British Isles, 5 km grid, 172 x 144 cells.
- Input emissions: UK National Atmospheric Emissions Inventory (NAEI) with 160 sub-sectors; 22 point sources; background area emissions (SO2, NOx, NH3) across 11 SNAP sectors; international shipping and European emissions.
- Ammonia inputs: from National Ammonia Reduction Strategy Evaluation System (NARSES) split into 5 sectors (livestock, fertiliser, non-agricultural abatable/non-abatable sources, waste sector).
- Spatial demarcation: regional land masks by England, Scotland, Wales, Northern Ireland to aid regulators in source attribution by country.
- Key outputs: footprints for SOx, NOy, NHx deposition; parallel outputs by short vs long-range input types; deposition separated for forest, moorland, and grid average habitats due to surface roughness effects.

- Running the model: baseline run with all sources, plus successive runs with each emission source abated by 25% to avoid non-linearities; footprints scaled by a factor of 4.
- Footprint calculation: FP(id=n) = DEP(id=0) – DEP(id=n), where DEP is FRAME-deposited deposition and id=0 is baseline.
- For each 5 km grid square, compute deposition for SOx, NOy, NHx across footprints; additionally decompose into detailed short/long-range source attribution types (10+ categories) and output by ecosystem type (forest, moorland, grid average) due to differing deposition rates.

- Post-processing and calibration: normalize individual footprints so their sum matches the baseline deposition; average discrepancy around 4% across components.
- Calibration to CBED: apply a calibration that aligns FRAME outputs with the official CBED (2011–2013) data. Uses a two-step approach:
  - Calibrate base DEP(UNC, 2012) to DEP(CAL, 2012) using CBED totals.
  - Calibrate footprints FP to ensure summed calibrated footprints reproduce CBED totals for 2012.
- Calibration aims to produce deposition totals consistent with official CBED data when footprints are aggregated.

- Spatial mapping to UK protected sites (SAC, SPA, SSSI):
  - FRAME outputs 160 files per footprint type per pollutant; aggregated to 90 footprint files to speed processing.
  - Python workflow merges footprints with a UK protected-site shapefile; computes for each site the minimum, maximum, and grid-average deposition per pollutant and footprint.
  - Grid-average deposition for a site is computed by area-weighting each grid square contribution.
  - Outputs three site-specific files representing deposition to forest, moorland, and grid average, each with min, max, and grid-average values across 90 footprints.

- Nature and units of recorded values:
  - All deposition values are in keq ha^-1 year^-1 (kilo-equivalents per hectare per year).
  - Conversion to kg: multiply sulfur deposition by 16 to get kg S ha^-1 year^-1; multiply nitrogen deposition by 14 to get kg N ha^-1 year^-1.
  - Total nitrogen deposition is the sum of NO2/NO3 and NH3/NH4 components.

- Quality control:
  - Normalization of footprints to ensure their sum matches the baseline, mitigating model non-linearities.
  - National budgets of total deposition checked against previous years for consistency.
  - Each footprint output saved as a jpg to aid error detection.

- Data structure and datasets:
  - Datasets 1–3 provide 3-year means (2013–2015) of ecosystem-specific source attribution and deposition for nitrogen and sulphur, with min, max, and area-weighted values at each SAC/SPA/SSSI site.
  - File names indicate site-level attribution by habitat (forest or moorland) or grid average: APIS_source_attribution_nitrogen_sulphur_to_forest_bysite.csv, APIS_source_attribution_nitrogen_sulphur_to_moorland_bysite.csv, APIS_source_attribution_nitrogen_sulphur_to_gridaverage_bysite.csv.
  - Key fields include SITECODE, SITENAME, X, Y, SITE_AREA, COUNTRY/ DESIGNATION, FOOTPRINT_ID/NAME, AREA_POINT, SOURCE_LOCATION, and deposition values for multiple components (local/short-range and long-range for SOD/SOW, NOD/NOW, NHD/NHW) with min, max, and avg.
  - All values are expressed in keq ha^-1 year^-1 and relate to 5 x 5 km grid resolution.
  - Data are organized to support site-level deposition attribution for forests, moorlands, and grid-average habitats.