# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring program designed by BSBI, UKCEH, Plantlife, and JNCC to annually track changes in plant abundance and diversity.
- It supports volunteer plant recorders surveying plants and habitat attributes in standardized plots across the UK, Isle of Man, and Channel Islands.
- Objectives:
  - Detect change in priority habitats.
  - Understand drivers and pressures behind change.
  - Contribute to the UK Biodiversity Indicator ‘C7 Plants of the wider countryside’ by measuring plant community change across important habitats.
- The document provides an overview of the NPMS dataset held at UKCEH Wallingford and the Evidence Quality Assurance (EQA) process used for NPMS.

## Dataset scope and contents

- The dataset is updated annually and includes:
  - locationTypes_2015to2020.csv
  - sampleAttributes_2015to2020.csv
  - sampleInfoWithLatLong_2015to2020.csv
  - occurrences_2015to2020.csv
  - npmsHabitatLookup.csv
  - dominScores.csv
- Data purpose is to describe sampling locations, samples, plant occurrences, habitat classifications, and harmonized abundance metrics.

## Dataset structure and key fields

- locationTypes_2015to2020.csv
  - location_id: unique location identifier
  - location_type: survey plot type (e.g., square, linear)
- sampleInfoWithLatLong_2015to2020.csv
  - id: sample identifier
  - survey_id: NPMS survey type (e.g., Wildflower, Inventory, Indicator)
  - date_start: sample date
  - location_id: links to locationTypes_2015to2020.csv
  - entered_sref / entered_sref_system: spatial reference and CRS (e.g., OSGB, 4326)
  - monad / monadCRS / country: spatial context at 1 km monad level
  - created_on / created_by_id: provenance metadata
- sampleAttributes_2015to2020.csv
  - sample_attribute_id / sample_id: linkage to sample
  - caption / text_value: description and value of the attribute (e.g., habitat)
- occurrences_2015to2020.csv
  - id: occurrence identifier
  - sample_id: links to sample
  - taxonversionkey / preferred_taxon: taxon identity
  - domin: Domin (cover) score for the occurrence
  - record_status: verification status (C = not reviewed, V = verified, R = rejected)
  - sensitivity_precision: clarity on spatial sensitivity (e.g., blurred data at 10 km)
- npmsHabitatLookup.csv
  - NPMS_broad_habitat / NPMS_fine-scale_habitat: habitat classification mapping
- dominScores.csv
  - domin: observed Domin value
  - dominIndex / midPoint: harmonized, interpretable cover metrics

## Data relationships and metadata practices

- Linking structure:
  - location_id in sampleInfoWithLatLong_2015to2020.csv connects samples to placement locations in locationTypes_2015to2020.csv.
  - sampleInfoWithLatLong_2015to2020.csv connects to sampleAttributes_2015to2020.csv via sample_id for habitat and other attributes.
  - occurrences_2015to2020.csv connects to samples via sample_id, with taxon data and Domin values.
- Metadata and provenance:
  - Created_by_id records which user submitted data; created_on timestamps data entry.
  - entered_sref and monadCRS denote spatial referencing; sensitivity_precision indicates if data are spatially blurred.
- Data harmonization:
  - Habitats and Domin scores are harmonized through lookups (npmsHabitatLookup.csv, dominScores.csv) to support cross-survey comparability.

## Evidence Quality Assurance (EQA) and governance

- EQA basis:
  - NPMS data quality is supported by published methodological research and project reports; users are urged to consult specific journal articles and CEH/BSBI/NERC materials.
- Key QA framework and outputs:
  - Design and sampling strategy developed with statistical and botanical input; grid-based plots and linear plots with randomization for unbiased sampling.
  - Habitat definitions and target species were peer-reviewed; data input uses controlled terms, a species dictionary, and automated checks.
  - Data verification via iRecord (botanical experts) for higher-level reviews; online data capture with structured spatial database.
  - Analysis conducted by experienced ecologists using R; results disseminated through NPMS newsletters and peer-reviewed publications.
- QA governance and risk management:
  - NPMS overseen by a project Steering Group; external peer review used where risk warrants it (e.g., survey design).
  - Outputs checked by scientists to ensure claims are evidence-supported; outputs subject to ongoing expert critique from the monitoring community at CEH.
  - Uncertainty and limitations are communicated in outputs; robust statistical design enables uncertainty estimation.
  - Documentation and version control:
    - All design work documented; versions archived and backed up off-site per CEH Data Management Plan; project management adheres to PRINCE2 standards.

## Data access, sharing and use

- Data will be publicly accessible to allow independent review and use.
- Survey guidance and supporting documents are available to surveyors, with resources for data handling and analysis.
- Users are encouraged to refer to EQA publications and methodological papers for proper interpretation and limitations.

## Challenges and considerations for data stewards

- Data stewardship challenges relevant to NPMS:
  - Ensuring timely data submission from volunteers and aligning with standard metadata.
  - Achieving consistency in metadata (locations, dates, methods) across multiple survey types and years.
  - Managing large, multi-table datasets with complex linking and harmonization requirements.
  - Maintaining interoperability across different systems and formats and ensuring data accuracy, including geopositioning and taxon names.
  - Balancing data openness with sensitivity (e.g., blurred locations) and verification statuses.

## Summary for data governance and stewardship

- NPMS provides a well-structured, openly shareable plant monitoring dataset with clearly defined linking between locations, samples, attributes, and occurrences.
- Standardized metadata, spatial referencing, and harmonized habitat/ Domin classifications support cross-study comparability and long-term trend analysis.
- Provenance, quality assurance, and version control are embedded in the data lifecycle, with an explicit governance framework and risk-based review processes.
- Users should consult the cited QA literature and project documentation for uncertainty, methods, and limitations, and should rely on the PRINCE2-based data management approach for repository stability and reproducibility.