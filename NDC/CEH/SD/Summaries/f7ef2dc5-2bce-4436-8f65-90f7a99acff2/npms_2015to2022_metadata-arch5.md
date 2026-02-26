# The National Plant Monitoring Scheme

## Overview and purpose
- National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring program designed by BSBI, UK CEH, Plantlife and JNCC.
- Aims to provide annual indications of changes in plant abundance and diversity and to detect changes in priority habitats, understand drivers, and contribute data for UK Biodiversity indicators.
- Supports volunteer recorders across the UK, Isle of Man, and Channel Islands, using a structured, repeatable sampling framework.
- The quarterly/annual dataset is maintained by UKCEH in Wallingford and is accompanied by field guidance and evidence quality assurance documentation.

## Data assets (files provided)
- locations_2015to2022.csv: unique location_id and location_type describing survey plot types; links to sampling events via location_id.
- sampleInfoWithLatLong_2015to2022.csv: sampling events with id, survey_id, date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id; includes LATITUDE, LONGITUDE, monad, monadCRS, country; ties to location_id for event history.
- sampleAttributes_2015to2022.csv: additional sample data linked to sample_id; includes caption and text_value for attributes (e.g., habitat).
- occurrences_2015to2022.csv: species occurrences with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), sensitivity_precision (blurring flag).
- npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv: harmonised Domin score mappings and mid-point interpretations.

## Data model and linkage
- Location-centric structure: locations_2015to2022.csv provides location_id and type; sampleInfoWithLatLong_2015to2022.csv provides time-stamped sampling events linked by location_id.
- Sample-level details: sample_id (through survey_id) ties to events with date, coordinates (entered_sref, lat/long), CRS (monadCRS), and spatial context (monad, country).
- Attribute data: sampleAttributes_2015to2022.csv links additional descriptive data to samples via sample_id (e.g., habitat information).
- Observations: occurrences_2015to2022.csv records species observations tied to samples; includes verification status and potential spatial sensitivity (sensitivity_precision).
- Taxonomy and habitat context: npmsHabitatLookup.csv and dominScores.csv support harmonisation across versions and formats from various survey modules.

## Data quality, provenance, and QA
- Evidence Quality Assurance (EQA) framework and external publications underpin data quality and methodological rigor.
- Data are validated through:
  - Controlled vocabularies, standardized dates, and map-based location entry.
  - Verification via the iRecord system for botanical records (expert review where needed).
  - Spatial range checks and a data dictionary to ensure consistency.
- Output quality is assessed and documented; uncertainty and limitations are communicated in outputs (newsletters, reports) and peer-reviewed materials.
- Distinct data versions are archived; data management follows formal project governance (Data Management Plan, PRINCE2 standards).

## Data governance, privacy, and transparency
- Recorder identities: public-facing data do not disclose recorder names; unique IDs are used for traceability while preserving privacy.
- Data publication: NPMS data are intended to be publicly available for independent review and reuse.
- Documentation and guidance: NPMS survey guidance, habitat indicators, and taxon references are provided to ensure consistent data collection and interpretation.

## Access, sharing, and interoperability
- Data are accessible through the NPMS platform and accompanying guidance documents (survey guidance, indicator lists, ID guides).
- Example workflows illustrate joining datasets (e.g., linking sampleAttributes to sampleInfoWithLatLong via sample_id to retrieve habitat information).
- Data are provided in CSV format and are designed to be usable in common statistical environments (e.g., R, SQL).

## Updates, versioning, and documentation
- NPMS datasets are annually updated; documentation and field guidance accompany data releases.
- Project governance includes versioned design outputs, with off-site backups and an established data management plan.
- All design outputs and methodological decisions are archived and subject to project reviews.

## EQA framework and questions (highlights)
- Q1: Peer review of methods and publications; design decisions involve statisticians and botanical experts; field methods include tiered volunteer engagement and training.
- Q2: Quality assurance levels are determined by risk; a project Steering Group and targeted external peer reviews are used as needed.
- Q3: Uncertainty, quality, and limitations are clearly checked and communicated in outputs; ongoing feedback from the scientific community is expected.
- Q4: Bias reduction through robust statistical design enabling uncertainty estimation via models.
- Q5: Document tracking and version control via a Data Management Plan; design outputs are archived and backups maintained.

## Practical notes for data stewards
- Monitor and enforce consistent use of location_id, sample_id, and survey_id links across files to preserve data integrity.
- Maintain harmonised Domin and habitat classifications via dominScores.csv and npmsHabitatLookup.csv for cross-version comparability.
- Ensure sensitive records are appropriately blurred (sensitivity_precision = 10000) and privacy-preserving measures are upheld.
- Facilitate data access while maintaining provenance; document updates and changes through versioned releases and clear metadata.

## Resources and references
- NPMS field guidance and survey resources: NPMS website and content sections for survey guidance and resources.
- Key publications and reports supporting EQA and NPMS methodology (listed in the document).
- iRecord verification system for data validation.