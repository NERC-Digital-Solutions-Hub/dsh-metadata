# Introduction

- Study scope: 51 sites across three Regions of Interest (ZOIs) within the Corridor Ankeniheny-Zahamena (CAZ), Madagascar.
- Sampling design: at each site, measurements and samples at five locations along ~60 m transects, from upslope (location 1) to downslope (location 5); measurements at soil surface and two depths below the surface.
- Soil texture: a soil sample is taken at each measurement location and combined to form one bulk sample per depth per transect.
- Data status: missing data are denoted as NaN.
- Purpose: the file describes the data collection methods and the contents of the data file.

## Study metadata and site descriptors

- Transect number: used by the P4GES hydrology team for all measurements and samples.
- ZOI: study region as used in the P4GES project.
- Land use classification (six categories): CC (closed canopy forest), RF (reforestation), TSA (tree fallow), SSA (shrub fallow), TM (degraded grassland), EUC (eucalyptus plantation).
- Site identifiers: site location name (related to transect and land use), P4GES site name (comparison with other P4GES datasets).
- Soil description and vegetation: brief soil texture notes; dominant species.
- Site description: average slope aspect and slope angle for the site; aspect and average slope for the transect.

## Sample locations and geospatial data

- For each measurement location (1–5): position, latitude, longitude (WGS84); local slope.
- Data collection tools: handheld GPS used to obtain coordinates; inclinometer used to measure slope.
- Some transects have slope measurements taken between sample points (gaps noted).

## Soil hydraulic conductivity data (Ksat)

- Surface Ksat (0–10 cm): measured with a double ring infiltrometer (inner ring 15 cm diameter); ponding depth 10–20 cm; Ksat calculated from steady-state infiltration rate at the end of the test.
- Per-point values: provided for each measurement point (1–5); plus site-level statistics (average, median, standard deviation).
- Subsurface Ksat: measured at 10–20 cm and 20–30 cm using a constant-head permeameter (Amoozemeter); values per measurement point and site-level statistics (average, median, SD).
- Method references: see Zwartendijk et al. (2017) for details on infiltration-based Ksat measurements.

## Soil texture data

- Sampling depths: 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm; samples combined to form one bulk sample per depth per transect.
- Sample handling: bulk samples stored in airtight bags; analyzed at different laboratories.
  - VU University Amsterdam (The Netherlands) using a Helium-Neon Laser Optical System.
  - Transects 55–57 analyzed at University of Zürich (Switzerland) using sieving and a Sedigraph.
- Special notes: for transects 1–10, bulk samples from the 12.5–17.5 cm and 22.5–27.5 cm depths were combined prior to analysis.
- Outputs: percentages of clay, silt, and sand for each bulk sample.

## Other soil hydrological characteristics

- Undisturbed soil cores: 100 cm³ at each measurement location and at each depth (2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm).
- Measurements taken: weight immediately after sampling, after 5 days of saturation, after 3 days of gravity drainage, and after oven-drying at 105°C for 24 hours.
- Per-sample data: values provided for each location (1–5) with site-level statistics (average, median, SD).
- Calculated properties:
  - Bulk density: dry weight divided by 100 cm³ volume.
  - Porosity: determined from saturated vs. dry weight and water density.
  - Moisture content at field capacity: calculated from drainage and oven-dried weight.
- Data interpretation: these measurements provide porosity, bulk density, and field-capacity moisture content for each depth and transect.

## Data usage, structure, and quality

- Data structure: per-point measurements (1–5) along transects plus site-level statistics (mean, median, SD) across the parameters described.
- Data completeness: includes missing data denoted as NaN; notes on potential metadata gaps across labs and transects.
- Data provenance: multiple laboratories involved in texture analyses; references provided for methods and context.
- References for methodology:
  - Styger, Rakotondramasy, Pfeffer, Fernandes, Bates (2007) on land-use classification.
  - Zwartendijk, van Meerveld, Ghimire, Bruijnzeel, Ravelona, Jones (2017) on soil hydrological functioning and Ksat measurements.