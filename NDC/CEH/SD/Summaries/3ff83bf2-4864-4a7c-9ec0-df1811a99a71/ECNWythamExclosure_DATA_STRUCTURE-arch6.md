# Explanatory Information: Species codes and Quality Codes

- Purpose
  - Provide crosswalks for interpreting coded data in ECN datasets.
  - Help users translate numeric species codes and quality codes into meaningful biological and data-quality information.

- Explanatory Information: Species codes
  - Function: Maps numeric species codes to species names and alternative taxonomic references.
  - Nature of mappings: Each entry lists a code (e.g., 1209, 1210, 1220, etc.) and one or more associated taxon names (often including scientific names, synonyms, or closely related taxa). Some codes appear to map to multiple names across different taxonomic references.
  - Coverage and usage: Used to decode fields that record species presence, abundance, or identity within ECN vegetation datasets. Essential for consistent interpretation across sites and time.
  - Cross-references and notation: The mappings may include multiple layers of references (e.g., Latin names, common names, and alternative codes such as Bry_315, Vas_1046, etc.), indicating crosswalks to other vocabularies or catalogues.
  - Related documentation: The broader dataset documentation (and quality notes) should be consulted for methodological context and to resolve any ambiguities in the mappings.

- Explanatory Information: Quality Codes
  - Function: Defines the numeric quality codes used to describe data reliability and contextual conditions.
  - Range and structure: A broad set of codes, typically grouped by topic (e.g., data collection, laboratory processing, hydrology, weather, site disturbance, and identification confidence).
  - Examples of common codes and meanings:
    - 100: No information available - data lost.
    - 101–121, 122–125, 126–188: Various field and sampling issues (e.g., no sample, partial loss, debris in sample, equipment issues, environmental conditions).
    - 199–241: Additional field/lab or identification quality notes (e.g., unidentified material, low/medium confidence identifications).
    - 501–513: Laboratory-related issues (e.g., no sample in lab, sample discarded, contamination, measurement problems).
    - 999: Unusual event - see the quality text for details.
  - Identification confidence: Codes 238–241 indicate the status of taxon identification and confidence (e.g., stem dead, unidentified, medium confidence, low confidence).
  - Usage guidance: Quality codes should be consulted alongside the corresponding quality text to assess data reliability and to decide whether to include, weight, or exclude records in analysis.
  - Documentation linkage: Quality notes are typically complemented by separate quality text files (e.g., ECN_VF_qtext.csv) that describe each code in more detail. The ECN data documentation also provides broader context for interpreting these quality indicators.