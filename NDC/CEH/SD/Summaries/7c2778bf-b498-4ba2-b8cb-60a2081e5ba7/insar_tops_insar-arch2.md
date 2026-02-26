# Survey Overview

- Objective: measure peatland surface motion across Caithness and Sutherland in the Flow Country using Intermittent Small Baseline Subset InSAR (APSIS) to produce timeseries of peat surface height and long-term mean motion.
- Cadence and period: data collected every 6–12 days on 410 Sentinel-1A/B images from 12/03/2015 to 01/06/2019; missing pixels excluded due to low coherence; some survey dates missing due to processing issues or poor coherence.
- Processing authority: Terra Motion Ltd.

## Survey Area

- Area: approximately 930 km2 of blanket bog in the Flow Country (Caithness and Sutherland).
- Masking: surface water bodies and the sea removed prior to processing.

## Methodology

- Data sources: 410 Sentinel-1A and Sentinel-1B images (Orbit 125), sourced from the European Space Agency Copernicus Open Access Hub.
- InSAR technique: APSIS (formerly ISBAS) to improve density and distribution of survey points, enabling measurements in vegetated areas where standard DInSAR struggles.
- Processing workflow: co-registration of SLCs, time-series generation using Terra Motion in-house Punnet software; SNAPHU for phase unwrapping.
- Spatial/temporal constraints: maximum horizontal baseline 250 m; maximum temporal separation 1 year; coherence threshold 0.25; point threshold 360.
- Reference: motion measured relative to a stable reference point at Wick Airport (58.4533° N, 3.0879° W).

## Outputs and Resolution

- Pixel-level products (for each georeferenced pixel): 
  - Time series of multiannual average line-of-sight velocity (m/yr).
  - Mean velocity in the line-of-sight (m/yr).
- Spatial resolution: approximately 80 by 90 m.
- Additional outputs: ortho_velocity_utm_isbas.tif (mean LOS motion), ortho_velocity_utm_isbas_evv.tif (corrected mean vertical motion), ortho_cohcount.tif (coherent interferograms per pixel), ortho_velocity_utm_verror.tif (standard error of LOS motion).

## Data Formats and Naming

- Coordinate reference system: WGS84 UTM Zone 29N.
- No-data: -999.
- Time-series files: individual .tif files with corresponding .aux files; filenames reflect dates, e.g., 20190701.tif and 20190701.tif.aux.
- Height data: stored as per-date height values in meters.
- Example auxiliary outputs: ortho_velocity_utm_isbas.tif, ortho_cohcount.tif, veror.tif.

## Data Sources and References

- Primary data: Copernicus Sentinel data (2015–2019) from the ESA hub (S1A and S1B).
- Key references for APSIS/ISBAS methods and related processing: Bateson et al. (2015), Chen & Zebker (2001), Gong et al. (2016), Osmanoglu et al. (2016), Sowter et al. (2016).

## Quality, Limitations, and Access

- Data quality: missing pixels due to low coherence; some survey dates missing due to processing issues or coherence problems.
- Coverage: processing area excludes water bodies and sea; applies to vegetated peatland within the Flow Country.
- Data handling: datasets are stored and uploaded to appropriate portals; outputs ready for integration with standard environmental monitoring and policy performance formats.

## Appendices and Data Inventory

- Appendix contains a detailed table of Sentinel-1 images used (S1A/S1B, dates, file names) across the survey period, illustrating data provenance and coverage.