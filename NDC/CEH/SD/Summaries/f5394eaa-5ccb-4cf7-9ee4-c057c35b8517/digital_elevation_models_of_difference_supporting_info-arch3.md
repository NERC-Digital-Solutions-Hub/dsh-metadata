# Digital Elevation Models of Difference (DoD) for landscape change following the 7 February 2021 avalanche-debris flow in Chamoli District, Uttarakhand, India

## What are these data?
- Digital Elevation Models of Difference (DoD): raster (.tif) datasets that quantify vertical topographic change between two dates.
- DoDs are used in GIS for analyses of landscape change and to support related geospatial modelling.

## Why were the data collected?
- To analyze landscape change after the 7 February 2021 avalanche-debris flow in Chamoli District, Uttarakhand, India.
- To support numerical modelling using CAESAR-Lisflood (as noted in the data collection resources).

## Where were the data collected?
- Spatial extent described by a bounding box in WGS 84 / UTM Zone 44:
  - Top left: 352312 m E, 3385209 m N
  - Lower right: 384787 m E, 3358896 m N

## When were the data collected?
- Raw DEMs underpinning the DoDs were generated between 10 February 2021 and 27 April 2022 (in a rolling sequence).
- DoDs themselves were created within that same time window.

## How were the data collected?
- DoDs were created in QGIS (versions 3.18 and 3.24) using the Raster Calculator.
- For a given DEM pair, the later DEM was subtracted from the earlier DEM.
- Interpretation: negative values indicate surface lowering (erosion); positive values indicate surface gain (deposition).

## Who was responsible for collection and interpretation?
- The project principal investigator (PI) created all DoDs using the described method.

## Completeness
- The dataset includes all DoDs generated as part of this research.
- Other DoDs could be generated using alternative input DEM pairs; the methodology to replicate and estimate a significant-change threshold is described in section 5.

## Nature and units of recorded values
- Data are raster grids; pixel values represent net elevation change between the two input DEMs.
- Negative values = erosion; positive values = deposition.

## Quality control
- Gaps/holes from input DEMs are carried into resulting DoDs.
- A two-sigma significant-change threshold is estimated using 16 stable hillside areas identified via Pléaides orthoimagery, by computing the standard deviation of DoD values within these areas.
- Reported uncertainty (two-sigma) for each DoD:
  - ±1.11 m for 2015-09 to 2021-02-10 DoD
  - ±0.91 m for 2021-02-10 to 2021-06-06 DoD
  - ±0.61 m for 2021-06-06 to 2021-12-25 DoD
  - ±1.14 m for 2021-02-10 to 2021-12-25 DoD
  - ±1.06 m for 2021-02-10 to 2022-01-27 DoD
- Stable areas polygons used for uncertainty assessment are included with the dataset.

## Dataset structure
- DoD files included:
  - 1509_composite_210210_DoD.tif
  - 210210_210606_DoD.tif
  - 210606_211225_DoD.tif
  - 210210_211225_DoD.tif
  - 210210_220127_DoD.tif
- Stability reference:
  - stable_areas.shp (plus associated files: .cpg, .dbf, .prf, .qmd, .shx)
- File naming convention:
  - The two dates in each DoD filename indicate the period spanned.
  - The composite from September 2015 is denoted as "1509" in the filenames.