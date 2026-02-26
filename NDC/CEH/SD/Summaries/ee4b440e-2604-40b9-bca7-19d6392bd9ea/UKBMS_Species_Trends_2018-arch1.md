# About the UK Butterfly Monitoring Scheme

- Organised and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee; relies on volunteers.
- Purpose: provide annual data on butterfly population status from a large-scale, site-based monitoring framework, including random 1 km square sampling; used to understand changes in insect populations and inform biodiversity policy questions.
- History and scale: running since 1976 with over 2,500 actively recorded sites each year.

## Data collection framework and components

- Standard butterfly transects (Pollard walks): fixed-route transects (typically 2–4 km) with weekly counts across the flight season (April–September); ~26 counts per year at almost 2,000 sites.
- Reduced effort surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focusing on specific species or reduced effort periods.
- Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares with two parallel transects; 2–4 visits per year (plus encouraged spring visits); targets common habitats (e.g., farmland); ~750 squares sampled annually.
- All components’ data are analyzed together to produce overall species indices.

## Nature of data and trend analysis

- Data are expressed as abundance indices (relative measures) rather than absolute population sizes.
- Indices reflect a constant proportion of butterflies present, with detectability varying by species.
- Trend estimation uses the Generalised Abundance Index (GAI) method (2016) with site- and year-weighting to account for sampling variation and gaps in recording.
- The method combines counts from all components to estimate seasonal patterns and extrapolate missing data, with greater weight given to observed data.

## Quality control and data validation

- Field data recorded on standard forms and entered online or via Transect Walker; uploaded to a central database.
- Automatic checks flag unusual counts or records outside known flight periods; options to confirm or edit.
- Regional transect coordinators validate data; ongoing checks throughout the season.
- Additional automated and manual validation: cross-checks for records outside known distributions, unusual abundances, first-time site records, and other anomalies; data corrections are made in collaboration with coordinators or recorders.

## Details of this data download (structure and content)

- Provides long- and short-term trends in collated indices for species with sufficient data; delivered as a CSV.
- Key columns include:
  - COMMON_NAME and SCI_NAME (vernacular and scientific species names)
  - NYEARS (years in the trend)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL (overall trend slope, its SE, P-value, and description)
  - F_FULL_R (overall percent change across the full series)
  - T20_LIN_B/SE/P and T20_TRENDDETAIL/T20_20_R (last 20 years), plus T10_LIN_B/SE/P and T10_TRENDDETAIL/T10_10_R (last 10 years)
- Descriptions classify trends (rapid decline/increase, stable) based on slope direction and statistical significance.

## Licence and attribution

- Open Government Licence (OGL) allows free use and reuse with few conditions.
- Any research outputs must cite the dataset (including DOI) and include the attribution: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer advisory support and interpretation of outputs.
- Co-authorship and intellectual input contributions are welcome for publications, presentations, or posters.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - CEH: Marc Botham (ukbms@ceh.ac.uk)