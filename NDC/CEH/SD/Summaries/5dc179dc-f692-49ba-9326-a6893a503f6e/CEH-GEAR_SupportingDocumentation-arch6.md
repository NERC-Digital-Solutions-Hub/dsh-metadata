# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

- 1-km gridded daily and monthly rainfall estimates for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km² of catchment in the Republic of Ireland, covering from 1890 onwards; initial coverage 1890–2012 with annual extensions as new raingauge data become available.

- Estimates derived from Met Office observed precipitation data, interpolated using natural neighbour methodology with SAAR-based normalisation.

- Estimates refer to rainfall accumulated over 24 hours from 09:00 on a given day to 09:00 GMT the next day. Monthly estimates use monthly totals from the UK raingauge network; daily estimates use daily gauges, with adjustments to align daily grids to monthly totals.

## Data Sources

- Met Office MIDAS: definitive UK daily and monthly totals; QC procedures used to discard unrealistic extremes.
- SAAR 1961–1990 1-km grids:
  - GB SAAR 61-90
  - NI SAAR 61-90 (Met Éireann)
- CEH maintains a synced copy of MIDAS in an Oracle database for processing.

## Method for Deriving Daily and Monthly Grids

- Interpolation: natural neighbour interpolation with SAAR normalisation; no varying scale factor for normalisation chosen.
- Grid generation:
  - Monthly grids: derived from monthly gauges and daily gauges from the complete month; if a daily gauge shares coordinates with a monthly gauge, the monthly value is used.
  - Daily grids: two-stage process
    1) provisional daily grids via natural neighbour interpolation using daily gauges.
    2) adjustment by a monthly correction factor so the sum of daily grids matches the monthly grid.
- Units: rainfall depth in millimetres (mm).

## Minimum Distance Grids and Gap Ancillary Grids

- Minimum distance: distance to the closest gauge used (threshold of 100 km). Grids are not computed if the nearest gauge is >100 km away to preserve representativeness.
- Early grids (pre-1961) have geographical gaps, especially in Scotland, Wales, and SW England.
- Ancillary grids (monthly and daily; updated yearly) providing gap context:
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of missing days per grid point over the full period

## Quality Control

- Four-step QC to identify and reject erroneous high values (200-year return period rainfall reference from the Flood Estimation Handbook):
  1) Flag days/gauges exceeding reference rainfall.
  2) Cross-check flagged events against major UK rainfall event database.
  3) Visual assessment using available daily rainfall maps (post-1961 GB data) to judge plausibility.
  4) Time-series comparison with up to ten nearby gauges (prioritising three, then up to seven more) to confirm plausibility; identify multiday accumulations or data recording quirks; reject those cases.
- Specific rejection criteria:
  - Multiday accumulation values flagged as not suitable (e.g., gauges with periodic sampling).
  - If nearby gauges within 10 km show much lower rainfall (<20%), flag or reject the ORV.
  - Extreme values (e.g., 469 mm, 999.9 mm) rejected.
  - If unresolved, data for the identified periods are removed from the dataset used to produce grids.

## Data Format and Accessibility

- Storage format: NetCDF4, following CEH gridded dataset conventions.
- Structure: yearly files, separate files for GB and NI; daily and monthly grids stored separately.
- Core variables: rainfall amount and minimum distance (distance to the closest gauge used).
- Missing data: yearly missing records files (NetCDF4) plus three ancillary grids (monthly and daily) describing gaps as above.
- Output includes both the core gridded data and metadata about missing data and gauge proximity to support modelling and gap assessment.

## Usage, Updates, and References

- Designed to support hydrological use and wider data analyses; suitable for modelling and derivation of self-serve data products.
- Updated annually as new raingauge data become available.
- References provided for methodology and validation, including Collier et al. (data consolidation and reservoir safety rainfall concepts) and Keller et al. (CEH-GEAR description manuscript).