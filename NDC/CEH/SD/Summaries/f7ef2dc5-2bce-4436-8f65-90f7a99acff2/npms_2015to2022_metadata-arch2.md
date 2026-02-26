# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring initiative designed by BSBI, UK CEH, Plantlife and JNCC.
- Aims to provide an annual indication of changes in plant abundance and diversity.
- Supports volunteer plant recorders to monitor plants and habitat attributes using small plots across the UK, Isle of Man, and Channel Islands.
- Objectives include detecting changes in priority habitat quality, understanding drivers/pressures behind change, and contributing data to the UK Biodiversity Indicator 'C7 Plants of the wider countryside'.
- The NPMS dataset is continually updated and stored at UKCEH Wallingford; this documentation describes the files provided and the Evidence Quality Assurance (EQA) process.

## NPMS Data, Scope and Guidance

- NPMS collects data in a structured, standardized way to enable temporal comparisons and policy evaluation.
- Field recording guidance and related resources for surveyors are provided (with links to NPMS guidance and resources for surveyors).

## Overview of Files Provided

- locations_2015to2022.csv: unique location identifiers and survey plot type (square or linear).
- sampleInfoWithLatLong_2015to2022.csv: sampling events per location, including sample id, survey_id, date, location_id, spatial reference details, timestamps, recorder ID, latitude, longitude, monad and related CRS, and country.
- sampleAttributes_2015to2022.csv: additional data captured about samples, linked to samples via sample_id; includes attribute category and text_value.
- occurrences_2015to2022.csv: species occurrences with fields for id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status, and sensitivity_precision (e.g., blurred records).
- npmsHabitatLookup.csv: mapping between NPMS broad habitat and fine-scale habitat categories.
- dominScores.csv: harmonised Domin score mappings and mid-point interpretations to enable consistent magnitude interpretation across survey types.

## Accessing Habitat Information (Example)

- Habitat information can be retrieved by joining sampleInfoWithLatLong_2015to2022.csv with sampleAttributes_2015to2022.csv on sample_id where caption equals NPMS Habitat.

- Example approach (conceptual):
  - Load sampleInfoWithLatLong_2015to2022.csv and sampleAttributes_2015to2022.csv
  - Filter sampleAttributes where caption == 'NPMS Habitat'
  - Merge on sample_id to obtain habitat data per sample

## Application of Evidence Quality Assurance (EQA)

- Publications supporting EQA for NPMS include several journal articles, other published articles, and technical/research reports.
  - Key journal articles: design, launch and assessment of NPMS; ecological monitoring with citizen science; models for interval-censored plant cover data; and related communications.
  - Other articles and reports: broader NPMS developments, design histories, and methodological advances (e.g., occupancy/abundance indicators, cross-scheme considerations, etc.).
  - Numerous internal and external reports detailing design, QA processes, and methodological development.
- EQA context covers:
  - Sample stratification, survey design, habitat definitions, target species indicator selection, field recording, data input/verification, data publishing, analysis, and reporting.
  - Availability of data for independent review and publication of results.
  - Use of expert review and workshop-based peer input for high-risk elements.
  - Communication of uncertainty and limitations, with evidence-based claims and openness to external critique.
  - Robust statistical design to manage biases and uncertainty.
  - Documentation and version control aligned with a Data Management Plan and PRINCE2 project management standards.

## Access and Quality Assurance of Outputs

- Outputs (newsletters, reports, publications) are reviewed by scientists to ensure claims are evidence-based.
- The NPMS engages with external ecologists and encourages ongoing critique and feedback.
- Uncertainty and limitations are acknowledged through model-based uncertainty estimates and transparent reporting.

## Governance, Review and Documentation

- Oversight by a project Steering Group; external peer review is applied where risk warrants.
- Design and outputs are tracked with versioned documentation; components are backed up off-site per the UK CEH Data Management Plan.
- Organization and reporting involve expert teams in botany, statistics, and science communication, with dissemination through newsletters and peer-reviewed journals.

## Challenges for Analysts Monitoring the Environment

- Increasing the value of NPMS datasets by integrating with other relevant data sources (avoiding single-use datasets).
- Enabling broad access to underlying data used to generate final outputs.