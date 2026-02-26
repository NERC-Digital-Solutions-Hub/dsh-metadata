# Survey Overview

- InSAR measurements over Caithness and Sutherland to quantify peatland surface motion across Flow Country using APSIS Intermittent Small Baseline Subset (ISBAS) InSAR.
- Data cover surface motion across all landcover types within the survey area, including timeseries of peat surface height and long-term mean motion.
- Cadence: approximately every 6–12 days, using Sentinel-1A/1B images; total of 410 images processed from 2015-03-12 to 2019-06-01.
- Missing pixels are excluded due to low coherence; some dates missing due to processing issues or coherence problems.
- Processing conducted by Terra Motion Ltd.

## Survey Area

- Area processed is about 930 km² of blanket bog in the Flow Country (Caithness and Sutherland), with water bodies and sea masked out.
- Outputs are georeferenced per pixel with area-focused processing (see Figure 1 reference).

## Data and Timeframe

- Data source: Sentinel-1A and -1B, Orbit 125, with images every 6–12 days.
- Timeframe: 12 March 2015 to 1 June 2019.
- Reference frame: Motion measured relative to Wick Airport (58.4533°N, 3.0879°W).
- Outputs per georeferenced pixel location (~80 by 90 m resolution):
  - Time series of multi-annual average line-of-sight velocity (m/yr).
  - Mean velocity in the line-of-sight (m/yr).

## Methodology

- APSIS (Adaptive Pixel System Intermittent Small Baseline Subset) InSAR method to improve density and spatial distribution of survey points in vegetated areas with low coherence.
- Based on an adapted SBAS DInSAR time-series algorithm to robustly estimate ground motion velocities.
- Processing workflow uses Terra Motion Ltd's Punnet software for co-registration of SLC data to time-series generation.
- Baseline constraints: maximum horizontal baseline 250 m; maximum temporal separation 1 year; coherence threshold 0.25; point threshold 360.
- Phase unwrapping performed with an in-house SNAPHU implementation.
- Output products include per-pixel motion time series and aggregated velocity products.

## Data Products and File Formats

- Core products (per-pixel):
  - Motion time series (LOS velocity) and mean LOS velocity at ~80 x 90 m resolution.
- Additional outputs:
  - ortho_velocity_utm_isbas.tif: Mean line-of-sight motion over the study period (m/yr).
  - ortho_velocity_utm_isbas_evv.tif: Corrected mean vertical motion over the study period (m/yr).
  - ortho_cohcount.tif: Number of coherent interferograms per pixel.
  - ortho_velocity_utm_verror.tif: Standard error of the LOS motion (m/yr).
- Time-series and height files:
  - Time-series files: .tif with corresponding .aux files containing relative height information for a date, named by date (e.g., 20190701.tif, 20190701.tif.aux). Height values are in meters.
- Coordinate reference system:
  - WGS84 UTM Zone 29N; no_data value is -999.
- File naming and structure:
  - Time-series files are date-stamped (YYYYMMDD) and stored as individual .tif files with accompanying .aux height files.
- Data provenance:
  - Sentinel data (2015–2019) from Copernicus Open Access Hub (ESA); processing described in the methodology section; references include key ISBAS/SBAS works.

## Access and Usage

- Outputs are designed to enable end-users to “self-serve” motion information and to understand long-term peatland surface dynamics.
- Users should note patchy coherence and dates missing due to processing or coherence, which affect completeness of the time series.
- Data can be used to assess peatland subsidence/ground motion patterns over the Flow Country and to compare across land cover types.

## Data Quality and Limitations

- Missing pixels due to low coherence; some dates unavailable due to processing issues or coherence limitations.
- Temporal sampling up to yearly gaps where baseline constraints or coherence issues prevent reliable estimation.
- Height and velocity products are smoothed representations at 80 x 90 m resolution and rely on the APSIS/ISBAS processing assumptions.

## Appendices and References

- Appendix enumerates the Sentinel-1 imagery used (S1A/S1B) with dates, file names, and processing details (Table 1 and extended lists).
- References include:
  - Sentinel data provenance (ESA Copernicus, 2015–2019).
  - ISBAS/InSAR methodology papers (Bateson et al. 2015; Cigna & Sowter 2019; Gong et al. 2016; Osmanoğlu et al. 2016; Sowter et al. 2016).
  - Phase unwrapping and time-series analysis foundational works.