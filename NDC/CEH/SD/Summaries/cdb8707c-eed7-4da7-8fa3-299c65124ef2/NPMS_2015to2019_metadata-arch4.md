# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC.
- Aims to collect data to provide an annual indication of changes in plant abundance and diversity.
- Supports volunteer plant recorders to monitor plants and habitat attributes in small plots selected via a structured methodology across the UK, Isle of Man and Channel Island countrysides.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand why change is occurring (pressures and drivers).
  - Contribute data for the UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring change in plant communities across important habitats.
- This document describes the NPMS dataset as held at CEH Wallingford, the files provided, and the evidence quality assurance (EQA) process used.

## Data products and files (overview)

- locations_2015to2019.csv: Unique location identifiers (location_id) and location_type describing the survey plot type at each location; links to sampling events in other files.
- sampleInfoWithLatLong_2015to2019.csv: Sampling events with id, survey_id (survey type), date_start, location_id, entered_sref and entered_sref_system (spatial reference details), created_on, created_by_id, LATITUDE, LONGITUDE, monad and monadCRS (1 km grid reference details), country; recorder information anonymized to unique IDs.
- sampleAttributes_2015to2019.csv: Additional data collected about samples; links to sample via sample_id; includes caption and text_value describing the attribute (e.g., habitat).
- occurrences_2015to2019.csv: Species occurrences recorded per sampling visit; fields include id, sample_id, taxonconversionkey, preferred_taxon, domin (Domin score), record_status (C = not reviewed, V = verified, R = rejected), sensitivity_precision (blurring of records if sensitive).
- npmsHabitatLookup.csv: Mapping between NPMS broad habitat categories and nested fine-scale habitats.
- dominScores.csv: Lookup between observed Domin scores and a harmonised Domin category; includes midPoint for interpretive purposes.
- The files collectively provide location, sampling events, habitat attributes, species occurrences, and harmonised metadata to support analysis and reporting.

## How the data are structured and how to access habitat information

- Location and sampling linkage:
  - location_id in locations_2015to2019.csv connects to sampling events in sampleInfoWithLatLong_2015to2019.csv.
- Habitat information:
  - Sample attributes include NPMS Habitat information with a caption field; users can join sampleInfoWithLatLong_2015to2019.csv with sampleAttributes_2015to2019.csv on sample_id to extract habitat data.
- Example workflow (illustrative):
  - Read sampleInfoWithLatLong_2015to2019.csv and sampleAttributes_2015to2019.csv
  - Filter sampleAttributes to caption == 'NPMS Habitat'
  - Merge on sample_id to obtain habitat information for each sample
- Access patterns can also be implemented in SQL or other database frameworks using LEFT JOINs between samples and attributes with the appropriate caption filter.

## Evidence Quality Assurance (EQA) in NPMS

- EQA guidance is supported by a body of publications and internal documentation to inform data use and interpretation.
- Key publications include:
  - Pescott et al. 2019, The design, launch and assessment of a new volunteer-based plant monitoring scheme for the United Kingdom (PLoS ONE).
  - Pescott et al. 2016, A comparison of models for interval-censored plant cover data (PeerJPrePrints).
  - Pescott et al. 2015, Ecological monitoring with citizen science (Biological Journal of the Linnean Society).
  - Additional related articles and reports listed to support methodology and interpretation.
- Other documents:
  - Internal and external reports on NPMS design, data use for air pollution inference, Bayesian occupancy/abundance indicators, and cross-scheme considerations.
- QA processes and governance:
  - Data input uses online capture with standardized species dictionaries, calendar dates, map-based locations, controlled terms for habitats, and Domin values; automated geographic range checks.
  - Verification through the iRecord system (BSBI-affiliated botanists) for records requiring higher expertise.
  - Data publishing: NPMS data are publicly available to enable independent review.
  - Analysis performed by experienced ecologists using R; results disseminated via NPMS newsletters and peer-reviewed outputs.
- Uncertainty, biases, and review:
  - Outputs are checked by scientists to ensure claims are evidence-supported.
  - Review conducted by a project Steering Group; external peer review occurs where risk is judged higher.
  - Robust statistical design allows uncertainty to be estimated in models.
  - Document tracking and version control are maintained; design work is archived and backed up off-site under a CEH Data Management Plan (PRINCE2 standard).

## How this data supports data leadership and governance

- End-to-end data system: from field collection by volunteers to processed, harmonised data products suitable for public reporting and indicator work.
- Emphasis on data quality, metadata, discoverability, and updates to support continuity and reuse.
- Clear pathways for collaboration and community involvement: standardised methodologies, habitat definitions, and transparency about uncertainties and limitations.
- Governance structures include a Steering Group, potential external peer reviews, and a commitment to public data publication for independent scrutiny.

## End notes and resources

- Field guidance and additional resources for surveyors are available via NPMS website links and documentation (survey guidance, indicator species lists, ID guides, etc.).
- Example workflow and methodological notes illustrate how NPMS data can be integrated with other data sources for broader biodiversity assessments.