# Common Standards Monitoring guidance documents for UK habitats

## Overview
- Describes the dataset that lists species occurring in the Common Standards Monitoring (CSM) guidance documents for UK habitats, linking them to CSM habitat types and National Vegetation Classification (NVC) communities.

## Data collection and quality assurance
- Vascular plants and charophytes data were extracted from JNCC documentation by Dr Kevin Walker.
- Some genera (e.g., Carex spp.) or descriptive terms were replaced with species-based names using the author’s knowledge and UK NVC occurrences.
- Habitat experts validated data during the National Plant Monitoring Scheme (NPMS) development (e.g., Pescott et al. 2019).
- Dr Oli Pescott performed manual checks and matched taxa to the NPMS indicator species; species names were also checked via automated BSBI database look-ups followed by manual verification.

## Data structure and content
- csmIndicatorSpecies.csv
  - Columns include: Species_(Stace_1997) (taxon name from Stace, 1997), CSM_indicator_status (positive/negative for the habitat), NPMS_Indicator (whether used by NPMS as an indicator), CSM_guidance (CSM guidance document source), CSM_habitat (relevant CSM habitat), NVC_communities (relevant NVC communities), NVC_group (NVC group list), CSM_comment (additional notes from guidance).
- csmHabitatsAndRefs.csv
  - Columns include: CSM_guidance_document (name of the guidance document), CSM_habitat_included (habitats within the document), British_NVC_communities_covered (NVC communities covered), CSM_guidance_document_URL (URL to guidance document).
- nameLookup.csv
  - Columns include: Species_(Stace_1997) (Stace name), DDb_matched_name_(full/taxon_name/qualifier/authority) (BSBI automated matches), DDb_accepted_name_(full/taxon_name/qualifier/authority) (currently accepted names per BSBI), taxon_errors/warnings (automated warnings from BSBI).

## Provenance and validation
- Data derived from JNCC guidance documents with subsequent expert review during NPMS development.
- Taxon names reconciled against BSBI database with automated matching and manual verification, ensuring alignment with current accepted names.

## Access, references and supporting materials
- Related resources cited in the dataset:
  - Joint Nature Conservation Committee (JNCC) documentation for common standards monitoring: http://www.jncc.gov.uk
  - National Plant Monitoring Scheme (NPMS): https://www.npms.org.uk
  - Pescott et al. 2019 (manual checks and NPMS indicators): https://doi.org/10.1371/journal.pone.0215891
- CSM indicators are tied to guidance documents and provide URLs in csmHabitatsAndRefs.csv for direct access.