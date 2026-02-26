# National Plant Monitoring Scheme (NPMS)

## Aim and scope
- Habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC.
- Collects data to provide annual indications of changes in plant abundance and diversity.
- Supports volunteer plant recorders to monitor plants and habitat attributes in small plots selected by a structured methodology across the UK, Isle of Man, and Channel Islands.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers and pressures behind change.
  - Contribute data to UK Biodiversity Indicator C7 (plants of the wider countryside) by measuring changes in plant communities across important habitats.
- Provides an annually updated dataset representing the current state of the NPMS database held at UKCEH Wallingford.

## Data and files provided
- locationTypes_2015to2020.csv
- sampleAttributes_2015to2020.csv
- sampleInfoWithLatLong_2015to2020.csv
- occurrences_2015to2020.csv
- npmsHabitatLookup.csv
- dominScores.csv

## File descriptions (what they contain)
- locationTypes_2015to2020.csv
  - Unique location_id and location_type describing the survey plot type at each location; links to sampleInfoWithLatLong_2015to2020.csv.
- sampleInfoWithLatLong_2015to2020.csv
  - Sample-level data: id, survey_id (type of NPMS survey), date_start, location_id, entered_sref and system, created_on, created_by_id, latitude, longitude, monad, monadCRS, country.
  - Includes repeated sampling events per location.
- sampleAttributes_2015to2020.csv
  - Additional data about samples linked by sample_id; includes category (caption) and value (text_value).
- occurrences_2015to2020.csv
  - Species occurrences: id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C/V/R), sensitivity_precision (e.g., blurred records).
- npmsHabitatLookup.csv
  - Mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv
  - Lookup between recorded Domin scores and a harmonised Domin category; includes midPoint for cover estimation.

## Accessing habitat information (example)
- Example workflow in R:
  - Merge habitat information with samples using sample_id and id.
- Notes: SQL or other database frameworks can achieve the same via LEFT JOINs with the appropriate where clause on habitat attributes.

## Evidence Quality Assurance (EQA) and governance
- EQA framework supported by publications and guidance on NPMS data use.
- Key publications and reports referenced (design, validation, and analysis of NPMS; citizen science in ecological monitoring).
- Quality assurance elements include:
  - Data input and verification via structured databases, species dictionaries, calendar dates, map-based locations, and controlled terms.
  - Verification via iRecord system for higher-qualification records.
  - Automated geographic range checks; public data publishing for independent review.
  - Analysis performed by experienced quantitative ecologists using R.
  - Reporting produced by a multidisciplinary project team (botany, statistics, communication).
- Q1-Q5 governance questions addressed:
  - Q1: Design and methodological development (sampling stratification, habitat definitions, indicator species selection, field recording with three participation levels, data input/verification, data publishing, analysis, and reporting).
  - Q2: Review and QA levels overseen by a project Steering Group; external peer review for higher-risk outputs.
  - Q3: Uncertainty, quality, assumptions, and limitations disclosed and checked by scientists before publication.
  - Q4: Bias reduction via robust statistical design enabling uncertainty estimation through models.
  - Q5: Document tracking and version control via archived design reports and off-site backups under a Data Management Plan; adherence to PRINCE2 project standards.

## How NPMS works (sampling and data flow)
- Grid-based plot design with square plots and linear plots to cover habitat types; random with respect to landscape to reduce bias.
- Field recording supports volunteers with varying botanical expertise; three participation levels and extensive guidance/training.
- Data input uses structured, systematized processes; verification through iRecord for expert validation.
- Analysis and reporting conducted by specialists; outputs disseminated via NPMS newsletters and peer-reviewed journals.

## Outputs, uncertainty, and data availability
- The NPMS dataset is updated annually to provide a snapshot of current conditions and changes over time.
- Outputs are designed to be publicly available for independent review.
- Uncertainty is incorporated into analyses via robust statistical modeling; results and limitations are communicated in outputs.

## Data management and access
- Data are stored in a centralized NPMS database at UKCEH (Wallingford).
- Versioned design and outputs are archived; data management aligned with established project standards and backups.
- Resource links and guidance are available on the NPMS website for survey guidance, indicator lists, and ID guides.

## Resources and references
- NPMS website and supporting documents for survey guidance and resources.
- List of journal articles, reports, and further reading on NPMS design, analysis, and application to ecological monitoring and policy-relevant indicators.

## Summary for analysts
- NPMS provides a structured, QA’d, volunteer-based plant and habitat monitoring dataset with clear data lineage and documentation.
- Data are organized into relational components (locations, samples, attributes, occurrences) with harmonised habitat and Domin score mappings.
- Robust QA, governance, and openness principles support reproducible analysis and policy-relevant reporting; data can be combined with other environmental datasets for broader monitoring and assessment.
- Key outputs include habitat change detection, understanding drivers, and contributing to biodiversity indicators, with data publicly available for scrutiny.