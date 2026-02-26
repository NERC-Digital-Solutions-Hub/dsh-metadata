# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

- A 1-km gridded dataset of daily and monthly rainfall estimates for Great Britain (GB), Northern Ireland (NI), and ~3000 km2 of catchment in the Republic of Ireland, extending from 1890 onwards with annual updates as new raingauge data become available.

- Derived from the Met Office national precipitation observations; daily/monthly grids produced via natural neighbour interpolation with SAAR-based normalization; daily rainfall is defined as rainfall over 24 hours from 09:00 on one day to 09:00 on the next.

- Developed to British Standards BS7843-4:2012 guidance.

- Detailed methodology and validation described in Keller et al. (2014).

## Data Sources

- Met Office MIDAS: definitive UK national daily and monthly rainfall totals; data provided to CEH monthly under licence; CEH maintains an in-house copy and syncs with MIDAS.
- Met Office SAAR grids: 1961-1990 standard period for GB (61-90) and for NI.
- Met Eireann 1-km SAAR grid for NI (61-90).

## Methodology

- Interpolation: natural neighbour interpolation with normalization by SAAR; no additional scale factor applied.

- Daily grids:
  - Stage 1: provisional daily grids using all available daily gauges.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so daily sums align with monthly grids (monthly data informs daily corrections; if a daily gauge shares coordinates with a monthly gauge, the monthly value is used).

- Monthly grids:
  - Generated from monthly raingauge totals and complete daily-monthly consistency; daily gauges with identical coordinates to monthly gauges are superseded by the monthly gauge.

- Minimum distance grids:
  - Distance to the closest gauge; a 100 km threshold is applied (no grid values beyond this) to ensure data representativeness.
  - Ancillary grids are produced to document gaps:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total days with missing data per grid point
  - Separate sets for monthly and daily data; updated yearly with new dataset versions.

## Data Quality and QC

- A 4-step QC procedure targets high (extreme) rainfall values using a 200-year return period reference rainfall (from the Flood Estimation Handbook model).

  1) Identify days where observed rainfall exceeds the reference value.
  2) Cross-check with records of major UK rainfall events; genuine if a match is found.
  3) Visually inspect days with no clear matches using daily rainfall maps (post-1961 GB); genuine if patterns show plausible large events.
  4) For remaining cases, compare time series with up to the 10 nearest gauges (downscaled to the three closest when time constraints apply); identify multiday accumulations or gauge reporting issues (false positives due to non-daily measurements).

- Outcomes in step 4:
  - Exclude cases with multiday accumulations (non-daily recording periods).
  - If neighboring gauges show much lower rainfall (<20%) within 10 km, reject the ORV.
  - Reject obvious extreme values (e.g., 469 mm, 999.9 mm).
  - Accept remaining ORVs (including those with no nearby gauges but consistent daily records).

- The QC process may remove data flagged by MIDAS as problematic due to incorrect flags, improving overall data reliability.

## Data Format and Structure

- Storage format: NetCDF4, following CEH gridded dataset conventions.
- Structure: yearly files; GB and NI stored separately; daily and monthly grids stored in distinct files.
- Core variables: rainfall amount (mm) and minimum distance (distance to the nearest gauge used for the estimate).
- Additional files:
  - Yearly missing data records (NetCDF4) indicating spatial/temporal extent of missing data.
  - Ancillary grids (NetCDF4) for monthly and daily data:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total days missing per grid point for the entire period

## Data Gaps, Coverage, and Usage Considerations

- Minimum distance threshold of 100 km means some remote areas (notably pre-1961 Scotland, Wales, SW England) have missing values.
- Pre-1961 networks were sparser, leading to geographical gaps in the early grids.
- Ancillary gap grids help modelers understand spatial-temporal coverage and plan analyses accordingly.

## Access, Updates, and Provenance

- Data updated annually as new raingauge data become available.
- Derived from Met Office data with quality control; distributed under licence terms with Met Office through CEH.
- Documentation and references provided for methodological choices and quality control procedures.

## References

- Collier, C.G., Fox, N.I., Hand, W.H. (2002). Extreme Rainfall and Flood Event Recognition. Technical Report FD2201. Defra/Environment Agency.
- Keller, V.D.J., et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use. Manuscript in Preparation.
- Spackman (1993). Calculation and Mapping of Rainfall Averages for 1961-90. British Hydrology Society Meeting.
- Stewart, E.J. et al. (2011). Reservoir Safety - Long Return Period Rainfall. CEH Project report.
- Svensson, C. et al. (2009). Data Consolidation. Defra project WS194/2/39.
- Walsh, S. (2012). New Long-term rainfall averages for Ireland. National Hydrology Conference Proceedings.