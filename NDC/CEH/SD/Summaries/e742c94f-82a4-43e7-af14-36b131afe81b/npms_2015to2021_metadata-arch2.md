# The National Plant Monitoring Scheme (NPMS) – Data Files and Evidence Quality Assurance

- The NPMS is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC to provide an annual indication of changes in plant abundance and diversity.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand why change is occurring (pressures and drivers).
  - Contribute data for the UK Biodiversity Indicator C7 (Plants of the wider countryside) by measuring change across key habitats.
- Scope: Volunteered plant recorders monitor plants and habitat attributes in a structured set of plots across the UK, Isle of Man, and Channel Islands.
- Data purpose: The attached dataset provides a snapshot of the current NPMS database (as held at UKCEH Wallingford) and describes the files and the Evidence Quality Assurance (EQA) process.

## Overview of files provided

- locations_2015to2021.csv (169 kb)
  - Provides a unique location_id and location_type describing the survey plot type (square or linear) related to habitat type.
- sampleInfoWithLatLong_2015to2021.csv (2,857 kb)
  - Contains sampling events with fields including id (sample), survey_id, date_start, location_id, entered_sref, lat/long, monad, country, created_on, created_by_id.
- sampleAttributes_2015to2021.csv (8,667 kb)
  - Additional data about samples linked by sample_id; includes caption and text_value describing attribute categories (e.g., habitat).
- occurrences_2015to2021.csv (13,464 kb)
  - Records species occurrences with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status, sensitivity_precision; includes verification status and any spatial blurring flags.
- npmsHabitatLookup.csv (2 kb)
  - Maps NPMS broad habitats to fine-scale habitats.
- dominScores.csv (1 kb)
  - Provides a harmonised Domin category (dominIndex) and midPoints for cover-abundance interpretation.

- Example guidance (how to access habitat information):
  - Demonstrates joining sampleInfoWithLatLong_2015to2021.csv with sampleAttributes_2015to2021.csv on sample_id to extract NPMS Habitat data; can be implemented in R or SQL with a LEFT JOIN.

## Data structure and key concepts

- location_id links to sampleInfoWithLatLong_2015to2021.csv to connect locations to sampling events.
- survey_id identifies NPMS survey types (e.g., Wildflower, Inventory, Indicator).
- Spatial referencing: entered_sref and entered_sref_system specify coordinate systems (OSGB, OSIE, 4326); monad and monadCRS define 1 km grid locations and their CRS.
- Habitat and attribute data: sampleAttributes includes descriptive categories (caption) and values (text_value) for each sample.
- Occurrences: taxon information (taxonversionkey and preferred_taxon) with Domin scores and verification status; sensitivity_precision flags sensitive data if applicable.
- Data harmonisation: npmsHabitatLookup and dominScores enable consistent interpretation across different survey forms.

## Evidence Quality Assurance (EQA) for NPMS

- Publications underpinning EQA are provided (journal articles, reports) and recommended for users alongside NPMS guidance.
  - Examples include design and evaluation of the volunteer-based monitoring scheme and methodological comparisons.
- EQA components and processes:
  - Sample design and survey approach: Regular grid of square plots and gridlines for linear plots, developed with statistical and botanical input; habitat definitions reviewed by habitat experts.
  - Target species: Indicator species selected through objective methods and project team review to balance representativeness and volunteer feasibility.
  - Field recording: Volunteer-based with multiple participation levels; training and guidance provided; formal QA of field recording is under consideration for future.
  - Data input/verification: Online data capture with structured spatial database; species dictionary, date calendars, map-based location entries, and controlled terms; automated geographic checks; iRecord-backed verification by botanical experts for higher-level records.
  - Data publishing: Data will be publicly accessible to enable independent scrutiny.
  - Analysis: Conducted by experienced quantitative ecologists using R scripts.
  - Reporting: Delivered by a team with botany, statistics, and science communication expertise; disseminated through NPMS newsletters and peer-reviewed publications.
- Governance and review:
  - Managed by a project Steering Group; external peer review engaged as needed based on risk (e.g., survey design workshops).
- Uncertainty, limitations, and transparency:
  - Outputs are reviewed to ensure claims are supported by evidence; uncertainty is acknowledged and can be estimated through modelling.
  - Bias mitigation through robust statistical design.
- Documentation and version control:
  - Design outputs are archived with version control; data management plan (PRINCE2-based) governs backup and off-site storage.
  - All design stages are documented and versioned.

## Application and use of NPMS data

- The annually updated NPMS dataset supports monitoring of habitat quality and plant community changes, contributing to policy-relevant indicators and scientific analyses.
- Data are stored in the UKCEH NPMS database and are intended for public access to enable independent review and reuse by researchers, policy-makers, and the public.

## Practical notes for analysts

- Neatly structured data with clear links across locations, samples, and occurrences enable time-series analyses of habitat change and plant communities.
- Standardised formats (domin, monad, coordinates, and taxon keys) facilitate cross-study integration and comparison.
- When using the data, refer to the NPMS survey guidance and EQA publications for methodological context and quality considerations.