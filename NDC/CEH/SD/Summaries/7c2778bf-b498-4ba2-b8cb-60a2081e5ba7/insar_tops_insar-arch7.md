# Survey Overview

- InSAR measurements over Caithness and Sutherland were used to quantify peatland surface motion in the Flow Country using the APSIS (Intermittent Small Baseline Subset) InSAR technique.
- Data cover surface motion across land cover types within the survey area and include timeseries of peat surface height and long-term mean motion.
- Cadence and coverage: data were collected every 6–12 days, using Sentinel-1A and Sentinel-1B images, from 12 March 2015 to 1 June 2019, with missing pixels excluded due to low coherence and missing survey dates due to processing issues or coherence problems.
- Processing: completed by Terra Motion Ltd using the Punnet software; phase unwrapping via in-house SNAPHU implementation.

## Survey Area

- Processing area is approximately 930 km2 of blanket bog in the Flow Country (Caithness and Sutherland), excluding surface water bodies and the sea.
- A map (Figure 1) shows the APSIS-processed area.

## Methodology and Data Products

- APSIS InSAR methodology: applies a modified low-resolution SBAS time-series approach to improve point density and spatial distribution in vegetated areas where traditional InSAR struggles with coherence.
- Outputs per georeferenced pixel:
  - Motion time series: multiannual average line-of-sight velocity (m/yr)
  - Mean velocity in the line-of-sight
- Resolution: about 80 by 90 meters per pixel.
- Reference frame: motion measured relative to a stable reference point at Wick Airport (58.4533° N, 3.0879° W).
- Additional data products available:
  - ortho_velocity_utm_isbas.tif: Mean LOS motion over the study period (m/yr)
  - ortho_velocity_utm_isbas_evv.tif: Corrected mean vertical motion over the study period (m/yr)
  - ortho_cohcount.tif: Number of coherent interferograms per pixel
  - ortho_velocity_utm_verror.tif: Standard error of LOS motion (m/yr)

## File Naming Convention and Coordinate System

- Coordinate reference system: WGS84 UTM Zone 29N.
- No-data value: -999.
- Time-series data: stored as individual .tif files with corresponding .aux files.
- Example naming: 20190701.tif and 20190701.tif.aux.
- Height information: stored as relative height of the land surface for a given date (units in meters).
- Additional files formatted similarly (e.g., ortho_velocity_utm_isbas.tif, etc.).

## Data Quality, Gaps, and Limitations

- Missing pixels occur where coherence is low; such pixels are excluded from the time series.
- Missing survey dates exist due to processing issues or poor coherence.
- Baseline and processing constraints:
  - Maximum horizontal baseline: 250 m
  - Maximum temporal separation: 1 year
  - Coherence threshold: 0.25
  - Point threshold: 360
- Data are limited to the study area and are subject to the usual uncertainties of InSAR-based velocity measurements, especially in vegetated peatlands.

## Reference and Usage Notes

- Data sourced from Copernicus Sentinel (S1A/S1B) platforms; processed by ESA with APSIS implementation.
- Primary purpose: enable map-based visualization and exploration of peatland surface motion and related temporal trends for researchers and policymakers.
- Suggested GIS use: integrate with other land-surface datasets, apply masking for non-peat surfaces if needed, and consider pixel-level coherence and standard error when interpreting motion rates.