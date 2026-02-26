# Survey Overview

- Interferometric Synthetic Aperture Radar (InSAR) measurements over Caithness and Sutherland to quantify peatland surface motion in the Flow Country.
- Uses the APSIS (Advanced Pixel System Intermittent Small Baseline Subset) InSAR technique, with two data products per georeferenced pixel: (1) time series of multiannual average line-of-sight velocity (m/yr) and (2) mean velocity in the line-of-sight.
- Data collected on a 6–12 day cycle from 12 March 2015 to 1 June 2019; missing pixels due to low coherence and missing survey dates due to processing issues or poor coherence; processing performed by Terra Motion Ltd.

## Survey Area

- Processing covers approximately 930 km2 of blanket bog in the Flow Country (Caithness and Sutherland), excluding surface water bodies and the sea.
- Area masked as land cover for the analysis; figure illustrating processing extent is referenced.

## Methodology

- Input data: 410 Sentinel-1A and Sentinel-1B IW (Interferometric Wide) images (orbit 125), acquired between 12 March 2015 and 1 June 2019.
- Processing framework: APSIS, an adapted low-resolution SBAS-DInSAR time-series algorithm, implemented via Terra Motion Ltd's Punnet software (co-registration of SLC data to time-series generation).
- Key parameters:
  - Maximum horizontal baseline: 250 m
  - Maximum temporal separation: 1 year
  - Coherence threshold: 0.25
  - Point threshold: 360
- Reference frame: Motion measured relative to a stable reference point at Wick Airport (58.4533° N, 3.0879° W).
- Phase unwrapping: In-house SNAPHU implementation.
- Output resolution: approximately 80 by 90 m per georeferenced pixel.
- Outputs: motion time series and mean velocity per pixel location.

## Data Products

- Primary products per pixel:
  - Motion time series of multiannual average LOS velocity (m/yr)
  - Mean LOS velocity over the study period
- Supporting/auxiliary products:
  - ortho_velocity_utm_isbas.tif (Mean LOS motion over the study period)
  - ortho_velocity_utm_isbas_evv.tif (Corrected mean vertical motion)
  - ortho_cohcount.tif (Number of coherent interferograms within each pixel)
  - ortho_velocity_utm_verror.tif (Standard error of LOS motion)
- Height files:
  - .tif and .aux files with relative land-surface height on a given date; filenames follow a date-based convention (e.g., 20190701.tif, 20190701.tif.aux).
- Height units: meters.

## File Naming Convention and CRS

- Coordinate reference system: WGS84 UTM Zone 29N
- No-data value: -999
- Time-series files: individual .tif files and corresponding .aux files; filenames include dates (YYYYMMDD), e.g., 20190701.tif and 20190701.tif.aux

## Data Source and Access

- Sentinel data provenance: Copernicus Open Access Hub; data processed by ESA.
- Data processing and methods are based on APSIS (and ISBAS) methodologies with cited literature.
- Data are provided to enable landscape-scale peatland motion assessment and reproducibility of results.

## Quality, Limitations, and Governance

- Data quality: missing pixels in areas of low coherence; some survey dates missing due to processing or coherence issues.
- Limitations: data gaps across time due to coherence constraints and processing issues; results are conditioned by baseline and coherence thresholds, and reference frame stability.
- Governance considerations for Data Stewards:
  - Clear documentation of data lineage: source Sentinel data, APSIS processing, Punnet implementation, SNAPHU for phase unwrapping.
  - Metadata should cover processing parameters (baselines, coherence thresholds, date ranges), reference point, and data quality flags (coherence-based gaps, verrors).
  - Structured data organization: separate time-series and auxiliary products with consistent file naming and CRS.
  - Open access data origin: Copernicus Sentinel data; ESA processing; suitable for reuse with proper attribution.

## References and Appendices

- Core references for data methods and processing are cited (ISBAS/APSIS methodology, SNAPHU, SBAS-DInSAR literature).
- Appendix includes an extensive list of Sentinel-1 acquisitions used (S1A and S1B across multiple dates), reflecting substantial input data for reproducibility and audit trails.