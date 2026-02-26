# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, using multiple standardized butterfly recording methods.

- Data collection methods
  - All-species transects (Pollard walks): fixed-route line transects (typically 2–4 km) with 26 counts per year from April to September, in a 5 m wide band, under suitable weather; transects fixed to enable year-to-year comparability.
  - Single-species transects: follow the all-species protocol but record for only one focal species in one or more weeks.
  - Timed counts: record abundance of a target species over a set time/area under suitable weather.
  - Egg/larval web counts: count eggs or larval webs in suitable habitat areas.

- Data collection in the field and entry
  - Data recorded on standard forms.
  - Entered into Transect Walker software (free download) by the recorder or regional transect coordinator.
  - Transect Walker files uploaded to an Oracle database housing all records.
  - Each transect coordinator aggregates data for their region.

- Analytical methods and indices
  - After validation, a General Additive Model (GAM) imputes missing values and computes site indices.
  - Site indices from all methods are combined to form a national annual index (Collated Index) per species.
  - Missing values are estimated using a log-linear regression model that accounts for year effects (weather-related) and site effects (population variation).
  - Collated Indices are updated annually as new monitoring data are incorporated; past years’ indices may shift slightly with updated data.
  - Site indices are relative measures, reflecting a constant proportion of true population size, and are scaled as Log10 Collated Index (LCI) with an average of 2 across the series.

- Data storage and formats
  - Collated Indices are stored as CSV files.
  - Columns include: Species (scientific name per Fauna Europaea v2.2), Common name (per Emmet & Heath), Year, No. Sites, Collated Index, Time period.

- Quality control and validation
  - Automatic checks in Transect Walker flag anomalous counts or records outside flight periods.
  - Regional coordinators review records for each region for plausibility.
  - Additional validation includes: distribution-range checks (against Butterflies for the New Millennium data and UKBMS data), flight period consistency, new-site records, extreme abundances, and unusual year-site patterns.

- Data governance and provenance considerations
  - Standardized data collection forms and recording processes ensure consistency across sites and methods.
  - Use of controlled vocabularies for species names and metadata sources (Fauna Europaea, Emmet & Heath references) supports interoperability.
  - Data are continuously updated and versioned through annual incorporation of new data, requiring mechanisms to reference the exact data snapshot used for each Collated Index.