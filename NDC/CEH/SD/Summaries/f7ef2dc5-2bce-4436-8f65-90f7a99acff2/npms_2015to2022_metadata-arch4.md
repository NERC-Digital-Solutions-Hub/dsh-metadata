# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UK CEH, Plantlife and JNCC.
- Purpose: collect data to provide an annual indication of changes in plant abundance and diversity; supports volunteer plant recorders to monitor plants and habitat attributes in small plots across the UK, Isle of Man and Channel Islands.
- Objectives:
  - Detect changes in the quality of priority habitats.
  - Understand why changes occur (pressures and drivers).
  - Contribute data for UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring change in plant communities across important habitats.
- This document describes the files in the NPMS dataset, the evidence quality assurance (EQA) process, and how data are managed and used.

## Datasets and File Structure

- locations_2015to2022.csv: Unique location_id with location_type (square or linear plot); links to repeated sampling events via location_id in the sampleInfoWithLatLong_2015to2022.csv.
- sampleInfoWithLatLong_2015to2022.csv: Records for individual samples at a location; fields include id, survey_id (97: Wildflower, 154: Inventory, 155: Indicator), date_start, entered_sref, coordinate system, created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country.
- sampleAttributes_2015to2022.csv: Additional data about samples; fields include sample_attribute_id, sample_id, caption, text_value; used to describe habitat attributes (e.g., NPMS Habitat).
- occurrences_2015to2022.csv: Species occurrences observed during sampling; fields include id, sample_id, taxonversionkey, preferred_taxon, domin (Domin scale), record_status (C=not reviewed, V=verified, R=rejected), sensitivity_precision (10000 indicates spatially blurred records).
- npmsHabitatLookup.csv: Mapping between NPMS broad habitat categories and fine-scale habitats.
- dominScores.csv: Harmonised domin score mappings; includes domin, dominIndex, midPoint to standardise cover-abundance data across survey forms.
- Example provided shows how to join sampleHabitat information from sampleAttributes to sampleInfoWithLatLong using SQL or R to access NPMS habitat data.

## Data Quality Assurance and Evidence

- EQA framework and supporting publications underpin data quality and interpretation.
  - Key journal articles: design and assessment of NPMS (Pescott et al. 2019; 2015; 2016); comparisons of interval-censored plant cover data; ecological monitoring with citizen science.
  - Other articles and reports describe NPMS development, data use for air pollution inferences, Bayesian occupancy/abundance indicators, and cross-scheme considerations.
- QA processes and governance:
  - Sample design and survey design developed with statistical and botanical experts; regular grid of square plots and gridlines for linear plots; habitat definitions peer-reviewed; target species list developed with project team.
  - Field recording involves volunteers with varying botanical expertise; three contribution levels and training; guidance provided.
  - Data input and verification via online capture, species dictionary, standardized metadata (dates, locations, habitats, Domin values); automated geographic range checks; iRecord verification for expert review of certain records.
  - Data publication is planned to be publicly accessible for independent review.
  - Analysis conducted by experienced ecologists using R; results disseminated via NPMS newsletters and peer-reviewed journals.
- QA questions addressed:
  - Peer review and stakeholder involvement in methods and publications; oversight by a project Steering Group; external peer review for risk-related outputs.
  - Communication of uncertainty, quality, assumptions, and limitations through outputs checked by scientists.
  - Bias avoidance via robust statistical design enabling uncertainty estimation.
  - Document tracking and version control through a Data Management Plan and PRINCE2-compliant practices; design work documented with archived versions and off-site backups.

## Access, Use, and Dissemination

- The NPMS dataset provides a snapshot of the current state of the NPMS database held at UKCEH Wallingford.
- Data will be publicly available to allow independent review of results.
- The document provides guidance on programmatic access (example in R) and outlines how data can be merged to retrieve habitat information for samples.

## Design, Methodology, and Data Stewardship Highlights

- Sampling design:
  - Regular grid of square plots and a set of linear plot lines to cover diverse habitats; grid-based design chosen for spatial randomness relative to underlying landscapes.
  - Habitat definitions developed through peer review with habitat experts.
  - Target species indicators selected via objective methods and project team review to balance scientific relevance with volunteer engagement.
- Field recording and training:
  - Field data collected by volunteers with varying botanical expertise; three contribution levels; training and guidance provided.
- Data handling:
  - Online data capture ensures structured spatial data; use of species dictionaries; controlled terms for habitats and associated metadata; automated verification checks.
  - iRecord used for expert verification of certain records.
  - Data management adheres to a formal plan with versioning and backups.
- Analysis and reporting:
  - Analyses conducted by quantitative ecologists; results disseminated through newsletters and peer-reviewed publications.
  - Clear communication of uncertainties and limitations in outputs.

## Implications and Considerations for Data Leaders

- NPMS demonstrates a multi-file, linked dataset approach with clear identifiers (location_id, id, sample_id) and harmonised taxonomic and cover data (domin, dominScores).
- Emphasizes the importance of:
  - Robust data governance, version control, and data management planning (PRINCE2 framework).
  - Public data release while maintaining appropriate verification workflows (eRecord) and metadata standards.
  - Collaboration across institutions (BSBI, CEH, Plantlife, JNCC) and engagement with volunteer networks, ensuring data quality without compromising inclusivity.
  - Documented QA processes, external peer review, and explicit handling of uncertainty and limitations in outputs.
- For wider data strategy, NPMS highlights practices to improve discoverability, metadata comprehensiveness, and cross-scheme data integration (habitat mappings, harmonised domin scores) to enable broader biodiversity indicators and policy-relevant insights.