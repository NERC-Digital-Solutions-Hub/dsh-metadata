# National Plant Monitoring Scheme survey data (2015-2023)

## Scope and purpose
- Provides plot-level plant occurrence data for NPMS across the UK, Channel Islands, and Isle of Man for 2015–2023.
- Includes plant observations, habitat characteristics, metre-scale measurements, Domin frequency-abundance scale values, plot type, sampling date, and precise spatial location.
- Enables reconstruction of the sampling history for any sampled plot, including gaps.

## Data collection and ingestion
- Data collected by volunteers into a custom Indicia database system (PostgreSQL/PostGIS) via the NPMS website or app.
- Indicia serves as the master database; data extraction is performed with SQL queries.

## Data structure and files provided
- locations_2015to2023.csv: unique location_id, location_type, samplecount.
- sampleInfoWithLatLong_2015to2023.csv: sample id, survey_id (type of NPMS survey), date_start, location_id, entered_sref and system, created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country.
- sampleAttributes_2015to2023.csv: sample_attribute_id, sample_id, caption, text_value (e.g., habitat attributes).
- occurrences_2015to2023.csv: id, sample_id, taxonversionkey, preferred_taxon, domin, record_status, sensitivity_precision (including optional spatial blurring).
- npmsHabitatLookup.csv: mapping between NPMS broad and fine-scale habitats.
- dominScores.csv: harmonised Domin categories with mid-points for cross-compatibility across survey types.
- Notes: Example provided for merging habitat information via R or SQL (LEFT JOIN on sample_id).

## Data quality assurance and reliability
- Evidence Quality Assurance (EQA framework) supported by multiple publications and internal reports.
- Governance: project Steering Group with external peer review where warranted; risk-based quality checks.
- Data entry and verification: online capture with a species dictionary, controlled terms, date formats, and map-based locations; automated geographic range checks; iRecord verification for expert review.
- Uncertainty and limitations: outputs reviewed by scientists; ongoing feedback from the ecological community; models used to estimate uncertainty in analyses.

## Governance, access, and versioning
- Oversight by NPMS project Steering Group; external peer review as needed.
- Documentation and outputs tracked and archived; project Data Management Plan aligned with PRINCE2 standards; backups stored off-site.

## Technical context and usage notes
- Spatial references include OSGB (British National Grid), OSIE (Irish National Grid), and WGS84; monad concept used to denote 1 km grid squares.
- Habitat information can be accessed by joining sampleInfoWithLatLong with sampleAttributes (NPMS Habitat) or via SQL/R workflows.
- Intended to support annual indicators of habitat quality, drivers of change, and UK Biodiversity Indicator (C7) through analysis of plant communities.

## Implications for data leaders
- Provides a comprehensive, volunteer-driven, longitudinal plant-monitoring dataset with clear metadata, QA processes, and governance.
- Demonstrates an end-to-end data lifecycle: collection via volunteers, centralized spatial database, standardized attributes, quality assurance, and public data sharing.
- Highlights the importance of robust data standards, provenance, and documentation to enable reproducible analyses and cross-institution collaboration.
- Indicates potential for data-driven policy and monitoring insights, while acknowledging gaps, varying survey types, and sensitivity constraints.