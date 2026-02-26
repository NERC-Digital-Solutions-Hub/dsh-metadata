# National Plant Monitoring Scheme survey data (2015-2023)

## Overview
- Plot-level plant occurrence data for 2015–2023 across the UK, Channel Islands, and Isle of Man.
- Observations include plants and habitat characteristics at metre scale, with Domin frequency-abundance (Domin) scores.
- Includes plot type, NPMS habitat, sampling date, and precise plot location.
- Enables reconstruction of each plot’s sampling history, including gaps.

## Data Collection and Structure
- Data collected by volunteers into the Indicia system (PostgreSQL/PostGIS) via NPMS website or app.
- Data extracted from the master database using SQL queries.
- Files provided:
  - locations_2015to2023.csv: unique location_id, location_type, samplecount
  - sampleInfoWithLatLong_2015to2023.csv: sample id, survey_id, date_start, location_id, coordinates, CRS info, created_on/by
  - sampleAttributes_2015to2023.csv: sample_attribute_id, sample_id, caption, text_value
  - occurrences_2015to2023.csv: id, sample_id, taxonversionkey, preferred_taxon, domin, record_status, sensitivity_precision
  - npmsHabitatLookup.csv: mapping between NPMS broad and fine-scale habitats
  - dominScores.csv: harmonised Domin categories and mid-point estimates
- Spatial and temporal fields:
  - entered_sref and entered_sref_system for sample coordinates
  - monad (1 km squares) and monadCRS (OSGB, OSIE, UTM30)
  - LATITUDE/LONGITUDE for sample locations

## Data Model and Linking
- Core relationships:
  - location_id links locations_2015to2023.csv to sampleInfoWithLatLong_2015to2023.csv
  - sample_id (id) links sampleInfoWithLatLong_2015to2023.csv to occurrences_2015to2023.csv
- Habitat and Dominant abundance:
  - NPMS habitat information accessed via sampleAttributes_2015to2023.csv (e.g., caption = NPMS Habitat)
  - npmsHabitatLookup.csv and dominScores.csv provide harmonised habitat and Domin mappings
- Example data integration approach is provided (R and SQL) to attach habitat information to samples.

## Data Quality, Evidence, and QA
- NPMS designed to monitor habitat quality and plant community change; QA is integral.
- Data entry uses controlled vocabularies, dictionaries, date calendars, and map-based locations.
- Automated checks (geographic range, data consistency) plus iRecord verification for expert review.
- Outputs are intended for public access and independent review; analysis conducted by experienced ecologists.
- Supporting publications and reports outline the evidence quality assurance framework and methods.

## Access, Use, and Example Workflows
- Data can be joined across files to obtain habitat information for each sample (example provided in R; comparable SQL approaches available).
- Data reconstruction includes sampling history per plot, including repeated sampling events.
- Guidance documents and surveyor resources are available through the NPMS website.

## Uncertainty, Limitations, and Data Ethics
- Some records may be blurred (sensitivity_precision = 10000) to protect sensitive observations.
- Domin scores may be blank for presence-only records; harmonisation implemented via dominScores.
- Volunteer-based data collection introduces variability in field recording and habitat classification.

## Governance, Versioning, and Access Control
- Oversight by NPMS Steering Group; external peer review applied as needed based on risk.
- Document tracking and version control follow a Data Management Plan; backups off-site; PRINCE2 project management standards.
- Data published publicly to enable independent review and broad use.

## Practical Notes for Data Support
- Primary data access via Indicia/NPMS interfaces; master database extraction with SQL.
- File sizes indicate substantial data coverage across years and plots.
- The dataset supports analyses of habitat change, plant community dynamics, and indicators related to UK biodiversity.

## References and Further Resources
- NPMS project materials, survey guidance (2nd edition), and related publications provide context for methods and QA.
- Key methodological and monitoring references listed in the accompanying NPMS documentation.