# Habitat samples dataset

- The NPMS (National Plant Monitoring Scheme) is a habitat-based plant monitoring program in the UK designed to provide annual indications of changes in plant abundance and diversity. It supports volunteer recorders to monitor plants and habitat attributes in fixed plots across the UK, Isle of Man, and Channel Islands.
- Objectives include: detecting changes in priority habitats, understanding drivers/pressures behind change, and contributing to UK Biodiversity Indicator C7 (plants of the wider countryside).

## Dataset purpose and scope

- Provides pre-joined NPMS samples with recorded surveyor habitat and additional habitat classification information.
- Includes information on whether surveyor-recorded habitats have changed over time for given plot locations.
- Aims to support training and validation of Earth Observation–based data products.
- Part of NPMS data collection (EIDC) with evidence quality assurance context.

## Dataset contents

- File: npmsHabitatSamples_2015to2022.csv (approx. 4.3 MB)
- Key fields include:
  - sample_id: unique NPMS fixed-plot sample identifier
  - survey_id: NPMS survey code (e.g., 87 Wildflower, 154 Inventory, 155 Indicator)
  - entered_sref / entered_sref_system: spatial reference for the sample
  - created_on / created_by_id: data entry timing and submitter
  - LATITUDE / LONGITUDE: sample location coordinates
  - monad / monadCRS: 1 km square (monad) and its coordinate system
  - country: territory context (Britain, Channel Islands, Northern Ireland)
  - surveyorHabitat / NPMS_hab_type / NPMS_broad_habitat: habitat classifications (fine or broad scale as recorded)
  - multipleHabs: indicator whether broad habitat changed between samples (Y/N)

## Data collection and processing workflow

- Plot design: fixed-grid plots with regular sampling, using gridlines for randomization to avoid landscape bias.
- Survey types: Wildflower, Inventory, and Indicator surveys, with varying levels of surveyor botanical expertise.
- Field recording: volunteer-based with training; three levels of contribution; guidance and training provided.
- Data entry and verification:
  - Online data capture with structured fields and controlled terms (habitats, dates, vegetation height, cover values).
  - Automated checks (e.g., geographic range validation); exceptions reviewed via the iRecord system (BSBI-affiliated experts).
- Analysis and publishing:
  - Results analyzed by experienced quantitative ecologists using R scripts.
  - Outputs disseminated through NPMS newsletters and peer-reviewed publications.

## Evidence Quality Assurance (EQA) framework

- Publications underpinning EQA include peer-reviewed articles, practical reports, and technical reviews (see NPMS references).
- Design and development questions (Q1–Q5) address governance and quality:
  - Q1: Methods and peer review; design workshops with statistical and botanical experts; camera-ready survey design and habitat definitions vetted by experts.
  - Q2: Quality control levels set by a project Steering Group; external peer reviews as needed.
  - Q3: Uncertainty and limitations communicated; outputs reviewed to ensure claims are evidence-based.
  - Q4: Bias minimization via robust statistical design enabling uncertainty estimation through modeling.
  - Q5: Version-controlled documentation and data management (PRINCE2 standard; off-site backups).

## Outputs, access, and usability

- Data will be publicly available to enable independent review and reuse.
- Supports training and validation of EO-based data products; allows integration with other data sources to increase dataset value.
- Outputs include newsletters and peer-reviewed publications; results intended for researchers, volunteers, policymakers, and the public.

## Governance, monitoring, and continuity

- Steering Group oversight with potential external peer input.
- Continuous opportunities for feedback from the broader Monitoring science community within CEH.
- Documentation and data management are standardized, version-controlled, and backed up.