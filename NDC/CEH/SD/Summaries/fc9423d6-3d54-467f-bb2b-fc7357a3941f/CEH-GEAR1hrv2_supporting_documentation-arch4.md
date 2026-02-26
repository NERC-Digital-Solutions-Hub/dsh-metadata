# Data access and citation

- The CEH-GEAR1hr.v2 dataset provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onward, currently covering 1990–2016 with ongoing updates as new raingauge data become available.
- Data are available from the Environmental Information Data Centre and must be cited as described below.

## Overview

- Version: CEH-GEAR1hr.v2 (updated hourly rainfall dataset for GB)
- Purpose: designed for hydrological modelling; supports hourly rainfall analysis with attached metadata about data provenance and processing.
- Citation requirements:
  - Data citation: Lewis, E.; Quinn, N.; Blenkinsop, S.; et al. (2020). Gridded estimates of hourly areal rainfall for Great Britain - version 2 (1990-2016) [CEH-GEAR1hr.v2].
  - Methodology reference: Lewis et al. (2018) for the rule-based QC method underpinning the hourly dataset.
  - Data source references and DOIs provided in the release notes.

## Data sources and coverage

- Gauges: 2,606 UK rain gauges from multiple agencies (MO/MIDAS, England Environment Agency, NRW, SEPA).
- Daily and hourly data streams:
  - Daily CEH-GEAR rainfall data (used as the base for disaggregation)
  - Hourly gauge data from Met Office MIDAS, EA WISKI, NRW WISKI, and SEPA WISKI
- Quality control: a systematic QC procedure applied to hourly gauge data to discard suspect values
- Period and density: gauge network expanded in v2 relative to v1, with up to ~500 extra gauges on certain days

## Data processing and methodology

- Core approach:
  - Hourly grids derived by disaggregating CEH-GEAR daily rainfall data using hourly gauge data.
  - Nearest-neighbour interpolation on a 1-km grid to preserve observed storm shapes.
  - If the nearest hourly gauge is >50 km away, or there is daily rainfall with no corresponding hourly rainfall, a statistical disaggregation (average storm shape) is used.
- Statistical disaggregation:
  - Table 1 provides average hourly fractions (storm shapes) for different daily totals and seasons.
  - Disaggregation generally begins at 9:00 hours when applied.
- Minimum distance grids:
  - For each grid cell/day, the distance to the nearest gauge is stored (Min_dist).
  - A 50 km distance threshold is applied; grids farther than this are not calculated and may use statistical disaggregation.
- Data products and metadata:
  - Each daily file indicates whether statistical disaggregation was used (Stat_disag).
  - Min_dist is stored in the NetCDF file alongside rainfall values.
- Quality control:
  - Three-step QC process (gauge comparison to CEH-GEAR daily data; automated QC tests; rule-based exclusion).
  - QC flags (Table 2) and a rule base (Table 3) determine which values are removed (replaced with -999).
  - Gauges and time steps retained only if correlation criteria are met (Spearman rs > 0.8 and P00+P11 > 0.8).
- Quality and rejection statistics:
  - v2 applies stricter rule-based rejection; large volumes of data are flagged and removed as per the rule base.
- Example storms:
  - Illustrate how gauge proximity affects hourly estimates and the use of statistical disaggregation on days with sparse gauge coverage.
- Format and structure:
  - NetCDF4 format, CEH gridded conventions, monthly files named CEH-GEAR-1hr.v2_YYYYMM.
  - Variables per file: Rainfall_amount (hourly rainfall in mm), Stat_disag (0/1), Min_dist (m).

## Data format and access

- File structure: monthly NetCDF4 files (CEH-GEAR-1hr.v2_YYYYMM).
- Variables:
  - Rainfall_amount: hourly rainfall (kg/m^2, equivalent to mm)
  - Stat_disag: indicates if statistical disaggregation was used (1) or not (0)
  - Min_dist: distance to the nearest hourly gauge used for derivation (m)
- Time metadata:
  - time_coverage_resolution = P1H (hourly)
  - time_coverage_duration = P27Y (27 years)
- Access and use:
  - Metadata and citations are essential; the dataset is intended for hydrological modelling and related analyses.
  - Users should account for diurnal shaping introduced by statistical disaggregation and the potential blocky spatial patterns from nearest-neighbour interpolation.

## Appropriate use and limitations

- Designed for hydrological modelling; analyses involving the diurnal cycle or trends should account for processing steps that impose a predefined daily-to-hourly distribution.
- Nearest-neighbour interpolation can create abrupt spatial transitions; non-smoothing between gauges may affect spatial analyses.
- Statistical disaggregation is used in specific grid cells (e.g., far from gauges or daily-only rain events) and can influence diurnal-cycle interpretations.
- Metadata should be consulted to understand when and how disaggregation was applied for any given grid cell and day.

## Data quality, governance, and provenance

- Quality assurance:
  - Comprehensive QC flags and automated rule-based exclusions to improve data reliability.
  - Post-QC correlation criteria ensure selected gauges contribute high-quality data.
- Provenance:
  - Data originate from multiple national agencies and Met Office data archives; detailed attribution is provided in the release.
  - Acknowledgments highlight funding and collaborations (e.g., SINATRA, CONVEX, Hydro-JULES).

## Usage guidance and caveats for Data Leaders

- Ensure correct citation of both the dataset and the methodology when using CEH-GEAR1hr.v2.
- Leverage the Min_dist and Stat_disag metadata to assess the reliability of hourly estimates at specific grid cells and times.
- When integrating with organisational data governance, document the data lineage from primary gauges through the QC steps to the final hourly grids.
- Consider potential biases introduced by diurnal-shape imposition and spatial non-smoothing when communicating results to policy colleagues or external partners.

## Acknowledgements and references

- Funding and data providers acknowledged (SINATRA, CONVEX, INTENSE, Hydro-JULES; MO, EA, NRW, SEPA, Met Office).
- Primary references:
  - Lewis et al. (2018) on the QC method (Journal of Hydrology)
  - Keller et al. (2015); Tanguy et al. (2019) for CEH-GEAR
  - Lewis et al. (2020) CEH-GEAR1hr.v2 data descriptor
- Data citations and DOIs provided in the release notes.