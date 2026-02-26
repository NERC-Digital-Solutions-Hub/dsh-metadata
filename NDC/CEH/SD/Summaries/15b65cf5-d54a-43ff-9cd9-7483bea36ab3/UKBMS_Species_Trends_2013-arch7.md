# Experimental design/sampling regime

- Overview of UK Butterfly Monitoring Scheme (UKBMS)
  - Data from over 1,000 sites annually across the UK using fixed transect routes (Pollard walks) to sample habitat types and management activity.
  - Includes all-species transects (fixed-route, weekly counts Apr–Sep) and single-species transects (focal species, fewer weeks).
  - Transects typically 2–4 km long, divided into habitat/management sections, with counts in a 5 m wide band along the transect.
  - Weather- and time-of-day constraints: walks between 10:45 and 15:45, suitable butterfly activity conditions.

- Data collection methods and workflow
  - Field data recorded on standard forms and entered into Transect Walker software.
  - Data entry can be by the recorder or a regional transect coordinator.
  - End-of-season data compiled by transect coordinators for each region.
  - Transect Walker files uploaded to an Oracle database containing all records.

- Sampling design details
  - All-species transects: fixed routes to ensure year-to-year comparability; all butterflies recorded along the transect.
  - Single-species transects: follow the same methodology but focused on one species during a subset of weeks.
  - Timed counts and egg/larval web counts provide additional abundance data for selected species.
  - Counts and data collection occur under predefined weather and activity criteria.

- Analytical methods
  - After data validation, General Additive Models (GAM) impute missing values and compute site indices.
  - Collated Indices are derived by combining site indices across monitored sites; indices are log10-transformed with a mean scaled to 2.
  - National trends are estimated via linear regression on the collated indices.
  - Time periods analyzed: entire series (1976–2013), last 20 years (1993–2013), and last 10 years (2003–2013). Not all species have full-length series due to data gaps; the number of contributing years is recorded.

- Nature and units of recorded values
  - Site indices: relative measures of population size (not absolute counts); correlate with more intensive methods (e.g., MRR).
  - Collated Indices: log10-transformed values scaled for comparability; trends reported as slopes (change per year).
  - Series details: include slope, standard error, P-value, trend description, and percent change for the full series, plus 20-year and 10-year equivalents.

- Quality control
  - Automatic checks in Transect Walker flag potential data entry errors (e.g., out-of-range counts, atypical flight periods).
  - Regional coordinators validate records with local knowledge.
  - Additional automated/manual validation screens for records outside known distribution, unusual timing, first-time site records, or extreme values.

- Format and storage of data
  - Species Trends stored as CSV files.
  - Columns include: Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change, 20-yr slope/Std.Err/P-value/Trend/% change, 10-yr slope/Std.Err/P-value/Trend/% change.
  - Species identifiers follow Fauna Europaea standards and common reference names.

- GIS-relevant considerations and potential data products
  - Spatial layers representing transect routes, site locations, and habitat units enable map-based visualization of site indices, collated indices, and trend categories.
  - Temporal data allows animated or time-series mapping of population trends across regions.
  - Uncertainty and significance (standard errors, P-values) support confidence-aware mapping and decision-making.
  - Data limitations to consider in GIS work: relative rather than absolute population sizes, data gaps leading to varying year coverage, and potential updates to past years as new data are incorporated.