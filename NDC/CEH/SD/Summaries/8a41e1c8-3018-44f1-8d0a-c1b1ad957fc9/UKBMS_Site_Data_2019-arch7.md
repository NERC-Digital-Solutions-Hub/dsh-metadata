# About the UK Butterfly Monitoring Scheme

## Overview
- Long-running, organization-wide data program (since 1976) funded by Butterfly Conservation, CEH, BTO, and JNCC.
- Over 2,500 active sites tracked annually; data collected via volunteers to monitor butterfly population trends for biodiversity policy questions.
- Data are used to create abundance indices (relative measures) that reflect seasonal patterns and support trend analyses.

## Data collection methods and GIS relevance
- Three sampling components:
  - Standard butterfly transects (Pollard walks): fixed routes, 2–4 km, weekly counts (26 visits/year) across habitat sections.
  - Wider Countryside Butterfly Survey (WCBS): stratified 1 km squares with two parallel transects; 2–3 visits per square/year, focusing on common habitats.
  - Targeted surveys: single-species transects, timed counts, and egg/larval web counts using alternative methods.
- Data integration: counts from all methods are analyzed together to produce species-wide indices.
- Geographic scope and outputs: site- and square-based data support map-based visualisations of distribution and trends; includes coordinates for GIS mapping.

## Data download structure and fields
- Dataset span: site location and attributes for UK butterfly monitoring between 1976 and 2019; sensitive sites omitted.
- File format: CSV (comma-separated values).
- Key fields:
  - Site number, Site name
  - Gridreference (6-figure typical), Easting, Northing (start point coordinates)
  - Length (transect length in metres)
  - Country
  - No. Sections (transect divisions)
  - No. Yrs surveyed, First year surveyed, Last year surveyed
  - Survey type (UKBMS standard transect or WCBS)
- Use: supports GIS mapping of site locations and temporal coverage; enables spatial analysis of monitoring effort and trends.

## Data quality and validation
- Data capture: field forms, online entry via UKBMS data site or Transect Walker; uploaded to central database.
- Automated checks: real-time validation for implausible counts or out-of-season records.
- Regional validation: transect coordinators review data for questionable entries; continuous season-long checks.
- Additional validation: automated/manual queries for records outside known ranges or unusual patterns; corrections applied to main dataset.
- Data history note: since 2017, submitters agreed to Open Government Licence; potential historic data IP restrictions may apply; contact if issues arise.

## Licensing, attribution, and reuse
- Licence: Open Government Licence (OGL) for data download and reuse.
- Citations: must include the dataset’s DOI/citation as provided in metadata.
- Attribution: include statement “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.”
- Dan clarity: historical data may have third-party restrictions; if concerns, contact dataset maintainers.

## Collaboration and contact
- Offers of collaboration and co-authorship for scientific outputs resulting from UKBMS data.
- Primary contacts:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect co-ordinator): transect@butterfly-conservation.org