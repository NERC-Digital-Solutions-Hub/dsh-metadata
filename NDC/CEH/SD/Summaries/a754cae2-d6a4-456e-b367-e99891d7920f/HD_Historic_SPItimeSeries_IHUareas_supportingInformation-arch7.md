# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

- Purpose and content
  - Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas.
  - SPI calculated for multiple accumulation periods (1, 3, 6, 9, 12, 18, 24 months) across all calendar months.
  - Data stored as CSV, designed to support map-based GIS analyses and portal integration (CEH droughts portal).

- Spatial and temporal scope
  - Time period: 1862–2015; baseline period for distribution fitting: 1961–2010.
  - Spatial units: IHU hydrometric areas (coarsest IHU resolution). Each record linked to a hydrometric area by POLYGONID.

- Data structure and format
  - File format: CSV with 10 columns.
  - Key fields: RID (row ID), POLYGONID (IHU area ID), THEDATETIME (date), plus 7×12 SPI aggregations (84 time series) across durations and months.
  - SPI values are normal scores (mean 0, SD 1), units-less, clipped to the range -5 to +5. Missing data encoded as -9999.

- Data sources and underpinnings
  - SPI data derived from Met Office 5 km monthly rainfall grids (historic digitised rainfall data included; updated for 1960–2000).
  - IHU hydrometric areas used as spatial units.
  - Historical rainfall data supplemented by multiple sources (1910–1959 UKCP09, 1960–2000 daily-derived grids, 2012–2015 updates, and rescued data 1862–1909).

- Methodology and calculations
  - SPI computed as per McKee et al. (1993): fits a gamma distribution to precipitation accumulations, then transforms to a standard normal distribution.
  - Gamma parameters estimated with L-moments (via modified SCI R package) instead of maximum likelihood.
  - For accumulation periods > 12 months, overlapping data introduce autocorrelation; serial correlation considerations noted.
  - Extreme SPI values truncated at ±5 due to uncertainty at distribution tails.
  - Note: gamma distribution is still widely used for Europe; newer distributions (e.g., Pearson type III, Tweedie) may be explored in future updates.

- Changes in version 2
  - Underlying rainfall data updated to Met Office 5 km grids (instead of CEH-GEAR-based data).
  - New monthly rainfall grids derived for 1960–2000; 9-month accumulation period added.
  - Overall methodology for SPI remains consistent with prior version.

- Applications and use within GIS
  - Enables aggregation of SPI over specific geographic areas (IHU hydrometric areas) to study drought history and trends.
  - Suitable for map-based visualisation and integration into drought portals; compatible with joining to IHU shapefiles via POLYGONID.

- Data quality, caveats, and interpretation
  - Serial autocorrelation present for long-duration SPIs due to overlapping time periods.
  - The independence assumption for standard frequency analysis is not met for long-duration SPI series; trend analyses should account for autocorrelation.
  - Interpretation depends on accumulation period: short-term (1–3 months) reflects immediate moisture stress; longer-term (12–24 months) relates to hydrological impacts like reservoirs and groundwater.

- Acknowledgments and references
  - Results produced through DrIVER and Historic Droughts projects; contributions from multiple UK institutions and the Met Office.