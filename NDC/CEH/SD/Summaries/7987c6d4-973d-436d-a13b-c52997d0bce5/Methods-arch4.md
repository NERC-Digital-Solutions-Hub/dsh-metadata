# Introduction

- Study of 51 sites across three regions (ZOIs) within the Corridor Ankeniheny-Zahamena (CAZ), Madagascar; measurements taken at five locations along ~60 m transects, from upslope (location 1) to downslope (location 5); measurements and samples at the surface and two depths below the surface; missing data denoted NaN.
- The document describes the data collection methods and the contents of the data file.

## Study design and site metadata

- Transect number used by the P4GES hydrology team for all measurements and samples.
- Land use classification into six categories: CC (closed canopy forest), RF (reforestation), TSA (tree fallow), SSA (shrub fallow), TM (degraded grassland), EUC (eucalyptus plantation).
- Site location naming linked to transect number; P4GES site name used for cross-dataset comparison.
- Brief soil description available; dominant species recorded.
- Site description includes average slope aspect and angle; transect-level aspect and slope.

## Measurements and sampling details

- Sample locations: five measurement points per transect (1–5) with latitude, longitude (WGS84), and local slope; slope measured with inclinometer; transects may have variable slope measurements (e.g., some transects 16–18, 22, 31–44).
- Soil surface saturated hydraulic conductivity (Ksat) 0–10 cm:
  - Measured with a double ring infiltrometer (inner ring 15 cm diameter; ponding depth 10–20 cm).
  - Ksat values provided for each measurement point (1–5) plus site-level statistics (mean, median, standard deviation).
- Ksat for 10–20 cm and 20–30 cm:
  - Measured with an Amoozemeter (constant head permeameter).
  - End-of-test steady-state infiltration rates yield Ksat; values per point and site statistics (mean, median, standard deviation).
- Soil texture:
  - Samples collected at 2.5–7.5 cm, 12.5–17.5 cm, and 22.5–27.5 cm; bulk sample per depth per transect created by compositing at each measurement point.
  - Analysis performed with Helium-Neon Laser Optical System (VU Amsterdam) or, for transects 55–57, at the University of Zürich using sieving and Sedigraph.
  - Reported as percentages of clay, silt, and sand; note that for transects 1–10 the two deeper sub-samples were pooled prior to analysis.
- Other soil hydrological characteristics:
  - Undisturbed soil cores (100 cm³) collected at each measurement location for depths 2.5–7.5 cm, 12.5–17.5 cm, and 22.5–27.5 cm.
  - Determinations include porosity, moisture content at field capacity, and bulk density; measurements taken immediately after sampling, after saturation (5 days), after gravity drainage (3 days), and after oven drying at 105 °C for 24 hours.
- Key soil property definitions:
  - Bulk density: oven-dried dry weight divided by 100 cm³ volume.
  - Porosity: derived from saturated versus dry weights and water density; expressed as percentage.
  - Moisture content at field capacity: calculated from drainage and dry weights relative to water density and sample volume.

## Data quality, governance, and provenance

- Missing data are explicitly indicated as NaN in the data file.
- Data are generated from multiple labs (VU Amsterdam for most texture analyses; University of Zürich for some transects) with documented methods (laser optical system, sieve/Sedigraph).
- The data file includes per-point measurements (points 1–5) and per-site aggregates (mean, median, standard deviation) for Ksat and soil texture.
- References underpinning methods:
  - Styger et al. 2007 on slash-and-burn farming impacts and fallow succession.
  - Zwartendijk et al. 2017 on rebuilding soil hydrological functioning after swidden agriculture.

## Implications for data strategy and usage

- Comprehensive, multi-depth soil hydrology dataset with standardized transect-based sampling across diverse land uses.
- Rich metadata: transect/ZOI identifiers, land use, coordinates, slope, dominant species, and site descriptions enable tracking, cross-site comparisons, and integration with broader datasets.
- Data governance considerations:
  - Clear provenance from multiple laboratories requires harmonized metadata and units.
  - Gaps and missing data management are essential for cross-site analyses.
  - Consistent depth intervals and measurement protocols support reproducibility and co-ownership of data products.