# Description

- The Common Standards Monitoring (CSM) guidance documents for UK habitats are used to implement monitoring of designated nature conservation sites. This dataset provides lists of species that occur in those documents, linked to both CSM habitats and National Vegetation Classification (NVC) communities.

## Overview

- Focuses on vascular plants and charophytes extracted from JNCC documentation.
- Species are connected to CSM habitats and the corresponding NVC communities, enabling cross-walks between guidance and classification schemes.

## Collection, generation, and quality control

- Data on plants were extracted from JNCC documents by Dr Kevin Walker.
- Some genera (e.g., Carex spp.) or descriptive qualifiers were replaced by species-level identifications based on the author’s knowledge and UK NVC occurrences.
- Habitat experts reviewed these modifications during the development of the National Plant Monitoring Scheme (NPMS) (references: Pescott et al. 2019).
- Dr Oli Pescott performed manual checks and matched taxa to NPMS indicator species; names were validated via automated BSBI database look-ups followed by manual verification; results are included in this deposit.

## Data structure (files and key fields)

- csmIndicatorSpecies.csv
  - Species_(Stace_1997): taxon name (Stace 1997)
  - CSM_indicator_status: positive/negative status for the species within the CSM habitat
  - NPMS_Indicator: whether the species is used as an NPMS indicator
  - CSM_guidance: source CSM guidance document
  - CSM_habitat: relevant CSM habitat
  - NVC_communities: relevant NVC communities for the CSM habitat
  - NVC_group: NVC group list for the communities
  - CSM_comment: any notes from the CSM guidance about the indicator

- csmHabitatsAndRefs.csv
  - CSM_guidance_document: name of the CSM guidance document
  - CSM_habitat_included: list of CSM habitats included in the document
  - British_NVC_communities_covered: NVC communities covered by the document
  - CSM_guidance_document_URL: link to the current guidance document

- nameLookup.csv
  - Species_(Stace_1997): Stace taxon name
  - DDb_matched_name_(full/taxon_name/qualifier/authority): automated BSBI name matches (full, taxon, qualifier, authority)
  - DDb_accepted_name_(full/taxon_name/qualifier/authority): currently accepted BSBI name
  - taxon_errors/warnings: automated BSBI match warnings or issues

## Data provenance and references

- Source: JNCC (Common Standards Monitoring) guidance documents.
- Data contributors: Dr Kevin Walker (data extraction), Dr Oli Pescott (manual checks and NPMS alignment).
- Validation: expert checks during NPMS development; automated and manual name verification against the BSBI database.
- Related references: NPMS (Pescott et al. 2019) and BSBI database name checks; guidance documents linked to CSM and NVC classifications.

## How to use this dataset

- Link species occurrences to specific CSM habitats and corresponding NVC communities for monitoring analyses.
- Use validated taxonomic names and accepted BSBI names to ensure consistent species matching across datasets.
- Integrate with NPMS indicators to assess monitoring coverage and target species.
- Leverage the document URLs to access the original CSM guidance for context and methodology.

## Considerations for analysts

- Taxonomic updates: names may have changed; rely on DDb_accepted_name fields for current nomenclature.
- Data harmonisation: authors replaced some higher taxa/descriptions with species-level records; consider this when aggregating at genus level.
- Coverage and scope: dataset focuses on species indicators drawn from CSM guidance; local-scale data or other taxa may be outside scope.