# About the UK Butterfly Monitoring Scheme

- Purpose and mandate: The UK Butterfly Monitoring Scheme (UKBMS) provides annual data on butterfly population status to address policy questions about biodiversity status and trends.
- Organisers and supporters: Organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology (CEH), British Trust for Ornithology, and the Joint Nature Conservation Committee; with significant volunteer contributions.
- Data users and outputs: Outputs are used to understand insect population changes and to inform environmental policy; results are presented via reports, charts, or dashboards.

## Data collection and sampling framework

- Three components:
  - Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km), recording all species in a 5 m band weekly from April to September; ~26 counts per year; ~2000 sites.
  - Reduced effort surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focusing on specific species.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects; 2–4 visits per square (vs. 26 for standard transects); about 750 squares annually; started in 2009 to sample farmland habitats.
- Scale and integration: Data from all components are combined to produce species-level indices.
- Notable references: Pollard & Yates (1993) foundational methodology.

## Nature of data and trend analysis

- Index-based measures: Abundance indices derived from counts along transects and sites; indices are relative, not absolute, population sizes.
- Index construction: Generalised Abundance Index (GAI) method (2016) with weighting to reflect the proportion of the flight period surveyed at each site-year, giving more weight to observed data than extrapolated data.
- Use of full data: All counts across a season (from all components) inform the seasonal pattern and are extrapolated to address gaps.

## Quality control

- Data entry and validation: Field forms, online entry (UKBMS data portal or Transect Walker software), automatic checks for anomalies, and regional transect coordinators review records.
- Validation processes: Automated and manual checks for records outside species distributions, outside flight periods, first-time site records, extreme or unusual counts; data edits are made after coordination and queries.

## Details of this data download

- Content: Long- and short-term trends in collated indices for all species with sufficient data.
- Format: CSV file with described columns, including:
  - COMMON_NAME, SCI_NAME
  - NYEARS (years of series)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL, F_FULL_R (overall trend metrics)
  - T20_LIN_B/SE/P, T20_TRENDDETAIL, T20_20_R (20-year trend metrics)
  - T10_LIN_B/SE/P, T10_TRENDDETAIL, T10_10_R (10-year trend metrics)

## Licence and attribution

- Licence: Open Government Licence (OGL) for free use and reuse with minimal conditions.
- Citation and attribution: Include the metadata DOI/citation in reports; attribution statement required: contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- Collaboration: UKBMS partners offer advisory support, interpretation help, and potential co-authorship for publications arising from UKBMS data.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - CEH: Marc Botham (ukbms@ceh.ac.uk)