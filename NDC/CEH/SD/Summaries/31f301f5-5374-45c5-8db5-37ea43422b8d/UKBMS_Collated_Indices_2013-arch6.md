# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Primary methods:
  - All-species transects (Pollard walk): fixed-route, weekly counts April–September; transects 2–4 km, 45 minutes to 2 hours; 26 counts/year; 5 m wide belt to record all species; routes fixed to enable year-to-year comparisons; weather-dependent activity window (10:45–3:45, dry, Beaufort <5, temperature ≥13°C with sun or ≥17°C if overcast).
  - Single-species transects: same methodology as all-species but for one focal species, recorded on one or more weeks.
  - Timed counts: abundance of a species over a set period within a defined area (weather and time window as above).
  - Egg/larval web counts: number of eggs or larval webs in suitable habitat.
- Data are collected in the field on standard forms and entered into Transect Walker software; entered by recorder or regional transect coordinator; regional coordinators compile data for their region.

- Data flow:
  - Transect Walker files uploaded to an Oracle database holding all records.

- Experimental design rationale:
  - Transects sampled to cover habitat types and management across sites; fixed routes permit comparability across years.

- Timeframe and data scope:
  - Counts occur during the butterfly flight period (approx. April–September) with annual data updates and site coverage varying by year.

- Analysis and outputs (overview):
  - Data quality and validation precede analysis.
  - Site indices calculated using General Additive Models (GAM) to impute missing values.
  - Collated Indices (national annual indices for each species) derived by combining site indices via loglinear regression, accounting for year effects and site effects.
  - Collated Indices updated annually as new data are incorporated; based on species recorded at five or more sites per year.

- Nature and units of recorded values:
  - Site indices are relative measures; Collated Indices are log-transformed (Log10) and scaled so the average index over the series equals 2, providing a relative measure of population size over time. Some species vary in detectability.

- Quality control and data validation:
  - Automatic checks in Transect Walker flag unusual counts or flights outside known ranges.
  - Regional coordinators review data for questionable records.
  - Additional automated/manual validations assess distributions, flight periods, first-time site records, extreme or atypical abundances.

- Data storage format:
  - Collated Indices stored as CSV.
  - Columns include: Species (scientific name per Fauna Europaea), Common name, Year, No. Sites (sites contributing to the index that year), Collated Index, Time period (data used to produce the indices).