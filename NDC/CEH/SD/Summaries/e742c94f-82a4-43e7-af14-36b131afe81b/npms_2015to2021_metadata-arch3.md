# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC to provide an annual indication of changes in plant abundance and diversity across the UK, Isle of Man, and Channel Islands. It supports volunteer plant recorders to monitor plants and habitat attributes in small plots chosen through a structured methodology.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand why change is occurring (pressures and drivers).
  - Contribute data for the UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring change in plant communities in important habitats.
- Data are stored in the NPMS database at UKCEH Wallingford and are provided as an annually updated dataset. The document describes the files and the Evidence Quality Assurance (EQA) process used for NPMS, and references field guidance, indicator species lists, and ID guides.
- Guidance and resources for surveyors are available online, including older and updated versions of NPMS survey guidance and related materials.
- The document also includes an example of how to access habitat information and outlines how data are quality assured and published.

## Overview of files provided

- locations_2015to2021.csv (169 KB)
  - Provides a unique location identifier (location_id) and location_type describing the survey plot type (square or linear).
  - location_id links to sampleInfoWithLatLong_2015to2021.csv for repeated sampling events at the location.
- sampleInfoWithLatLong_2015to2021.csv (2,857 KB)
  - Contains information about individual samples: id, survey_id (type of NPMS survey: 87 Wildflower, 154 Inventory, 155 Indicator), date_start, location_id, entered_sref and entered_sref_system (spatial reference), created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country.
- sampleAttributes_2015to2021.csv (8,667 KB)
  - Additional data about samples linked to sampleInfoWithLatLong_2015to2021 by sample_id; includes sample_attribute_id, caption, text_value describing attribute categories and values (e.g., habitat information).
- occurrences_2015to2021.csv (13,464 KB)
  - Records species occurrences observed during sampling: id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), sensitivity_precision (e.g., blurred records for sensitive data).
- npmsHabitatLookup.csv (2 KB)
  - Lookup between NPMS broad habitat categories and NPMS fine-scale habitat categories.
- dominScores.csv (1 KB)
  - Lookup between domin scores and a harmonised Domin category list, including mid-point interpretations for cover-abundance categories.

## Example: accessing habitat information

- The dataset structure allows linking habitat information to samples via sampleInfoWithLatLong and sampleAttributes (caption = 'NPMS Habitat'), enabling retrieval of habitat data for each sample using standard database or R commands (example provided in the document).

## Application of Evidence Quality Assurance (EQA) of the NPMS

- The NPMS data and methods are supported by a range of publications and reports to underpin EQA. Key sources include:
  - Journal articles on design, launch, assessment, and statistical approaches for NPMS (e.g., Pescott et al. 2019; 2016; 2015).
  - Additional articles describing the monitoring approach and citizen science aspects (e.g., Walker et al. 2015; Pescott et al. 2015).
  - Internal and external reports related to NPMS design, inference methods, and cross-scheme considerations (e.g., Defra report, JNCC technical reviews).
- EQA questions addressed in NPMS documentation include:
  - How methods and publications were peer reviewed and who was involved.
  - How the correct level of review/quality assurance is decided based on risk.
  - How outputs communicate uncertainty, quality, assumptions, and limitations.
  - How biases are avoided in statistics and outputs.
  - How document tracking and version control are managed (PRINCE2 standards, data management plans, off-site backups).
- Outputs are subjected to scientist verification and are intended to be publicly available for independent review, with ongoing feedback from the monitoring community.

## Governance and quality assurance details (Q&A style highlights)

- Q1: Methods and publications are peer reviewed via expert workshops and project team review, with final approaches subjected to statistical and botanical expert input.
- Q2: Oversight by a project Steering Group; external peer review is used when risk justifies it (e.g., survey design).
- Q3: Uncertainty, quality, assumptions, and limitations are clearly communicated; outputs are checked by scientists to ensure claims are evidence-based.
- Q4: Bias avoidance through robust statistical design that supports uncertainty estimation via models.
- Q5: Document tracking and version control are enforced; design stages are archived and backed up off-site under a Data Management Plan aligned with PRINCE2 standards.