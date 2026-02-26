# Common Standards Monitoring guidance documents for UK habitats

- Purpose and scope
  - Provides lists of species that occur in the Common Standards Monitoring (CSM) guidance documents for UK habitats.
  - Links species to both CSM habitats and National Vegetation Classification (NVC) communities.
  - Supports monitoring of designated nature conservation sites and data discovery.

- Data provenance and collection
  - Data on vascular plants and charophytes extracted from JNCC documentation by Dr Kevin Walker.
  - Taxonomic decisions include replacing certain genera/descriptions with species based on author knowledge and UK NVC occurrences.
  - Habitat experts validated during the National Plant Monitoring Scheme (NPMS) development.
  - Manual checks by Dr Oli Pescott; species names verified via automated BSBI look-ups and subsequent manual checks; results included in the dataset.

- Data structure and schema
  - csmIndicatorSpecies.csv
    - Fields include: Species_(Stace_1997), CSM_indicator_status, NPMS_Indicator, CSM_guidance, CSM_habitat, NVC_communities, NVC_group, CSM_comment.
  - csmHabitatsAndRefs.csv
    - Fields include: CSM_guidance_document, CSM_habitat_included, British_NVC_Communities_covered, CSM_guidance_document_URL.
  - nameLookup.csv
    - Fields include: Species_(Stace_1997), DDb_matched_name_(full/taxon_name/qualifier/authority), DDb_accepted_name_(full/taxon_name/...), taxon_errors/warnings.
  - Relationships: indicator species mapped to CSM habitats and NPMS indicators; taxa cross-checked against BSBI database; names linked to accepted nomenclature.

- Quality control and validation
  - Habitat experts review indicator status and related guidance.
  - Taxon names undergo automated BSBI matching followed by manual verification.
  - Inclusion of CSM-specific comments and caveats to document interpretation and any issues.

- Access, updates, and governance
  - Data aligned with current CSM guidance documents; document-specific URLs provided for traceability.
  - Dataset intended to be updated as CSM guidance documents and nomenclature evolve; provenance and processing steps documented to support governance and reproducibility.

- Considerations for Data Stewards
  - Maintain metadata completeness and consistent naming conventions (e.g., Stace names, BSBI accepted names).
  - Track changes in CSM guidance and taxa nomenclature; ensure dataset remains interoperable with NPMS and NVC classifications.
  - Coordinate updates across multiple data files (indicator species, habitats/refs, and name lookups) to preserve data integrity.

- References and related materials
  - NPMS (National Plant Monitoring Scheme) indicators and methods.
  - BSBI database for automated and manual taxon name verification.
  - JNCC documentation and the 2019 Pescott et al. study cited within the metadata.