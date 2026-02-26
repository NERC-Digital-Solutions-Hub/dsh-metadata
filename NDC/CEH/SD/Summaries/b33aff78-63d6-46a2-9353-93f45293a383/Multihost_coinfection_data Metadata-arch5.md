# Metadata for: MultihostCoinfectionData.csv

## Overview
- Metadata for a 2018 mesocosm experiment at ZSL exploring how host community composition (toad vs frog vs mixed) and exposure history influence Bd (Batrachochytrium dendrobatidis) and ranavirus infections.
- Demonstrates data collection and preparation steps typical for data stewardship: capturing design, treatments, variables, and outcomes to support discoverability and reuse.

## Experimental design and data scope
- Experimental communities: 3 types based on host composition
  - 100% toads (Bb only)
  - 100% frogs (Rt only)
  - 50/50 mixed community
- Pathogen exposure regimes (four treatments):
  - Control: Phase 1 sham, Phase 2 sham
  - Bd only: Phase 1 Bd exposure, Phase 2 sham
  - RV only: Phase 1 sham, Phase 2 ranavirus exposure
  - Co-infection: Phase 1 Bd exposure, Phase 2 ranavirus exposure
- Two-phase design by pathogen type
  - Phase 1: Bd zoospores vs sham
  - Phase 2: RV-positive corpses vs RV-negative corpses (or sham)
- Experimental structure
  - 12 distinct community x exposure combinations
  - 6 replicates per combination
  - Duration: six weeks

## Data structure and key variables
- tank_ID: unique mesocosm identifier
- individual_ID: unique identifier for each host individual
- species: species of each individual
- community_treatment: host community composition (Bb = toads, Rt = frogs, mixed)
- exposure_treatment: one of the four exposure regimes
- Phase1_dose: Bd exposure status in Phase 1 or control
- Phase2_dose: RV exposure status in Phase 2 or control
- death_date: date of death or euthanisation
- bd_status: Bd infection status at end (0 = uninfected, 1 = infected)
- bd_load: Bd DNA load in genomic equivalents; NA if negative
- Rv_status: ranavirus infection status at end (0 = uninfected, 1 = infected)
- Rv_load: ranavirus DNA load in genomic equivalents; NA if negative
- Coinfection_status: presence of both pathogens at end (0 = negative, 1 = positive)

## Data quality and interpretation notes
- Units: Bd/Rv loads expressed as genomic equivalents.
- NA handling: NA values denote negative test results for the corresponding pathogen.
- Potential metadata inconsistency: Rv_load description appears to reference Bd DNA; check alignment to ensure Rv_load reflects ranavirus DNA measurements.

## Data governance and sharing considerations
- Metadata supports data discovery, reuse, and integration with other datasets by clearly documenting experimental design, treatments, and outcomes.
- Standardized fields enable consistent filtering and analysis across studies (e.g., community_treatment, exposure_treatment, phase doses, and infection outcomes).
- Documentation should be maintained for:
  - Coding schemes (e.g., what constitutes “mixed” vs. single-species treatments)
  - Definitions of Phase1_dose and Phase2_dose
  - Any updates or corrections to the Rv_load descriptor
- Access and provenance: record authors, affiliations, and methodological details to support appropriate data use and citation.

## Particular challenges and considerations for data stewards
- Aligning multiple systems and formats if data are integrated with other datasets.
- Ensuring timely data delivery and updates from data creators, especially if additional cleans or corrections are needed.
- Managing large or complex datasets across many treatments and replicates; maintain clear mapping between tank IDs and treatment conditions.
- Ensuring interoperability of variable naming and coding schemes across related datasets.

## Suggested stewardship actions
- Validate and harmonize variable definitions and units, especially Rv_load terminology.
- Confirm and document the exact coding for community_treatment and exposure_treatment.
- Create and attach a data dictionary or codebook to accompany the CSV metadata.
- Establish a straightforward update protocol if corrections or additions are made to the dataset.
- Provide guidance on interpreting NA values and the coinfection status variable for end users.