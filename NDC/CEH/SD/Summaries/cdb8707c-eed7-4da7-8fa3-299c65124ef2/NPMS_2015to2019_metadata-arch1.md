# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife, and JNCC to provide annual indications of changes in plant abundance and diversity.
- It supports volunteer recorders to monitor plants and habitat attributes in small plots using a structured methodology across the UK, Isle of Man, and Channel Islands.
- Objectives:
  - Detect changes in the quality of priority habitats.
  - Understand why changes occur (pressures and drivers).
  - Contribute data to the UK Biodiversity Indicator C7 (Plants of the wider countryside) by measuring changes in plant communities across important habitats.
- The data snapshot covers the NPMS database as held at CEH Wallingford and includes files described below (2015–2019) and related evidence quality assurance material.

## Overview of files provided

-locations_2015to2019.csv (size ~537 kb)
- sampleAttributes_2015to2019.csv (size ~7.82 mb)
- sampleInfoWithLatLong_2015to2019.csv (size ~1.78 mb)
- occurrences_2015to2019.csv (size ~10.66 mb)
- npmsHabitatLookup.csv (size ~2 kb)
- dominScores.csv (size ~1 kb)

- locations_2015to2019.csv
  - Provides a unique location identifier (location_id) and a location_type describing the survey plot (square or linear).

- sampleInfoWithLatLong_2015to2019.csv
  - Contains sampling events at a location with fields: id (sample), survey_id (NPMS survey type), date_start, location_id, entered_sref and entered_sref_system, created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country.

- sampleAttributes_2015to2019.csv
  - Links to samples via sample_id; includes attribute category (caption) and value (text_value).

- occurrences_2015to2019.csv
  - Records species occurrences with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C/V/R), sensitivity_precision (blurred records indicated by value 10000).

- npmsHabitatLookup.csv
  - Mapping between NPMS broad habitat and fine-scale habitat categories.

- dominScores.csv
  - Provides a harmonised dominIndex and midPoint for Domin cover-abundance categories across survey levels.

- Example: accessing habitat information
  - Demonstrates merging sampleInfoWithLatLong with sampleAttributes to filter for NPMS Habitat data (using R or SQL LEFT JOIN).

## Evidence Quality Assurance (EQA) of the NPMS

- The NPMS data are supported by a body of publications and reports listed for users to consult alongside NPMS guidance.
  - Journal articles include design, launch, and assessment of NPMS; methods for interval-censored plant cover data; and ecological monitoring with citizen science.
  - Other articles and internal/public reports cover NPMS development, cross-scheme considerations, and technical reviews.
- EQA questions addressed:

  - Q1: Peer review and involvement
    - Methods and outputs developed through workshops with statistical and botanical experts; habitat definitions peer-reviewed; field recording guided by volunteer training; data input and verification use an online, structured workflow with a species dictionary and geographic checks; iRecord verification for expert reviews; data publishing planned for public access; analysis by experienced ecologists using R; dissemination via NPMS newsletters and peer-reviewed publications.

  - Q2: Appropriate level of review/QA by process/output risk
    - A project Steering Group oversees work; external peer review conducted when risks warrant it (e.g., survey design workshop).

  - Q3: Communicating uncertainty, quality, assumptions, and limitations
    - Outputs are checked by scientists to ensure claims are evidence-based; NPMS invites constructive critique from the broader monitoring science community.

  - Q4: Avoiding biases in statistics
    - Robust statistical design enables uncertainty to be estimated through models.

  - Q5: Document tracking and version control
    - Design work is documented; versions are archived and backed up off-site per a CEH Data Management Plan; project management follows PRINCE2 standards.

## Data collection and governance

- Field recording
  - Conducted by volunteers with varying botanical expertise; three levels of involvement; comprehensive guidance and training provided.

- Data capture and verification
  - Online data capture ensures structured spatial data; automated checks (geographic range, etc.); iRecord provides expert verification for certain records.

- Data sharing and accessibility
  - NPMS data will be publicly available to enable independent review of results.

- Analysis and reporting
  - Results analyzed by quantitative ecologists using scripts in R; reporting produced by a team with botany, statistics, and communication expertise; dissemination through newsletters and peer-reviewed journals.