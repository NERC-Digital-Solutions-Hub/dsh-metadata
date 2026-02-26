# Flower species and their estimated abundances on farmland

## Data overview
- Records of flower species and their estimated abundances on farmland.
- Study conducted on eight farms across Hampshire and West Sussex, England, UK.
- Data collection periods: May–August in 2014 and 2018.
- A single transect of 3 km marked per farm, covering diverse habitats (hedgerows, seed mixtures, grass margins, and regenerating areas).

## Locations and scope
- Farm locations provided with coordinates (Table 1) for eight sites labeled A–H.
- Each farm transect was split into distinguishable sections; sections retained across 2014 and 2018 surveys.

## Collection and generation methods
- Floral surveys conducted along each transect in three rounds per year.
  - 2014 (TJW): 17–27 May, 21 Jun–9 Jul, 3–15 Aug.
  - 2018 (RNN): 14–19 May, 20 Jun–7 Jul, 3–7 Aug (dates aligned with 2014 rounds).
- Each transect section walked in 2014 retained in 2018 surveys.
- Data captured at the section level, enabling year-to-year comparison.

## Nature and units of record
- For each transect section, recorded:
  - Flower species observed and estimated numbers of open flowers within a 2 m width on either side of the observer.
  - A flower counted if fully open; counted as a single flower, or as flowers within umbels/spikes/capitula.

## Quality control
- Counts calibrated between surveyors by cross-checking estimates from photographs and applying a scaling factor to ensure consistency.

## Data structure and dataset contents
- Data stored in an Excel spreadsheet named FloralResources.csv with 11 columns:
  - Year: year of data collection.
  - Round: survey round (1, 2, or 3) in date order.
  - Type: countryside stewardship category (ELS or HLS).
  - Farm: farm where the survey was conducted.
  - Label: transect section identifier.
  - What: type of management for the transect section.
  - Length (m): transect section length.
  - Width (m): transect section surveyed width.
  - Family: plant family surveyed.
  - Species: plant species surveyed.
  - Abundance: estimated abundance of open flowers in the transect section.

## Data governance considerations for Data Stewards
- Standardization: clear definitions (e.g., what constitutes a counted flower) and calibration process support consistent data quality across years and surveyors.
- Metadata richness: includes year, round, farm, management type, and spatial/dimensional attributes; consider expanding metadata with provenance, sampling scripts, and data licenses for reuse.
- Interoperability: dataset uses consistent fields, but notes alignment of survey rounds across years to facilitate longitudinal analyses; ensure consistent units and terminology when integrating with other datasets.
- Data availability and sharing: data presented as a CSV/Excel file; assess dissemination plan, versioning, and access controls if expanding to portals or catalogs.
- Provenance and updates: maintain changelog and maintainability of the transect schema if updates or additional years are added.
- Challenges to address: potential incomplete user needs (e.g., additional habitat or environmental covariates), timely data updates, and harmonizing formats across multiple seasons or researchers.