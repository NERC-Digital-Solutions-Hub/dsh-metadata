# Common Standards Monitoring guidance documents for UK habitats

## Purpose and scope
- Provides lists of species that occur within the Common Standards Monitoring (CSM) guidance for UK habitats.
- Links species to both CSM habitats and National Vegetation Classification (NVC) communities.
- Supports standardized monitoring of designated nature conservation sites and enables cross-time scrutiny of environmental health and policy performance.

## How data were collected and quality controlled
- Data on vascular plants and charophytes extracted from existing JNCC documentation by Dr Kevin Walker.
- Some genera or descriptive qualifiers in JNCC sources were replaced by species-level names based on expert knowledge and NVC occurrences.
- Habitat experts vetted data during the development of the National Plant Monitoring Scheme (NPMS) (e.g., Pescott et al. 2019).
- Dr Oli Pescott performed manual checks and matched taxa to NPMS indicator species; names were verified against the BSBI database (automated look-ups followed by manual checks). Results are included in the deposit.

## Data structure and key content
- csmIndicatorSpecies.csv
  - Links species (Stace 1997 names) to:
    - CSM indicator status for each habitat
    - NPMS indicator status
    - CSM guidance document
    - Relevant CSM habitat
    - Associated NVC communities and groups
    - Any relevant comments from CSM guidance
- csmHabitatsAndRefs.csv
  - Maps CSM guidance documents to:
    - Included CSM habitats
    - Covered British NVC communities
    - URL to the current CSM guidance document
- nameLookup.csv
  - Provides comprehensive name-matching data between Stace 1997 names and BSBI database matches
  - Includes accepted names (full, taxon name, qualifier, authority) and any taxon errors or warnings

## Provenance, references, and access
- Data are grounded in established sources:
  - JNCC Common Standards Monitoring guidance documents
  - National Plant Monitoring Scheme (NPMS) indicators (Pescott et al., 2019)
  - BSBI database name checks (Stace 1997 and later accepted names)
- Related references and resources:
  - NPMS indicator species linkage (Pescott et al. 2019)
  - JNCC and NPMS websites for guidance and indicators

## Relevance for environmental monitoring and policy scrutiny
- Enables standardized interpretation of habitat condition through consistent indicator sets.
- Facilitates comparison across habitats and time by linking indicators to CSM guidance and NVC communities.
- Supports data storage and portal upload workflows, ensuring datasets are accessible for analysis and policy evaluation.

## Challenges and considerations for analysts
- Value enhancement: integrate these indicator datasets with other environmental data to avoid single-use datasets.
- Data accessibility: ensure that underlying data (e.g., raw species lists and name-matching results) remain accessible to users beyond final outputs.