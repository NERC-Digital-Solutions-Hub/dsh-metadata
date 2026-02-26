# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

- Overview
  - A gridded rainfall dataset at 1-km resolution for Great Britain, Northern Ireland, and a ~3000 km² catchment in the Republic of Ireland, covering from 1890 onwards with initial coverage through 2012 and extending annually as new raingauge data become available.
  - Provides daily and monthly rainfall estimates in millimetres, derived from the Met Office observation network and processed to align with hydrological needs and standards (BS7843-4:2012).

- Data Coverage and Timeframe
  - Geographic scope: GB, NI, and ROI catchment area.
  - Timeframe: began 1890, with ongoing annual updates.
  - Temporal definition: daily rainfall refers to precipitation accumulated over 24 hours from 09:00 on a day to 09:00 the next day.

- Data Sources
  - Met Office MIDAS daily and monthly station totals; CEH maintains a synchronized copy in an ORACLE database.
  - Met Office SAAR grids for 1961–1990 (GB) and Met Eireann SAAR grids for NI.
  - Quality control procedures applied to remove unrealistic extremes and ensure data integrity.

- Derivation Method and Interpolation
  - Interpolation: natural neighbour interpolation with normalization by SAAR rainfall to create consistent daily and monthly grids.
  - Monthly grids: built from monthly raingauge data; when a daily gauge shares coordinates with a monthly gauge, the monthly value is used to avoid double counting.
  - Daily grids: produced via a two-stage process:
    1) provisional daily grids from natural neighbour interpolation using daily gauges.
    2) adjustment by a monthly correction factor to ensure daily grids sum to the monthly grids, incorporating information from monthly data in remote areas.
  - Data represent rainfall depth in millimetres.

- Minimum Distance Grids and Data Gaps
  - Minimum distance threshold for gauge influence: 100 km; grid points beyond this distance are not calculated.
  - This threshold helps maintain spatial representativeness, especially in sparsely gauged areas and earlier periods with lower station density.
  - Ancillary grids (monthly and daily) provide:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total number of missing days per grid point for the entire period
  - Early grids (pre-1961) may have more gaps due to sparser networks.

- Quality Control and Data Validation
  - A 4-step QC procedure rejects unrealistically high daily values and ensures reliability:
    - Step 1: identify days where reference 200-year rainfall is exceeded.
    - Step 2: cross-check high values against known major rainfall events.
    - Step 3: visually inspect maps for suspicious patterns; keep if pattern supports a genuine extreme.
    - Step 4: compare with up to the nearest gauges via time-series analysis; reject multiday accumulations and cases where nearby gauges show inconsistencies or data flags are questionable.
  - Rejections include multiday accumulations, large discrepancies with neighboring gauges, and extreme single-point values (e.g., 469 mm, 999.9 mm).
  - Inconsistent periods are removed from the rainfall database used for grid generation.

- Data Format and Structure
  - Storage format: NetCDF4, following CEH gridded dataset conventions.
  - Organization: yearly files; separate files for GB and NI; daily and monthly grids stored separately within each region.
  - Core variables: rainfall amount (mm) and minimum distance to the gauge (m).
  - Ancillary data: yearly missing records files (NetCDF4) plus three sets of ancillary grids (monthly and daily) describing missing data extents.
  - Data accessibility: NetCDF4 format suitable for GIS workflows and hydrological modelling.

- Practical Considerations for GIS Specialists
  - High-resolution, map-friendly 1-km grids enable detailed spatial analyses and map-based data visualisations for policy, client, and public audiences.
  - The minimum distance grids and missing-data ancillary grids help users assess data coverage, reliability, and limitations across space and time.
  - The two-stage daily grid construction allows daily estimates to be informed by monthly data, improving stability in data-sparse regions.
  - QA processes provide transparency on data quality and potential gaps, important for hydrological modelling and risk assessment.
  - Compliance with established standards (BS7843-4:2012) supports interoperability and data integrity in GIS applications.

- References
  - Includes foundational works and project reports related to data sources, QA procedures, and methodology (Collier et al., Keller et al., Spackman, Stewart et al., Svensson et al., Walsh).