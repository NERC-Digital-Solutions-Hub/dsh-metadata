# Introduction

- Study scope: 51 sites across three regions (ZOIs) within the Corridor Ankeniheny-Zahamena (CAZ), Madagascar.
- Field design: measurements and samples taken at five locations along ~60 m transects, from upslope (location 1) to downslope (location 5).
- Depths: measurements/samples at the surface and two depths below the surface.
- Soil texture sampling: a bulk sample per depth per transect created by combining samples at each measurement location.
- Data completeness: missing data denoted as NaN.
- Purpose: describes data collection methods and contents of the data file.

## Data collection design and location metadata

- Transect identifier: used by the P4GES hydrology team for all measurements and samples.
- Zone of Interest (ZOI): study region codes (2–4).
- Land use classification (six categories):
  - CC: closed canopy forest
  - RF: reforestation
  - TSA: tree fallow
  - SSA: shrub fallow
  - TM: degraded grassland
  - EUC: eucalyptus plantation
- Site identifiers: site location name (linked to transect) and P4GES site name (for cross-dataset comparison).
- Brief soil description: rough soil texture notes.
- Dominant species: names of dominant vegetation.
- Site description: average slope aspect and angle for the site and for the measurement transect.
- Sample locations: latitude/longitude (decimal degrees, WGS84) and local slope for points 1–5; slope measurements noted for certain transects.

## Measured variables and methods

- Soil surface saturated hydraulic conductivity (Ksat 0–10 cm)
  - Method: double ring infiltrometer (inner ring 15 cm diameter); ponding depth 10–20 cm.
  - Output: Ksat per measurement point (1–5) and site-level statistics (mean, median, standard deviation).
- Ksat at deeper depths
  - 10–20 cm and 20–30 cm: measured with Amoozemeter (constant head permeameter).
  - Output: per-point values and site-level statistics (mean, median, standard deviation).
- Soil texture
  - Sampling depths: 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm; bulk sample per depth per transect.
  - Analysis: Helium-Neon Laser Optical System (VU Amsterdam) or, for transects 55–57, sieving and Sedigraph at University of Zürich.
  - Output: percentages of clay, silt, and sand; note about transects 1–10 combining certain depths.
- Other soil hydrological characteristics
  - Undisturbed soil core (100 cm³) collected at each measurement location for depths 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm.
  - Measurements: weight after saturation (5 days), drainage (3 days), and oven-drying (24 h at 105°C) to derive porosity, moisture at field capacity, and bulk density.
  - Output: per-sample values (1–5) plus site-level statistics.
- Key definitions
  - Bulk density: oven-dried weight divided by 100 cm³ volume.
  - Porosity: (saturated weight − dry weight) / (density of water × 100 cm³).
  - Moisture content at field capacity: drainage-weight difference divided by water density and 100 cm³.

## Data structure, quality, and usage notes

- Data organization: values provided for each transect point (1–5) plus aggregated site statistics for Ksat, texture, and hydrological properties.
- Data quality considerations:
  - Missing data indicated as NaN.
  - Different laboratories analyzed soil texture for some transects (VU Amsterdam vs University of Zürich), which may affect comparability.
  - Some transects have incomplete slope measurements (noted in methods).
- Potential uses for data support:
  - Enable self-serve exploration of soil hydraulic properties across land-use types and spatial gradients.
  - Support cross-site comparisons and dashboards focusing on Ksat, texture, porosity, and field capacity.
  - Facilitate data quality checks, metadata reconciliation, and integration with other P4GES hydrology datasets.

## References

- Styger E, Rakotondramasy HM, Pfeffer MJ, Fernandes ECM, Bates DM. 2007. Influence of slash-andburn farming practices on fallow succession and land degradation in the rainforest region of Madagascar. Agriculture, Ecosystems & Environment, 119: 257–269.
- Zwartendijk BW, van Meerveld HJ, Ghimire CP, Bruijnzeel LA, Ravelona M, Jones JPG. 2017. Rebuilding soil hydrological functioning after swidden agriculture in eastern Madagascar. Agriculture, Ecosystems & Environment, 239: 101–111.