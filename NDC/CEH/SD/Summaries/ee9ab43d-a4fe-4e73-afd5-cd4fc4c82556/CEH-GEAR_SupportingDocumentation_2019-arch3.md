# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

## Overview
- Provides 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3,000 km2 of catchment in the Republic of Ireland, from 1890 onwards.
- Updated annually as new raingauge data become available.
- Rainfall estimates are in millimetres (mm) and defined as rainfall accumulated over 24 hours from 09:00 on day D to 09:00 on day D+1.
- Dataset designed to support hydrological and environmental monitoring, with metadata and data governance considerations.

## Data access and licensing
- Data accessible via DOIs:
  - Access: https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
  - Citation required: Tanguy et al. 2016 (CEH-GEAR) with full citation at https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
  - Full licensing and reuse conditions: https://doi.org/10.5285/ee9ab43da4fe-4e73-afd5-cd4fc4c82556
- Emphasises data sharing and transparency, with clear citation requirements.

## Dataset description
- Coverage and content:
  - 1-km resolution daily and monthly areal rainfall estimates for GB and NI; ~3,000 km2 of ROI catchment included.
  - Initially 1890–2012; extended annually as new data arrive.
  - Core variables: rainfall amount (mm) and minimum distance to gauge used for estimation.
- Data structure:
  - NetCDF4 format, yearly files; separate files for GB and NI, with daily and monthly grids stored separately.
  - Includes missing-data indicators and ancillary grids to describe data gaps.

## Data sources
- Primary raingauge data:
  - Met Office MIDAS database (daily and monthly totals; licensed to CEH; QC applied to remove unrealistic extremes).
- Baseline high-resolution grids used for normalisation:
  - SAAR 61-90 grids for Great Britain (Spackman 1993) and Northern Ireland (Walsh 2012).
- Underlying methodological framework aligned with established hydrological guidance (e.g., British Standards BS7843-4:2012; Flood Estimation Handbook references).

## Methodology (daily and monthly grids)
- Interpolation approach:
  - Natural neighbour interpolation across all available raingauges, normalised by SAAR.
  - Daily grids: two-stage process
    1) Provisional daily grids via natural neighbour interpolation.
    2) Adjustment using a monthly correction factor so daily sums match monthly grids.
  - Monthly grids: based on monthly raingauge network; monthly totals used as reference for daily corrections.
- Data usage rules:
  - If a daily and monthly gauge share coordinates, monthly value is used for interpolation.
  - Daily grids rely on a complete month of daily data; otherwise, a proxy via monthly data is used for correction.
- Representativeness and coverage:
  - Minimum distance threshold of 100 km; grid values are not produced if the nearest gauge is farther than 100 km.
  - Aims to balance accuracy with spatial coverage.

## Quality control (QC)
- Purpose: identify and reject unrealistically high daily rainfall values.
- Four-step QC process using a 200-year return-period rainfall reference (FD/WEF model):
  1) Flag days/gauges exceeding the reference value.
  2) Cross-check flagged values against major UK rainfall events database.
  3) Visual assessment with post-1961 daily rainfall maps to judge plausibility.
  4) Time-series comparisons with up to 10 nearby gauges to confirm consistency; multiday accumulations and data flags issues often lead to rejection.
- Rejection criteria include:
  - Multiday accumulation issues, inconsistent data flags, near-total disagreement with neighboring gauges, and extreme values (e.g., implausible single-day spikes).
- Outcome: only credible observed rainfall values are retained for grid generation.

## Format and structure
- NetCDF4 datasets:
  - Yearly files; GB and NI stored separately; daily and monthly grids separated.
  - Core variables: rainfall amount and minimum distance to the gauge.
- Missing data metadata:
  - Yearly missing-records NetCDF4 files accompany the core data.
  - Ancillary grids (monthly and daily) provide:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total number of missing days per grid point
- Ancillary data help users assess spatial and temporal data coverage and gaps.

## Data gaps and governance for monitoring frameworks
- Data gaps:
  - Pre-1961 data sparser; minimum distance rule results in gaps, especially in Scotland, Wales, and SW England.
- Ancillary indicators:
  - Three sets of ancillary grids per data type (monthly and daily) to communicate gap timing and extent.
- Governance and usability:
  - Clear licensing, citation, and data provenance support transparent monitoring and audit trails.
  - Metadata-rich structure facilitates data quality assessment and reproducibility in policy monitoring.

## Practical implications for monitoring frameworks
- Enables standardized, high-resolution areal rainfall inputs for hydrological and environmental policy assessment.
- Supports trend analysis, flood risk assessment, and climate monitoring across GB, NI, and ROI catchments.
- QC and metadata conventions enhance trust and comparability across monitoring programmes.
- The 100 km representativeness threshold and pre-1961 gaps should be considered when interpreting historical trends or performing regional analyses.

## Limitations and caveats
- Coverage limitations before 1961 and in regions with sparse gauge networks.
- 100 km minimum-distance rule may omit certain areas from daily rainfall grids.
- Interpolation and normalisation choices (natural neighbour + SAAR) introduce model-based uncertainties.
- Some daily values flagged as questionable may still propagate into analyses if not properly accounted for.

## References (key sources)
- Keller, V. D. J. et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
- Spackman, 1993; Walsh, 2012 (SAAR grids).
- Collier, C. G. et al. (2002); Stewart, E. J. et al. (2011); Svensson, C. et al. (2009).