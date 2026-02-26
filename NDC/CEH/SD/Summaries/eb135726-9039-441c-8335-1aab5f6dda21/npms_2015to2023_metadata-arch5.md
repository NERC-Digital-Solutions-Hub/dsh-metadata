# National Plant Monitoring Scheme survey data (2015-2023)

## Overview
- Plot-level plant occurrence data for 2015–2023 across the UK, Channel Islands, and Isle of Man.
- Observations include plant occurrences and habitat characteristics at metre-scale, with Domin frequency-abundance (Domin) cover data.
- Additional context: plot type, NPMS habitat, sampling date, and precise plot location to enable reconstruction of sampling history and gaps.

## Data scope and structure
- Data are provided as six CSV files:
  - locations_2015to2023.csv: unique location identifiers, location type (plot type), and sample counts per location.
  - sampleInfoWithLatLong_2015to2023.csv: sampling events with id, survey_id, date, location_id, spatial reference, timestamps, maker, latitude/longitude, monad (1 km square), country, and coordinate reference system details.
  - sampleAttributes_2015to2023.csv: attribute records linked to samples (sample_id), including captions and text values (e.g., habitat attributes).
  - occurrences_2015to2023.csv: species occurrences linked to samples, including taxon keys/names, Domin scores, record status, and sensitivity/precision flags.
  - npmsHabitatLookup.csv: mapping between NPMS broad and fine-scale habitats.
  - dominScores.csv: harmonised Domin category mappings and mid-point interpretations.
- Data model relationships:
  - locations_2015to2023.csv -> sampleInfoWithLatLong_2015to2023.csv via location_id.
  - sampleInfoWithLatLong_2015to2023.csv -> occurrences_2015to2023.csv via sample_id.
  - sampleAttributes_2015to2023.csv -> sampleInfoWithLatLong_2015to2023.csv via sample_id.
- Coordinate and geography:
  - Spatial references include OSGB, OSIE, and WGS84 (via monad and entered_sref/entered_sref_system).
  - Sensitive records may have coordinates blurred to 10 km (sensitivity_precision = 10000).

## Provenance and collection methodology
- Data collection via volunteers entering observations into the Indicia system (PostgreSQL/PostGIS) through the NPMS website or app.
- NPMS design aims to monitor habitat quality and plant community change across a standardized grid of plots and linear plots.
- Survey types include Wildflower, Inventory, and Indicator surveys; data input uses controlled terms, a species dictionary, date calendars, and map-based locations to minimize entry errors.
- Verification is supported through the iRecord system (BSBI-affiliated experts) for records requiring higher botanical expertise.

## Quality assurance, standards, and uncertainty
- Evidence Quality Assurance (EQA) framework supports data reliability; methods and outputs are described in related publications and NPMS documentation.
- QA features:
  - Online data capture with structured spatial database design.
  - Automated checks (e.g., geographic range checks) and expert verification through iRecord.
  - Steering Group oversight; external peer review when risk warrants.
  - Documentation of design decisions, habitat definitions, and target species indicators with periodic review.
- Uncertainty and limitations:
  - Robust statistical design to enable uncertainty estimation via models.
  - Clear communication of uncertainty, assumptions, and limitations in newsletters and reports.
  - Field recording relies on volunteers with multiple expertise levels; no formal ongoing field recording QA is embedded, but guidance and training are provided.
- Documentation and versioning:
  - Full design and outputs are tracked; versions archived and backed up off-site according to UK CEH Data Management Plan using PRINCE2 standards.

## Access, sharing, and governance
- Data are publicly accessible to support independent review and reuse; datasets are accompanied by guidance on use and interpretation.
- Data management and governance:
  - Data management plan in place; version control and off-site backups.
  - Clear lineage from field collection to published datasets, with traceable sample and attribute identifiers.
- Privacy and data sensitivity:
  - Sensitive records are flagged; spatial precision may be blurred to protect sensitive locations.

## Practical considerations for Data Stewards
- Metadata and standards alignment:
  - Ensure consistent definitions across files (e.g., survey_id, location_type, sample_id, domin, record_status).
  - Maintain accurate lookups (npmsHabitatLookup, dominScores) to enable harmonised analyses.
- Data ingestion and updates:
  - Maintain the linkages between locations, samples, attributes, and occurrences; verify integrity during updates.
  - Track changes through the Data Management Plan and PRINCE2 processes; archive prior versions.
- Access governance and risk management:
  - Monitor data sensitivity flags and ensure appropriate handling for blurred coordinates.
  - Schedule external reviews when risk is introduced by new outputs or methodologies.
- User guidance and transparency:
  - Provide clear instructions and examples (e.g., how to join sample habitat information in R or SQL) to aid data users.
  - Document limitations and uncertainty in data products to prevent misinterpretation.

## Usage notes and caveats
- Example workflows illustrate joining habitat information from sampleAttributes_2015to2023.csv with sampleInfoWithLatLong_2015to2023.csv to obtain habitat data for each sample.
- Data are suitable for analyzing habitat change and plant community indicators, with results to be interpreted alongside accompanying QA documents and methodological papers.