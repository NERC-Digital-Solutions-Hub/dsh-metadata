# Digital elevation models of difference (DoD)

## What these data are
- Digital elevation models of difference (DoD) are raster (.tif) geospatial datasets that quantify vertical (z) topographic change between two dates.
- DoDs show negative values for surface lowering (erosion) and positive values for surface gain (deposition).
- They are commonly used in GIS to analyze landscape change and support other geospatial analyses.

## Why these data were collected
- To analyze landscape change following the avalanche-debris flow on 7 February 2021 in Chamoli District, Uttarakhand, India.
- The DoDs also supported numerical modelling using CAESAR-Lisflood.

## Where these data were collected
- Area described by a bounding box in WGS 84 / UTM Zone 44:
  - Top left: 352312 m E, 3385209 m N
  - Lower right: 384787 m E, 3358896 m N

## When these data were collected
- Raw DEMs underpinning the DoDs were generated between 10 February 2021 and 27 April 2022.
- DoDs were created on a rolling basis within this window.

## How the data were collected
- DoDs were created in QGIS (v3.18 and v3.24) using the Raster Calculator.
- For a DEM pair, the later DEM was subtracted from the earlier DEM; negative values indicate erosion, positive values indicate deposition.

## Who was responsible
- The project Principal Investigator (PI) created all DoDs using the described method.

## Completeness of the dataset
- The dataset contains all DoDs generated as part of this research.
- Other DoDs could be generated from alternative input-DEM differencing, using data from this collection.
- Users can replicate the method to estimate associated significant change thresholds (described in section 5).

## Nature and units of recorded values
- Data are gridded rasters.
- Pixel values represent net elevation change between the two input DEMs.
- Negative values = surface lowering; positive values = surface gain.

## Quality control
- Holes/gaps from input DEMs are propagated into the DoDs (caused by photogrammetric reconstruction gaps due to cloud cover, occlusions, or large view-angle differences).
- A statistically significant change threshold was estimated per DoD using 16 stable hillside areas identified from Pléaides orthoimagery.
- The threshold is based on the standard deviation of DoD values within these stable areas, yielding a two-sigma uncertainty:
  - ±1.11 m (Sept 2015 – 10 Feb 2021 DoD)
  - ±0.91 m (10 Feb 2021 – 06 Jun 2021 DoD)
  - ±0.61 m (06 Jun 2021 – 25 Dec 2021 DoD)
  - ±1.14 m (10 Feb 2021 – 25 Dec 2021 DoD)
  - ±1.06 m (10 Feb 2021 – 27 Jan 2022 DoD)
- Stable area polygons used for uncertainty estimation are provided with the data resource.

## Dataset structure
- The dataset contains the following DoD raster files:
  - 1509_composite_210210_DoD.tif
  - 210210_210606_DoD.tif
  - 210606_211225_DoD.tif
  - 210210_211225_DoD.tif
  - 210210_220127_DoD.tif
- Stable areas:
  - stable_areas.shp (plus auxiliary .cpg, .dbf, .prf, .qmd, and .shx files)
- Naming notes:
  - The two dates in each DoD filename indicate the period spanned by that DoD.
  - The composite 1509 corresponds to September 2015.

## Significance thresholds and interpretation
- DoD values exceeding the estimated two-sigma thresholds are considered statistically significant changes.
- The threshold confidence varies by DoD period and is based on stable-area standard deviations.
- DoDs provide a basis for identifying and quantifying landscape change due to the avalanche-debris flow, useful for monitoring and modelling efforts.

## Reuse and accessibility for Analysts Monitoring the Environment
- The DoDs are designed for standard GIS analysis and can be combined with other data sources to enhance environmental monitoring.
- The data are created from established data sources and follow a reproducible methodology (QGIS Raster Calculator, documented thresholds).
- Analysts are encouraged to reuse and extend analyses, including generating additional DoDs from alternative input DEMs and applying the provided uncertainty thresholds.