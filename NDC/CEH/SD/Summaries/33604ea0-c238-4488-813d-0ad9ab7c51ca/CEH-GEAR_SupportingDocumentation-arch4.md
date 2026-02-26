# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

- Purpose and scope
  - CEH-GEAR provides 1-km gridded estimates of daily and monthly rainfall for Great Britain, Northern Ireland, and ~3000 km² in the Republic of Ireland from 1890 onward, with annual updates as new raingauge data become available.
  - Daily precipitation is defined as rainfall within 24 hours from 09:00 on a day to 09:00 GTM the next day.

- Data sources
  - Met Office MIDAS national dataset (daily and monthly totals), accessed under licence and synchronized with CEH’s ORACLE database; quality control discards unrealistic extremes.
  - Met Office SAAR (1951-1990 standard period) 1-km grid for GB (Spackman, 1993).
  - Met Éireann SAAR 1-km grid for Northern Ireland (Walsh, 2012).

- Method for deriving grids
  - Interpolation: natural neighbour interpolation with normalisation by SAAR values.
  - Normalisation: fixed SAAR-based scale; no varying-scale factor due to marginal improvements.
  - Daily grids: two-stage process – (1) provisional daily grids from all available gauges; (2) adjust with a monthly correction factor to ensure consistency with monthly grids.
  - Monthly grids: derived from monthly totals (or complete daily months) and used to inform daily corrections; if a daily gauge shares coordinates with a monthly gauge, the monthly value is used.

- Data processing and quality controls
  - Quality control uses a 200-year rainfall reference (from the Flood Estimation Handbook DF) to identify potential outliers.
  - Four-step QC procedure per gauge:
    - Flag potential extreme days exceeding reference rainfall.
    - Cross-check high values against major UK rainfall events database.
    - Visually inspect days with maps for post-1961 GB data; assess plausibility.
    - Time-series comparisons with up to ten nearby gauges; remove data from multiday accumulations or inconsistent measurements; reject extreme single-point values where justified.
  - Multiday accumulation and data flag issues can lead to rejection of certain gauges or periods, ensuring grids are built from consistent daily records.

- Minimum distance grids and gap reporting
  - Minimum distance threshold set at 100 km; grid points with no gauge within this distance are not calculated.
  - Ancillary grids provided to quantify gaps:
    - Year of first missing data for each grid point (monthly and daily).
    - Year of last missing data for each grid point (monthly and daily).
    - Total number of missing days per grid point (whole period).

- Data format and organization
  - Core data stored in NetCDF4 format, following CEH conventions.
  - Yearly files; separate folders for Great Britain and Northern Ireland; separate subfolders for daily and monthly grids.
  - Core variables: rainfall amount (mm) and minimum distance to gauge used.
  - Ancillary grids (NetCDF4): annual missing-data extents (first/last missing year, total missing days) for both monthly and daily data.

- Data governance and reproducibility
  - Dataset developed under guidance from BS7843-4:2012 to ensure appropriate data handling and quality standards.
  - In-sync master dataset with Met Office MIDAS; procedures exist to maintain alignment.
  - Documentation and references provided to enable traceability and reproducibility (including Keller et al. 2015; Spackman 1993; Stewart et al. 2011; Svensson et al. 2009; Walsh 2012; Collier et al. 2002).

- Practical considerations and limitations for data leaders
  - Coverage gaps are more pronounced pre-1961 due to sparser network density, reflected in missing data grids and higher reliance on interpolation.
  - The 100 km minimum-distance rule means some regions are not represented by gridded values and require interpretation of gap-related ancillary data.
  - Normalisation by SAAR ensures monthly totals are preserved, but daily estimates rely on the density and quality of daily raingauge networks.
  - Data handling includes rigorous QC to minimize false highs, but users should be aware of potential residual uncertainties in early periods and in regions with sparse gauge coverage.

- References
  - Collier, C. G., Fox, N. I. and Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition.
  - Keller, V. D. J., et al. (2015). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
  - Spackman, (1993). Calculation and Mapping of Rainfall Averages for 1961-90.
  - Stewart, E. J., et al. (2011). Reservoir Safety - Long Return Period Rainfall.
  - Svensson, C., et al. (2009). Data Consolidation for Reservoir Safety.
  - Walsh, S. (2012). New Long-term rainfall averages for Ireland.