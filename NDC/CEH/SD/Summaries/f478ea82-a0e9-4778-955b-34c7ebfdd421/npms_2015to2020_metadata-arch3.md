# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring program designed by BSBI, UKCEH, Plantlife and JNCC to provide an annual indication of changes in plant abundance and diversity.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand driving pressures behind changes.
  - Contribute data for the UK Biodiversity Indicator C7 (Plants of the wider countryside) by measuring plant community changes across important habitats.
- The dataset is updated annually and reflects the NPMS database at UKCEH Wallingford. It supports volunteer plant recorders and habitat attribute monitoring in small plots across the UK, Isle of Man, and Channel Islands.
- This document describes:
  - The files provided and their contents.
  - The evidence quality assurance (EQA) process used for NPMS data.

## Overview of files provided

- locationTypes_2015to2020.csv: Links a unique location_id to a survey plot type (e.g., square or linear) and ties to repeated sampling events.
- sampleInfoWithLatLong_2015to2020.csv: Contains sample-level information, including survey_id, date, location_id, spatial reference (entered_sref and entered_sref_system), creation metadata, recorder identifier, latitude/longitude, monad (1 km square), monadCRS, and country.
- sampleAttributes_2015to2020.csv: Additional data about samples, linked by sample_id; includes attribute category (caption) and text_value.
- occurrences_2015to2020.csv: Records species occurrences with fields for id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (verification), and sensitivity_precision (sensitive records blurred to 10 km if applicable).
- npmsHabitatLookup.csv: Mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv: Lookup between Domin values and harmonised categories, with midPoint interpretations for cover-concept scales.

## Example: accessing habitat information

- The files can be joined to extract habitat information for samples (e.g., merge sampleInfoWithLatLong with sampleAttributesWhere caption = 'NPMS Habitat') to obtain habitat context for each sample.

## Application of Evidence Quality Assurance (EQA) for NPMS

- NPMS data quality is supported by a body of publications and guidance available on the NPMS website, including:
  - Design, launch, and assessment of a volunteer-based plant monitoring scheme (Pescott et al., 2019).
  - Evaluation of interval-censored plant cover data models (Pescott et al., 2016).
  - Design and implementation discussions for citizen-science plant monitoring in Britain and Ireland (Pescott et al., 2015).
- Additional related articles and internal/commissioned reports detail the NPMS design, data use for air pollution inference, Bayesian occupancy/abundance indicators, and cross-scheme considerations.
- Governance and QA questions addressed:
  - Q1: Partnership peer review and involvement in design and outputs (habitat definitions, survey design, target species, field recording, data input/verification, and reporting).
  - Q2: Appropriate levels of external review based on risk; project Steering Group oversight; external expert workshops for survey design.
  - Q3: Communication of uncertainty, quality, assumptions, and limitations; outputs reviewed by scientists to ensure evidence-based claims.
  - Q4: Bias prevention through robust statistical design enabling uncertainty estimation via models.
  - Q5: Document tracking and version control via a Data Management Plan and PRINCE2-compliant project management; archival of report versions and off-site backups.

## Data collection, processing and dissemination workflow

- Design and sampling:
  - Regular grid plots (squares) and gridlines for linear plots; habitat definitions developed with habitat experts; habitat indicators selected to balance scientific usefulness and volunteer engagement.
- Field recording:
  - Volunteer involvement with varied botanical expertise; three levels of contribution; comprehensive guidance and training provided.
- Data input and verification:
  - Online data capture with structured spatial databases; use of a species dictionary, standardized dates, controlled habitat terms, and geo-range checks.
  - Verification through iRecord (BSBI-affiliated) for records requiring higher expertise.
- Analysis and reporting:
  - Analyses performed by experienced quantitative ecologists using R scripts.
  - Results disseminated via NPMS newsletters and peer-reviewed journal publications.
- Data sharing and governance:
  - Data published publicly to enable independent review.
  - Data management plans and standard project governance (PRINCE2) underpin versioning, storage, and updates.

## Relevance to monitoring framework authors

- NPMS demonstrates a comprehensive monitoring framework with:
  - Clear aims tied to policy-relevant indicators (habitat quality, driver identification, and biodiversity indicators).
  - Structured data architecture linking locations, samples, attributes, and species occurrences.
  - Emphasis on data quality assurance, metadata, and verifiable data flows from field collection to published outputs.
  - Open data publishing and a governance framework (Steering Group, external reviews, and data management practices) to manage risks and maintain transparency.
  - Documentation of uncertainties and limitations, with robust statistical design to quantify and communicate these aspects.
- Key challenges acknowledged and addressed align with typical Monitoring Framework archetype concerns:
  - Data gaps and accessibility are mitigated by volunteer-led data collection, standardized metadata practices, and public data sharing.
  - Silos are avoided through integrated data models and centralized, open-referenced datasets with clear provenance.
  - Metadata adequacy and data transformation are supported by explicit field definitions, reference dictionaries, and harmonised scales (Domin).
  - Data governance ensures datasets meet standards, are stored and updated appropriately, and are openly accessible for scrutiny and policy use.