# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

- Overview
  - CEH-GEAR provides 1-km gridded daily and monthly rainfall estimates for Great Britain, Northern Ireland, and about 3000 km2 of catchment in the Republic of Ireland from 1890 onward.
  - Initially covers 1890–2012; planned to be extended annually as new raingauge data become available.
  - Estimates are derived from the Met Office national precipitation database; monthly values use monthly and complete-month daily totals; daily values interpolate daily using all available raingauges.
  - Normalisation by average annual rainfall (SAAR) and natural neighbour interpolation are used to generate grids.
  - Daily rainfall refers to precipitation within 24 hours from 09:00 on day t to 09:00 GMT on day t+1.

- Data sources
  - Met Office MIDAS national daily and monthly totals; CEH maintains a synchronized copy in its Oracle database; quality control (QC) discards unrealistic extremes.
  - Met Office SAAR 61-90 1-km grids for GB; Met Eireann 61-90 1-km SAAR grid for NI.
  - All data compiled and QC procedures designed to ensure reliability for hydrological applications.

- Method for deriving daily and monthly grids
  - Interpolation: natural neighbour interpolation with SAAR normalisation (no scale-factor variation due to limited improvement).
  - Daily grids (two-stage process):
    - Stage 1: provisional daily grids via natural neighbour interpolation using all available daily gauges.
    - Stage 2: adjust provisional daily grids with a monthly correction factor so daily sums align with the monthly grids.
  - Monthly grids:
    - Generated from the monthly raingauge network; for months with complete daily data, daily gauges sum to monthly totals; if a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used in interpolation.
  - Daily vs monthly data integration:
    - Daily grids incorporate information from monthly grids, especially in remote areas with few daily gauges, by using the monthly correction factor.

- Minimum distance grids
  - A minimum distance threshold of 100 km is applied; grid points farther than this are not estimated to ensure representativeness.
  - Ancillary grids are provided to indicate spatial/temporal gaps:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total number of missing days per grid point for the full period
  - Separate sets exist for monthly and daily data.

- Quality control (QC)
  - A four-step QC processes identify and reject implausible high rainfalls using a 200-year return-period rainfall reference.
    - Step 1: Flag days/gauges exceeding the reference rainfall.
    - Steps 2–4: Validate flagged values against known extreme rainfall events, visual inspection of daily rainfall maps (post-1961 GB), and time-series comparisons with nearby gauges (up to ten gauges, then up to more if needed).
  - Key QC outcomes:
    - Multiday accumulation issues and inconsistent recording (e.g., weekly measurements) are rejected.
    - Cases with large discrepancies (e.g., neighboring gauges showing much lower rainfall) are rejected.
    - Extremely large values are rejected.
    - Remaining flagged values with consistent daily records may be accepted.
  - Consequence: data flagged and affected periods are removed from the rainfall database used to produce grids.

- Format and structure
  - Data stored in NetCDF4 format following CEH gridded data conventions.
  - Structure:
    - Yearly files; GB and NI in separate folders; daily and monthly grids stored separately.
    - Core variables: rainfall amount and minimum distance to the nearest gauge.
    - Ancillary missing data grids (year-of-first/last missing data, total missing days) in NetCDF4; mirrored in annual summaries.
  - Purpose: designed for hydrological modelling and scientific analyses requiring gridded rainfall fields with documented data quality and gaps.

- Uses, limitations, and references
  - Intended for hydrological use and modelling; annually updated with new data as available.
  - Limitations include sparser gauge networks pre-1961 (notable in Scotland, Wales, southwest England) leading to missing data in early grids; representativeness degrades with distance beyond 100 km.
  - References used for QC and methodology include: Collier et al. 2002; Keller et al. 2015; Spackman 1993; Stewart et al. 2011; Svensson et al. 2009; Walsh 2012.
  - Detailed methodology and data description available in Keller et al. (2014) and related CEH-GEAR documentation.