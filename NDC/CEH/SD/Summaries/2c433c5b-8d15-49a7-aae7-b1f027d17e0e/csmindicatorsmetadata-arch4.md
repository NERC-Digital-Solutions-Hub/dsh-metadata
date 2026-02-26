# Common Standards Monitoring guidance documents for UK habitats

## Purpose and scope
- Provides lists of species that occur in the Common Standards Monitoring (CSM) guidance documents.
- Links species to both CSM habitats and National Vegetation Classification (NVC) communities.
- Supports monitoring of designated nature conservation sites through standardized indicators.

## Data collection and quality control
- Species data on vascular plants and charophytes were extracted from JNCC documentation by Dr Kevin Walker.
- Some genera or descriptive terms from JNCC documents were replaced with species-level data based on expert knowledge and NVC occurrences.
- Habitat experts reviewed these data during the development of the National Plant Monitoring Scheme (NPMS).
- Manual checks and NPMS indicator alignment performed by Dr Oli Pescott, including automated and manual verification against the BSBI database.
- Species names were validated via automated look-ups to the BSBI (Botanical Society of Britain and Ireland) database, followed by manual verification; results are included in the dataset deposit.

## Data structure and key fields
- csmIndicatorSpecies.csv
  - Species_(Stace_1997): Taxon name per Stace (1997) reference.
  - CSM_indicator_status: Positive/negative status for the habitat.
  - NPMS_Indicator: Whether the species is used as an NPMS indicator.
  - CSM_guidance: Originating CSM guidance document.
  - CSM_habitat: Relevant CSM habitat.
  - NVC_communities: Relevant NVC communities for the habitat.
  - NVC_group: NVC group list for the communities.
  - CSM_comment: Additional comments from guidance.
- csmHabitatsAndRefs.csv
  - CSM_guidance_document: Name of the CSM guidance document.
  - CSM_habitat_included: List of CSM habitats within the document.
  - British_NVC_communities_covered: NVC communities contained in the document’s habitats.
  - CSM_guidance_document_URL: URL to the current version of the guidance document.
- nameLookup.csv
  - Species_(Stace_1997): Taxon name reference.
  - DDb_matched_name_(full/taxon_name/qualifier/authority): Automated BSBI name matches (full, taxon name only, qualifier only, authority only).
  - DDb_accepted_name_(full/taxon_name/qualifier/authority): Currently accepted BSBI name (as of publication time).
  - taxon_errors/warnings: Automated warnings from BSBI matching.

## Provenance, validation, and quality assurance
- Traceable lineage from JNCC guidance to NPMS indicators and BSBI name validation.
- Multi-step verification: expert habitat review, NPMS alignment, automated and manual BSBI name checks.
- Documentation of name changes and potential mismatches through the nameLookup relationships and error/warning fields.

## Access, discoverability, and reuse
- Data are linked to specific CSM guidance documents and BSBI/NPMS references.
- Includes direct URLs to current guidance documents for transparency and reproducibility.
- Structured to support integration with other data systems that require standardized species indicators, habitats, and NVC associations.

## Implications for Data Leaders
- Demonstrates end-to-end data governance: collection from authoritative sources, expert validation, standardized naming and reconciliation with taxonomic databases, and metadata-rich outputs.
- Supports scalable data stewardship across networks by aligning species indicators with habitats and communities, enabling co-ownership of data products and governance.
- Highlights the importance of metadata completeness (e.g., provenance, guidance source, habitat mappings, and URL links) to improve discoverability and trust.
- Addresses common data challenges: data provenance, taxonomy harmonization, quality assurance, and maintainability through clear data structures and references.