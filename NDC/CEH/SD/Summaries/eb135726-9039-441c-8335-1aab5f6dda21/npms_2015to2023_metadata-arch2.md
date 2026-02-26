# National Plant Monitoring Scheme survey data (2015-2023)

## Overview
- Plot-level plant occurrence data for 2015–2023 across the UK, Channel Islands, and Isle of Man.
- Observations at metre scale with Domin frequency-abundance cover data.
- Includes plot type, habitat, sampling date, and precise spatial location to enable reconstruction of sampling histories and gaps.

## Data contents and structure
- Files provided:
  - locations_2015to2023.csv: unique location identifiers, location type, and sample counts per location.
  - sampleInfoWithLatLong_2015to2023.csv: sampling events with sample ID, survey type, date, location linkage, spatial reference, creator, and lat/long details.
  - sampleAttributes_2015to2023.csv: additional data about samples linked to samples via sample_id (e.g., habitat information).
  - occurrences_2015to2023.csv: species observations with taxon names, Domin cover scores, verification status, and sensitivity info.
  - npmsHabitatLookup.csv: mapping between NPMS broad and fine habitat categories.
  - dominScores.csv: harmonised Domin score mappings and mid-point interpretations.
- Data relationships:
  - location_id links locations to repeated samples (sampleInfoWithLatLong_2015to2023.csv).
  - sample_id connects sampleAttributes to each sampling event.
  - occurrences connect to samples via sample_id, carrying taxon and Domin data.

## Data collection, processing, and storage
- Collected by volunteers through the Indicia system (PostgreSQL/PostGIS) via NPMS website or app.
- Master NPMS data reside in a central database; extracted for this resource via SQL queries.
- Data are intended to be stored, versioned, and accessible through appropriate portals.

## NPMS background and aims
- NPMS is a habitat-based plant monitoring program designed by BSBI, CEH, Plantlife, and JNCC.
- Objectives:
  - Detect changes in the quality of priority habitats.
  - Understand drivers and pressures behind changes.
  - Contribute to the UK Biodiversity Indicator on plants in the wider countryside.
- Methodology features:
  - Structured survey plots (grid-based squares and linear plots) across relevant landscapes.
  - Volunteer participation with tiered guidance and training.
  - Data capture with standardized fields, species dictionaries, and automated quality checks.
- Outputs are updated annually and stored at UKCEH Wallingford; supplementary survey guidance and resources are available online.

## Evidence Quality Assurance (EQA) and governance
- EQA framework supported by multiple publications and internal guidance.
- Key design elements underpinning quality:
  - Sample stratification and survey design (randomized grid/linear plots).
  - Habitat definitions and habitat indicator selection.
  - Field recording with three levels of contributor expertise plus training.
  - Online data input with standardized structures, spatial checks, and iRecord verification for expert review.
  - Public data publishing to enable independent review.
  - Analysis conducted by experienced quantitative ecologists using R; results disseminated via newsletters and peer-reviewed publications.
- Governance and review:
  - Project Steering Group oversees activities; external peer review for higher-risk outputs.
  - Uncertainty, limitations, and assumptions are explicitly addressed in outputs.
  - Robust design employed to minimize bias; uncertainty estimated via models.
  - Document tracking and version control implemented under a UK CEH Data Management Plan with PRINCE2 project management standards.

## Outputs, analysis, and usage
- The dataset supports:
  - Annual indicators of plant abundance and diversity changes.
  - Assessment of habitat change and understanding drivers of change.
  - Contribution to national biodiversity reporting.
- Analysis and reporting:
  - Conducted by a team with botany, statistics, and communication expertise.
  - Outputs include NPMS newsletters and peer-reviewed journal publications.
- Data accessibility:
  - Data from the NPMS are intended to be publicly available to enable independent review and reuse.

## Access notes and practical guidance
- Example workflows show how to retrieve habitat information by joining sampleInfoWithLatLong and sampleAttributes on sample_id, using either R or SQL.
- Data include rich metadata to reconstruct sampling histories, monitor consistency over time, and enable integration with other datasets.

## Data management and reproducibility
- All design and output documents are archived with off-site backups.
- Versioned documentation and data management practices align with PRINCE2 standards and the project’s Data Management Plan.

## Relevance to Analysts Monitoring the Environment
- Provides standardized, longitudinal, plot-level plant data suitable for evaluating environmental health and policy performance over time.
- Facilitates cross-dataset comparisons through harmonised habitat and Domin categorisations.
- Emphasizes data quality, transparency, and public accessibility to support scrutiny and policy evaluation.