# The National Plant Monitoring Scheme (NPMS)

- Purpose and scope
  - NPMS is a habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife, and JNCC to collect annual data on plant abundance and diversity.
  - It supports volunteer plant recorders to monitor plants and habitat attributes across the UK, Isle of Man, and Channel Islands.
  - Objectives:
    - Detect changes in the quality of priority habitats.
    - Understand why changes occur (pressures and drivers).
    - Contribute data for UK Biodiversity Indicator C7 (Plants of the wider countryside) by measuring plant community changes in key habitats.
  - The dataset provides an annually updated snapshot of the NPMS database held at CEH Wallingford and is supported by field recording guidance and survey resources.

- Overview of files provided (2015–2019)
  - locations_2015to2019.csv: Unique location_id and location_type describing survey plots (square or linear) and links to repeated sampling events.
  - sampleInfoWithLatLong_2015to2019.csv: Sample-level information including id, survey_id (87 = Wildflower, 154 = Inventory, 155 = Indicator), date_start, location_id, entered_sref and system, created_on, created_by_id, latitude, longitude, monad, monadCRS, country.
  - sampleAttributes_2015to2019.csv: Additional volunteer-collected attributes linked to samples via sample_id; includes caption and text_value.
  - occurrences_2015to2019.csv: Species occurrences with fields such as id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), and sensitivity_precision (blurred records).
  - npmsHabitatLookup.csv: Mapping between NPMS broad habitat and fine-scale habitat categories.
  - dominScores.csv: Harmonised Domin score mappings, including dominIndex and midPoint for consistent cover estimates across survey types.
  
- How the data are structured and linked
  - location_id in locations_2015to2019.csv links to sampleInfoWithLatLong_2015to2019.csv to connect locations with repeated samples.
  - sampleInfoWithLatLong_2015to2019.csv provides survey type, date, location, spatial reference, and contributor information.
  - sampleAttributes_2015to2019.csv supplements samples with categorical attributes (e.g., habitat) via sample_id.
  - occurrences_2015to2019.csv ties species observations to specific samples and records verification status and spatial sensitivity.

- Accessing habitat information (example)
  - Demonstrates joining sampleInfoWithLatLong with sampleAttributes to extract habitat data (e.g., via R or SQL with appropriate joins on id/sample_id and caption = 'NPMS Habitat').

- Evidence Quality Assurance (EQA) and referenced sources
  - EQA framework supported by multiple journal articles, reports, and methodological papers to guide data quality, design, and interpretation.
  - Key publications cited include: Pescott et al. (2019, 2016, 2015), Walker et al. (2015), and related NPMS technical reviews and internal/Defra reports.
  - Purpose of EQA: ensure uncertainty, assumptions, and limitations are communicated; validate biases and design choices; review processes and version control.

- EQA processes and governance
  - Steering Group oversees NPMS work; external peer review is used when risk warrants it (e.g., design issues).
  - Uncertainty and limitations are communicated in outputs (newsletters, reports) and are subject to scientific review.
  - Bias reduction achieved through robust statistical design and modelling to estimate uncertainty.
  - Documentation and version control: all design work is versioned and archived off-site per a CEH Data Management Plan; PRINCE2 project management standards are followed.

- End-to-end use and outputs
  - Data are intended to be publicly available for independent review and reuse.
  - Analyses conducted by experienced ecologists using R scripts; results disseminated via NPMS newsletters and peer-reviewed publications.
  - Outputs include clear communication of uncertainty, habitat indicators, and species-level results, with ongoing opportunities for feedback and refinement of methods.

- Notes on data provenance and guidance
  - Field recording guidance (second edition, 2019) and additional resources for surveyors are available via NPMS website.
  - Data are collected by volunteers with multiple training levels; data input uses standardized dictionaries, date calendars, map-based locations, and controlled habitat terms to minimize errors.