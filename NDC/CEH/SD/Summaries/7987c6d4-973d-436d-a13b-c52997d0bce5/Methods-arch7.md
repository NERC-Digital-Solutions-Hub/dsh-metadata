# Introduction

- Describes methods and contents of a data file from a study of 51 sites across three zones of interest (ZOIs) within the Corridor Ankeniheny-Zahamena (CAZ) in Madagascar.
- At each site, measurements and soil samples were taken at five locations along ~60 m transects, from upslope (point 1) to downslope (point 5).
- Measurements/samples were collected at the soil surface and at two depths below the surface; soil texture samples were combined to create one bulk sample per depth per site.
- Missing data are denoted as NaN.

## Study design and sampling

- Transect numbering used by the P4GES hydrology team for all measurements and samples.
- Zones of Interest (ZOI) are used to designate study regions (2–4 within P4GES context).

## Site metadata and land use

- Land use classified into six categories by dominant species and owner input:
  - CC: closed canopy forest
  - RF: reforestation
  - TSA: tree fallow
  - SSA: shrub fallow
  - TM: degraded grassland
  - EUC: eucalyptus plantation
- Site location name ties transect number to area and land use; P4GES site name provides an alternative reference for comparison.
- Brief soil description provided as rough field observation; dominant species listed.
- Site description includes average slope aspect and angle for the site, plus aspect and average slope for each transect.

## Spatial data and sample locations

- Sample locations are given with latitude/longitude (decimal degrees, WGS84) and local slope for measurement points 1–5.
- Coordinates obtained via handheld GPS; slope measured with an inclinometer.
- For transects 16–18, 22, and 31–44, slope measurements were taken between sample points.

## Measurements: soil hydraulic conductivity (Ksat)

- Surface layer (0–10 cm): Ksat measured with a double ring infiltrometer (inner ring diameter 15 cm). Ponding depth 10–20 cm. Ksat calculated from steady-state infiltration rate at experiment end.
- Subsurface layers:
  - Ksat at 10–20 cm
  - Ksat at 20–30 cm
  - Both measured with a constant-head permeameter (Amoozemeter) and derived from steady-state infiltration rate at end.
- For each measurement point (1–5), results are provided plus site-level average, median, and standard deviation.

## Soil texture and depth sampling

- Soil texture samples collected at three depths:
  - 2.5–7.5 cm
  - 12.5–17.5 cm
  - 22.5–27.5 cm
- Samples bulked per depth per transect; stored in airtight bags.
- Analyses:
  - VG-based method (Helium-Neon Laser Optical System) at VU University (Amsterdam) for most transects.
  - Some transects (55–57) analyzed at University of Zürich using sieving and Sedigraph.
- Reported as percentages of clay, silt, and sand.
- For transects 1–10, bulk samples from 12.5–17.5 cm and 22.5–27.5 cm were combined prior to analyses.

## Other soil hydrological characteristics

- Undisturbed soil cores (100 cm³) collected at each measurement location at depths 2.5–7.5 cm, 12.5–17.5 cm, and 22.5–27.5 cm.
- Measurements taken immediately after sampling, after 5 days of saturation, after 3 days of gravity drainage, and after oven-drying at 105 °C for 24 hours.
- Parameters derived per sample (and reported as per site):
  - Porosity
  - Moisture content at field capacity
  - Bulk density
- Bulk density computed as dry weight / 100 cm³.
- Porosity computed from weight differences, water density, and volume.
- Moisture content at field capacity computed from drainage and dry weight.

## Data visualization and references

- Figure references:
  - Figure 1: Double ring and permeameter measurements (Ksat methodologies).
  - Figure 2: Saturation and gravity drainage behavior of soil samples.
- References:
  - Styger et al. 2007 (land-use influence on fallow and degradation)
  - Zwartendijk et al. 2017 (soil hydrological functioning after swidden agriculture)