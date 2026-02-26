# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015)

## Scope and purpose
- Provides Standardised Streamflow Index (SSI) data for 303 UK catchments to assess hydrological drought and rare/high-flow events.
- SSI is calculated for accumulation periods of 1, 3, 6, 9, 12, 18 and 24 months, assigned to the end of each accumulation period.
- Aims to enable cross-catchment drought analysis and support drought management and planning tool development.

## Data origin and project context
- Derived from Historic Droughts project (2014–2018), a cross-disciplinary UK effort funded to understand past droughts and improve management tools.
- Involves eight UK institutions and combines hydrometeorological, environmental, regulatory, and social perspectives.
- SSI data built on historic reconstructions of daily river flow for 303 catchments (1891–2015).

## Data & methods (how SSI is produced)
- Daily streamflow: modelled reconstructions (1891–2015) with naturalised calibrations; used where available, otherwise modelled data; 305 daily series in total.
- SSI calculation: for each catchment and accumulation period, fit a Tweedie distribution to monthly aggregated flows; transform to normal scores (mean 0, sd 1) to obtain unitless SSIs.
- Software: R SCI package with a Tweedie extension to compute SSI.
- Data transformation: SSIs are "normal scores" with no units; values clipped to the range [-5, 5] to limit extreme tail effects.
- Time window for distribution fitting: Tweedie parameters fitted using 1961–2010 standard period (to align with SPI products).
- Temporal scope: SSI series cover January 1891 to November 2015.
- Autocorrelation caveat: for accumulation periods >12 months, overlapping data cause autocorrelation; SSI values reflect relative severity within the same series but independence assumptions for frequency analysis are violated.

## Accumulation periods and interpretation
- SSI-1, SSI-3, SSI-6, SSI-9, SSI-12, SSI-18, SSI-24 computed for every calendar month end.
- Example: SSI-6 for July 1998 uses flow from February 1998 to July 1998.
- Negative SSI indicates drier-than-average conditions; positive SSI indicates wetter-than-average conditions; more extreme values (towards -5 or +5) indicate rarer events.

## Data formats and file structure
- Format: CSV files, one per catchment (305 files for 303 catchments; 1891–2015 data).
- File naming: HD_SSI-CatchID-189101-201511.csv (Catchid matches NRFA ID; periods indicated by column headers).
- Each file includes the seven accumulation-period columns (1, 3, 6, 9, 12, 18, 24) with values as normal scores and no units.
- Missing data: encoded as -999; start of series includes initial missing months due to accumulation periods; some catchments have larger blocks of missing data.

## Missing data and data quality notes
- Two catchments (31023 West Glen at Easton Wood; 39017 Rey at Grendon Underwood) have substantial missing data because Tweedie could not be fitted for certain calendar months; totals of missing values and affected months detailed in Table 2.
- Additional missing values where Tweedie fitting failed for some months (Table 3) and overall minor missing value occurrences summarized in Appendix Table A1.
- Overall completeness: large portion of catchments have usable SSI data, but several have notable gaps requiring careful handling in analyses.

## Catchment metadata and accessibility
- HD_SSI_CatchInfo.csv provides catchment-level metadata:
  - Catchid, NRFACatchmentName, Area_sqkm, Nested flag, UKBN2_LFBN flag (low-flow suitability), NRFA_StationPage URL.
- Data are linked to the NRFA station pages for catchment-specific context and data sources.

## Documentation, acknowledgements, and references
- Acknowledged as an outcome of the Historic Droughts Project (grant NE/L01016X/1).
- Detailed methodological references include foundational works on SPI/SSI, Tweedie modeling, and UK drought characterization.

## Practical considerations for data reuse (Data Support orientation)
- Suitable for cross-catchment drought comparisons, trend analysis, and dashboard-style data products to enable self-serve exploration.
- Consider data quality and missing values per catchment; account for modelled vs observed data provenance.
- When aggregating or comparing accumulation periods, be mindful of autocorrelation issues for SSI-18 and SSI-24 due to overlapping data windows.
- Use the catchment metadata file to select catchments by characteristics (area, low-flow suitability, nesting) and to locate source stations.