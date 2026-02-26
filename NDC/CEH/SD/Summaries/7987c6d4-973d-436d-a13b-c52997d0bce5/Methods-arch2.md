# Introduction

- Study scope: 51 sites across three regions (ZOIs) within the Corridor Ankeniheny-Zahamena (CAZ) in Madagascar.
- Sampling design: measurements and samples at five locations along ~60 m transects, from upslope (point 1) to downslope (point 5); surface and two soil depths sampled; soil texture samples at each measurement location were combined to create one bulk sample per depth per site.
- Data handling: missing data denoted as NaN. The document describes data collection methods and the contents of the data file.

- Purpose and use: method and data content are provided to support standardized environmental monitoring and analysis of soil hydrological properties across sites and land-use types.

- Metadata and site descriptors:
  - Transect number: used by the P4GES hydrology team.
  - ZOI: study region (2–4) per P4GES.
  - Land use classification (six categories): CC (closed canopy forest), RF (reforestation), TSA (tree fallow), SSA (shrub fallow), TM (degraded grassland), EUC (eucalyptus plantation).
  - Site location name: related to transect and land use.
  - P4GES site name: alternative name for cross-dataset comparisons.
  - Brief soil description: rough soil texture notes from field observations.
  - Dominant species: names of dominant vegetation.
  - Site description: average slope aspect and angle for the site; transect aspect and slope.
  - Sample locations: latitude/longitude (WGS84) and local slope for points 1–5 (some transects have slope measurements between sample points).

- Soil hydraulic conductivity (Ksat):
  - Ksat (0–10 cm): measured with a double ring infiltrometer; ponding depth 10–20 cm; outputs per measurement point (1–5) plus site average, median, and standard deviation.
  - Ksat (10–20 cm) and Ksat (20–30 cm): measured with an Amoozemeter; same output structure (per point and site statistics).

- Soil texture:
  - Sampling depths: 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm; bulk sample per depth per transect.
  - Analysis: Helium-Neon Laser Optical System (VU Amsterdam) for most samples; some transects (55–57) analysed at University of Zürich using sieving and Sedigraph.
  - Note: For transects 1–10, the 12.5–17.5 cm and 22.5–27.5 cm bulk samples were combined prior to analysis.
  - Output: percentages of clay, silt, and sand for each sample.

- Other soil hydrological characteristics:
  - Undisturbed soil core (100 cm³) collected at each measurement location for depths 2.5–7.5 cm, 12.5–17.5 cm, and 22.5–27.5 cm.
  - Measurements: weights immediately after sampling, after five days of saturation, after three days of gravity drainage, and after drying in an oven at 105 °C for 24 hours.
  - Outputs: porosity, moisture content at field capacity, bulk density (per sample; also summarized as site statistics).
  - Calculations:
    - Bulk density = dry weight / 100 cm³.
    - Porosity = (saturated weight − dry weight) / (density of water × 100 cm³).
    - Moisture content at field capacity = (drained weight − dry weight) / (density of water × 100 cm³).

- Data outputs and availability:
  - For each measurement point along the transect (1–5), plus site-level statistics (average, median, standard deviation) are included in the data file.
  - Lab and method notes: some samples analyzed at different laboratories; transects 1–10 had certain depths combined prior to analysis.

- Figures referenced:
  - Figure 1: Double ring and permeameter measurements.
  - Figure 2: Saturation and gravity drainage behavior.

- References:
  - Styger E, et al. 2007. Influence of slash-and-burn farming on fallow succession and land degradation in Madagascar.
  - Zwartendijk BW, et al. 2017. Rebuilding soil hydrological functioning after swidden agriculture in eastern Madagascar.