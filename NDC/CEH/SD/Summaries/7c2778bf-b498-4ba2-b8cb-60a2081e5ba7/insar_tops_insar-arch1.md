# Survey Overview

- Objective: Use Interferometric Synthetic Aperture Radar (InSAR) with the APSIS/ISBAS approach to measure peatland surface motion across the Flow Country, Caithness and Sutherland. Provide timeseries of peat surface height and long-term mean motion across all landcover types in the survey area.
- Survey area: Approximately 930 km2 of blanket bog in the Flow Country, excluding surface water bodies and the sea.
- Data coverage: 6–12 day revisit cadence, collected from 12/03/2015 to 01/06/2019. Missing pixels are excluded due to low coherence; missing survey dates relate to processing issues or coherence gaps. Processing conducted by Terra Motion Ltd.

## Data and Coverage

- Sensor data: 410 Sentinel-1A and Sentinel-1B images (S1A/S1B), gathered every 6–12 days between 2015 and 2019.
- Outputs: For each georeferenced pixel, two time-series products at approximately 80 by 90 m resolution:
  - Multiannual average line-of-sight velocity (m/yr)
  - Mean velocity in the line-of-sight (LOS)

## Methodology and Processing

- Technique: Advanced Pixel System Intermittent Small Baseline Subset InSAR (APSIS), an adapted ISBAS/low-resolution SBAS-DInSAR time-series approach.
- Purpose: Improve survey point density and distribution in vegetated areas where coherence is typically challenging.
- Processing workflow:
  - In-house Punnet software used for co-registration of SLC data to time-series generation.
  - Baseline and coherence constraints: maximum horizontal baseline 250 m; maximum temporal separation 1 year; coherence threshold 0.25; point threshold 360.
  - Phase unwrapping: SNAPHU-based implementation.
- Reference frame: Motion measured relative to a stable reference point at Wick Airport (latitude/longitude given in document).

## Outputs and File Structure

- Time-series data: For each pixel location, a pair of georeferenced time-series products (approximately 80×90 m resolution).
- File naming and CRS:
  - Coordinate reference system: WGS84 UTM Zone 29N
  - Data values use no_data value -999; height units in meters
  - Time-series files: .tif with corresponding .aux files named by date (e.g., 20190701.tif, 20190701.tif.aux)
- Additional data products:
  - ortho_velocity_utm_isbas.tif = Mean LOS motion over the study period
  - ortho_velocity_utm_isbas_evv.tif = Corrected mean LOS motion over the study period
  - ortho_cohcount.tif = Number of coherent interferograms within each pixel
  - ortho_velocity_utm_verror.tif = Standard error of LOS motion (m/yr)

## Data Quality, Gaps, and Considerations

- Data gaps: Missing pixels due to low coherence; some survey dates missing due to processing issues.
- Coverage limitations: Resolution (~80×90 m) and LOS-only motion; no direct horizontal displacement provided.
- Scope: Masked out surface water bodies and sea; motion is relative to Wick Airport reference.

## References and Background

- Sentinel data (2015–2019) and ISBAS/APSIS methodology for InSAR processing.
- Foundational references include works on SBAS-DInSAR, ISBAS, coherence-velocity relationships, and time-series analysis of InSAR data (cited in the document).

## Appendix

- Appendix includes Table 1 detailing Sentinel-1 images used (capture of image IDs, dates, and file naming conventions).