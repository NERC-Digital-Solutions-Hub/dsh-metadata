# Common Standards Monitoring guidance documents for UK habitats

## Overview
- Provides lists of species that occur in Common Standards Monitoring (CSM) habitat guidance documents and links them to CSM habitats and National Vegetation Classification (NVC) communities.
- Used to support monitoring of designated nature conservation sites in the UK.

## Data provenance and collection methods
- Data on vascular plants and charophytes were extracted from existing Joint Nature Conservation Committee (JNCC) documentation by Dr Kevin Walker.
- Some genera or descriptive qualifiers from JNCC documents were replaced with species names based on the author’s knowledge and UK NVC occurrences.
- Habitat experts validated these changes during the development of the National Plant Monitoring Scheme (NPMS) (see Pescott et al. 2019).
- Dr Oli Pescott performed manual checks and matched taxa to NPMS indicator species; names were further checked via automated BSBI database lookups and manual verification.
- All results are included in the deposit to support interpretation and reuse.

## Data structure and key fields
- csmIndicatorSpecies.csv
  - Species_(Stace_1997): Taxon name as per Stace (1997)
  - CSM_indicator_status: Positive/negative status for the species in the relevant CSM habitat
  - NPMS_Indicator: Whether the species is used as an NPMS indicator
  - CSM_guidance: Source CSM guidance document
  - CSM_habitat: Relevant CSM habitat
  - NVC_communities: Relevant NVC communities for the habitat
  - NVC_group: NVC groupings for the communities
  - CSM_comment: Additional notes from the guidance regarding the species as an indicator
- csmHabitatsAndRefs.csv
  - CSM_guidance_document: Name of the CSM guidance document
  - CSM_habitat_included: List of CSM habitats covered
  - British_NVC_vegetation_Communities_covered: NVC communities covered within the document
  - CSM_guidance_document_URL: URL to the current version of the guidance document
- nameLookup.csv
  - Species_(Stace_1997): Taxon name from Stace (1997)
  - DDb_matched_name_(full/taxon_name/qualifier/authority): Automated BSBI name matches
  - DDb_accepted_name_(full/taxon_name/qualifier/authority): Currently accepted BSBI name
  - taxon_errors/warnings: Automatically generated warnings from BSBI matching

## Data quality and validation
- Taxon identifications subjected to expert checks (habitat experts; cross-validation with NPMS indicators).
- Names verified through automated BSBI lookups followed by manual verification to ensure alignment with accepted nomenclature.
- The dataset includes metadata and explicit linkage to source guidance documents, facilitating traceability and auditability.

## Linkages and usage
- Connects CSM guidance documents to specific habitats and to NPMS indicator species, enabling integrated monitoring and reporting.
- Maps CSM habitats to corresponding NVC communities, supporting consistency across monitoring frameworks.
- Provides provenance and versioned references (Stace taxonomy, BSBI nomenclature) to aid researchers and policymakers in interpreting indicator lists.

## Access, references, and documentation
- Primary source materials include:
  - JNCC guidance documents (CSM)
  - National Plant Monitoring Scheme (NPMS)
  - Stace, 1997 taxonomic reference
  - BSBI taxonomic database
  - Pescott et al. 2019 (NPMS methodology and validation)
- Related online resources:
  - JNCC: Common Standards Monitoring guidance for UK habitats
  - NPMS: National Plant Monitoring Scheme

## Considerations for authors of Monitoring Frameworks
- Ensuring clear provenance and transparent data transformations when adapting classification descriptors (e.g., replacing genera with species).
- Incorporating expert validation steps to align indicators with current monitoring schemes (e.g., NPMS) and vegetation classifications (NVC).
- Balancing taxonomic precision with usability by documenting any nomenclatural changes and accompanying rationale.
- Providing robust metadata and data governance information to facilitate data sharing while maintaining data quality and traceability.