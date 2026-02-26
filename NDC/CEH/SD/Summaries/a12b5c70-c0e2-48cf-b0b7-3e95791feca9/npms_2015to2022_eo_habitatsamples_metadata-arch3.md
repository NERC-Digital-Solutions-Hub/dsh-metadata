# Habitat samples dataset

- The NPMS is a habitat-based plant monitoring scheme designed by BSBI, UK CEH, Plantlife and JNCC to provide annual indications of changes in plant abundance and diversity across the UK, Isle of Man, and Channel Islands.
- Aims include detecting change in priority habitats, understanding drivers/pressures behind change, and contributing data for the UK Biodiversity Indicator C7 (Plants of the wider countryside).
- The scheme supports volunteer plant recorders to monitor plants and habitat attributes in fixed plots using a structured methodology.

## Objectives and scope

- Detect change in the quality of priority habitats.
- Help understand why change is occurring (pressures and drivers).
- Contribute data for national biodiversity indicators through plant community monitoring in important habitats.
- Field guidance and survey resources are available (second edition, 2019).

## Data and dataset description

- Habitat samples dataset is based on NPMS data updates from 2015–2022 and supports training/validation for Earth Observation-based data products.
- The dataset pre-joins NPMS samples with surveyor habitat and includes information on habitat classification and whether surveyor-recorded habitats have changed over time at any plot location.
- An evidence quality assurance (EQA) framework underpins the dataset.

## File: npmsHabitatSamples_2015to2022.csv

- Provides information about individual plant community samples collected at fixed plot locations over time.
- Key fields include:
  - sample_id: unique NPMS fixed-plot sample identifier.
  - survey_id: NPMS survey code indicating survey level (e.g., Wildflower, Inventory, Indicator).
  - entered_sref / entered_sref_system: spatial reference for the sample.
  - created_on / created_by_id: data entry timestamps and submitter identity (anonymised).
  - LATITUDE / LONGITUDE: geographic coordinates.
  - monad / monadCRS: 1 km grid cell context and its CRS.
  - country: territory context.
  - surveyorHabitat / NPMS_hab_type / NPMS_broad_habitat: habitat classifications (fine or broad scale).
  - multipleHabs: flag indicating potential change in broad habitat for a fixed plot.
- The dataset supports the training and validation of EO-based products by providing harmonised habitat and change information.

## Evidence Quality Assurance (EQA) and supporting materials

- EQA framework and dataset guidance are supported by multiple publications:
  - Journal articles (examples): 
    - The design, launch and assessment of a volunteer-based plant monitoring scheme (PLOS ONE, 2019).
    - Ecological monitoring with citizen science (Biological Journal of the Linnean Society, 2015).
    - A comparison of models for interval-censored plant cover data (PeerJ Preprints, 2016).
  - Other published articles and internal/research reports detailing NPMS design, implementation, and data use.
  - Reports on the use of NPMS data for inferences on air pollution impacts; design reports for NPMS development; technical reviews.
- Q1–Q5 framework questions guide quality assurance and governance:
  - Q1: Partnership peer review and involvement in sample design, habitat definitions, and target species selection; field recording guided for volunteer involvement; data input and verification via structured systems; results analysis by experienced ecologists; dissemination through newsletters and journals.
  - Q2: Oversight by a project Steering Group with external peer review where risk warrants; design workshop involvement for critical aspects.
  - Q3: Outputs checked by scientists to ensure claims are evidence-based; openness to external critique from monitoring science community.
  - Q4: Biases mitigated through robust statistical design enabling uncertainty estimation.
  - Q5: Document tracking and version control governed by a Data Management Plan and PRINCE2 project management standards; off-site backups.

## Design and implementation

- Sample stratification and survey design: Developed with expert input; final approach uses a regular grid of square plots and gridlines for linear plots to ensure random sampling with respect to the landscape.
- Habitat definitions: Developed via peer review with habitat experts.
- Target species indicators: Selected using an objective method and reviewed by the project team for suitability and volunteer engagement.
- Field recording: Conducted by volunteers with varying botanical expertise; three levels of participation; comprehensive guidance and training provided.
- Data input and verification: Online data capture with structured spatial database; use of a species dictionary, calendar dates, map-based locations, controlled terms; automated geographic range checks; verification via the iRecord system for expert review.
- Data publishing: Outputs will be publicly available to enable independent review.
- Analysis and reporting: Conducted by experienced quantitative ecologists using R; dissemination through NPMS newsletters and peer-reviewed publications.

## Governance, risk, and data management

- Outputs undergo scientific review to ensure they are supported by evidence.
- Steering Group oversight with selective external peer review based on risk.
- Versioning and document tracking are maintained under a formal Data Management Plan; backups stored off-site; alignment with PRINCE2 standards.
- Commitment to transparency and public data sharing to enable independent validation and broader use.

## Relevance for monitoring-framework authors

- Demonstrates a structured, governance-driven approach to designing and implementing a national monitoring framework that:
  - Balances scientific rigor with volunteer-based data collection.
  - Integrates metadata, data quality checks, and provenance to support data reuse and transparency.
  - Addresses common monitoring challenges: data gaps, access, metadata adequacy, data transformation needs, and clear communication of uncertainty and limitations.
  - Establishes clear pathways for data sharing, stakeholder engagement, and ongoing quality assurance.