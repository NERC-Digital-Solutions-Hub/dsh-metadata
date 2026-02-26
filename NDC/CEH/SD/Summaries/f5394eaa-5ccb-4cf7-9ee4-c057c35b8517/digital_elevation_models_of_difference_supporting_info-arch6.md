# Digital Elevation Models of Difference (DoD) for Chamoli avalanche-debris flow, Uttarakhand, India

## Overview
- Geospatial raster dataset (DoD) representing vertical topographic change between pairs of DEMs.
- DoDs created to analyze landscape change after the 7 February 2021 avalanche-debris flow and to support numerical modelling with CAESAR-Lisflood.

## Data content
- DoD rasters (.tif) where pixel values indicate net elevation change between the two DEMs:
  - Negative values = surface lowering (erosion)
  - Positive values = surface gain (deposition)
- Completeness: includes all DoDs generated for this research; additional DoDs could be created from other input DEMs.
- Units: meters of elevation change per pixel.

## Collection context
- Area: roughly bounded by WGS 84 / UTM Zone 44 in the Chamoli District, Uttarakhand, India.
  - Top left: 352312 m E, 3385209 m N
  - Bottom right: 384787 m E, 3358896 m N
- Timeframe:
  - Raw DEMs generated between 10 February 2021 and 27 April 2022.
  - DoDs created on a rolling basis within the same window.
- Responsible party: project Principal Investigator generated all DoDs.

## Methods and interpretation
- Creation method: DoDs produced in QGIS (versions 3.18 and 3.24) using the Raster Calculator.
  - For each DEM pair, later DEM minus earlier DEM.
  - Resulting DoD indicates changes between the date pair.
- Data structure: raster grids; each DoD file name encodes the date span (YY-MM-DD).
  - Example: 210210_210606_DoD.tif covers 2021-02-10 to 2021-06-10.
  - 1509 indicates September 2015 (composite DEM used in some analyses).
- Significance assessment: statistically significant changes identified using stable hillslope areas from Pléaides imagery.
  - Standard deviation of DoD within stable areas used to estimate a two-sigma DoD uncertainty.
  - Reported uncertainties:
    - ±1.11 m (Sep 2015 – 10 Feb 2021)
    - ±0.91 m (10 Feb 2021 – 06 Jun 2021)
    - ±0.61 m (06 Jun 2021 – 25 Dec 2021)
    - ±1.14 m (10 Feb 2021 – 25 Dec 2021)
    - ±1.06 m (10 Feb 2021 – 27 Jan 2022)
  - DoD values exceeding the relevant threshold are considered statistically significant.
- Quality control: holes or data gaps from input DEMs propagate into the DoD (due to photogrammetric gaps, cloud cover, occlusions, or view angle differences).

## Dataset structure and files
- DoD rasters:
  - 1509_composite_210210_DoD.tif
  - 210210_210606_DoD.tif
  - 210606_211225_DoD.tif
  - 210210_211225_DoD.tif
  - 210210_220127_DoD.tif
  - 210210_210606_DoD.tif (and other combinations as named)
- Stable areas:
  - stable_areas.shp (plus auxiliary .cpg, .dbf, .prf, .qmd, .shx files)
- Naming conventions: the two dates in each DoD file name indicate the period spanned by that DoD; “1509” indicates September 2015 (composite DEM).

## Usage, replication, and data products
- Users can reproduce additional DoDs by combining input DEMs from this collection using the same Raster Calculator workflow.
- Can estimate significant change thresholds for any DoD using the provided stable-area approach and two-sigma uncertainty values.
- Outputs support self-serve analysis and visualization (e.g., in GIS tools) and can inform further data products or policymaking related to landscape change analysis.