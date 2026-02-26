# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring initiative created by BSBI, UKCEH, Plantlife and JNCC to annually indicate changes in plant abundance and diversity.
- It supports volunteer recorders to monitor plants and habitat attributes in small plots across the UK, Isle of Man, and Channel Islands, using a structured sampling approach.
- Objectives:
  - Detect changes in priority habitat quality.
  - Understand drivers and pressures behind changes.
  - Contribute data to UK Biodiversity Indicator C7 (plants of the wider countryside) by measuring plant community changes across important habitats.
- The document describes the NPMS data files, their contents, and the evidence quality assurance (EQA) process for NPMS.

## Data architecture and files

- Files provided (summary of contents):
  - locations_2015to2021.csv: unique location identifiers and location type (e.g., square or linear plots).
  - sampleInfoWithLatLong_2015to2021.csv: sampling events at each location, including sample id, survey type, date, location linkage, spatial references, creator, coordinates, and recorder details.
  - sampleAttributes_2015to2021.csv: additional sample data linked to samples via sample_id (text descriptors and values).
  - occurrences_2015to2021.csv: species occurrences per sample, including taxon keys, preferred names, abundance (domin), verification status, and sensitivity.
  - npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale categories.
  - dominScores.csv: harmonised domin (cover-abundance) scores and mid-point interpretations for cross-survey compatibility.
- Example data linkage:
  - location_id links locations_2015to2021.csv to sampleInfoWithLatLong_2015to2021.csv.
  - sampleAttributes_2015to2021.csv links to samples via sample_id to provide habitat and other attributes.
- A sample workflow shows how to combine habitat information using these tables (e.g., merging sampleInfoWithLatLong with sampleAttributes filtered for NPMS Habitat).

## Data quality assurance and governance

- EQA and supporting publications underpin NPMS data quality, including design, monitoring, and analysis methods.
- Verification and data handling:
  - Observations are verified via the iRecord system (BSBI-affiliated botanical experts) for certain records; a verification status field indicates C (not reviewed), V (verified), or R (rejected).
  - Spatial data may be blurred for sensitive records (sensitivity_precision column).
  - Data input uses structured spatial databases, species dictionaries, calendar dates, and controlled terms to minimize entry errors; geographic range checks are performed automatically.
- Data publication and accessibility:
  - NPMS data will be publicly available to permit independent review.
  - Analysis is conducted by experienced ecologists using R; results disseminated via newsletters and peer-reviewed journals.
- Q&A style governance and QA considerations:
  - Q1: Methods and publications were peer reviewed where feasible; project design involved statistical and botanical experts; field design includes regular grids for square plots and gridlines for linear plots.
  - Q2: An oversees structure via a project Steering Group; external peer review applied where risk is higher.
  - Q3: Outputs clearly communicate uncertainties and limitations; subjected to scientist review before publication.
  - Q4: Bias avoidance through robust statistical design enabling uncertainty estimation by models.
  - Q5: Document tracking and version control via a Data Management Plan; design work archived and backed up off-site, aligning with PRINCE2 project management standards.

## Data access, interoperability, and usage

- Data sharing and discovery:
  - Data are intended to be publicly available for independent review and reuse.
  - The dataset uses harmonised and cross-referenced tables (e.g., dominScores, NPMS habitat mappings) to support cross-survey comparability.
- Practical integration guidance:
  - Linking tables facilitates extraction of habitat information for samples (example provided in the document).
  - Data can be accessed or joined via common keys like id, sample_id, and location_id in SQL or R workflows.
- Audience and impact:
  - Data support estimation of habitat change, drivers of change, and contribution to national biodiversity indicators.
  - Results are disseminated to researchers, volunteers, policy-makers, and the general public.

## Relevance for Data Leaders

- Strategic data governance:
  - Clear data model with linked location, sample, attribute, and occurrence data enabling end-to-end tracking of data lineage.
  - Emphasis on metadata, standardised vocabulary, and harmonisation (domin scores, habitat mappings) to ensure comparability across survey types and time.
- Data quality management:
  - Integrated EQA framework, including automated validation, external verification, and explicit handling of sensitive data.
  - Transparent uncertainty communication and methodological documentation to support credible decision-making.
- Data availability and collaboration:
  - Public data publishing approach facilitates external scrutiny, reproducibility, and wider community engagement.
  - Governance structure (Steering Group, potential external reviews) supports risk-aware data management and continuous improvement.
- Operational guidance for data strategy:
  - Robust version control and an overarching Data Management Plan; adherence to PRINCE2 standards for project management.
  - Emphasis on discovering and integrating data across partners and networks while maintaining data quality and discoverability.

## Resources and references

- NPMS website resources and survey guidance, habitat definitions, indicator species lists, and ID guides.
- Evidence Quality Assurance publications and project reports (journal articles, reports, and technical reviews) related to NPMS design, analysis, and application.