# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Most sites use fixed-route transects called Pollard walks to estimate butterfly abundance; some species use alternative standardised methods (timed counts or egg/larval web counts).
- All-species transects: fixed-route, weekly sampling across 2–4 km routes in suitable weather, typically 26 counts per year, with 5 m transect width sampling all species in the route.
- Transects are designed to sample diverse habitat types and management activities and must remain fixed year to year to enable trend comparisons.
- Weather constraints: sampling occurs between 10:45 and 15:45, in dry conditions with Beaufort wind <5, and temperature thresholds (≥13°C with ≥60% sunshine or ≥17°C when overcast).
- Single-species transects follow the same method but are recorded only for one focal species across one or more weeks.
- Timed counts and egg/larval web counts provide alternative methods for particular species and habitats.

- Pollard, Yates, and other foundational references underpin the methodology.

- Data collection methods involve field recording on standard forms, later entered into Transect Walker software (free download), either by the recorder or a regional transect coordinator.
- Transect Walker data are uploaded into an Oracle database that stores all records.
- Each transect coordinator manages data for all sites within their region.

- Analytical methods start with data validation, then use General Additive Models (GAMs) to impute missing values and derive site indices.
- Site indices from all sampling methods are combined to produce a national annual Collated Index for each species.
- Because not all sites are monitored every year, a loglinear regression model estimates missing values and yields indices and trends.
- The Collated Index for a species is updated annually as new data are incorporated; past years’ indices may adjust slightly.
- Collated Indices are calculated for species recorded from at least five sites per year.

- Nature and units of recorded values:
  - Site indices are relative measures of population size, not absolute counts; they reflect proportions of butterflies observed and relate to other population measures.
  - Collated Indices are presented as log10 values and are scaled so the average index over the series equals 2, providing a relative temporal measure.

- Quality control:
  - Automated checks in Transect Walker flag anomalous records (e.g., unusually high counts or flights outside known periods).
  - Regional coordinators review data for questionable records.
  - Additional validation checks screen for out-of-range distributions, atypical flight periods, first-time site records, and extreme abundances.

- Format and storage of data:
  - Collated Indices are stored as CSV files with columns: Species, Common name, Year, No. Sites, Collated Index, Time period.
  - Species names follow Fauna Europaea; common names follow standard references.
  - Raw field data flow: field forms → Transect Walker → Oracle database.
  - Collated Indices are periodically updated and made available in CSV format for dissemination.