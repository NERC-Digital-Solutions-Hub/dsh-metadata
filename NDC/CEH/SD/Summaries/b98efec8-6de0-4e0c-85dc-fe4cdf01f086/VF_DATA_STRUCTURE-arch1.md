# Explanatory Information: Species codes

## Overview
- The ECN dataset uses numeric species codes to represent taxa and provides extensive mappings to scientific names and cross-references to other taxonomic concepts.
- The coding framework is designed to support data analysis, reporting, and interoperability across datasets, aligning with ECN’s taxonomy approach (VESPAN-based) and cross-references to related concepts (e.g., BRC codes).
- Each code may have multiple variants, capturing different representations or statuses of the same taxon (e.g., 1319, 1; 1319, 2; 1319, 3).
- The mappings include both Latin names and common equivalents, with cross-references such as Vas_xxx to facilitate integration with other taxonomic resources.
- The dataset covers a wide range of taxa (examples shown include Rumex obtusifolius, Salix species, Sorbus aucuparia, and many others).

## Species code mappings (highlights)
- For a given code, several variants may exist to represent different taxonomic concepts or data sources. Examples:
  - 1319, 1 = Taxus baccata (c); 1319, 2 = Vas_2039; 1319, 3 = Taxus baccata.
  - 1148, 1 = Rumex sanguineus; 1148, 2 = Vas_… (multiple cross-references)…
- The mappings explicitly link numeric codes to:
  - Scientific names (e.g., Taxus baccata, Rumex obtusifolius, Salix spp., Sorbus aucuparia).
  - Cross-referenced identifiers (e.g., Vas_####) to other taxonomy systems.
  - Synonyms and related taxonomic concepts (e.g., subspecies, hybrids, or synonymous taxa).
- Example taxa groups represented in the mapping include a broad suite of vascular plants and trees, such as Rumex, Salix, Sorbus, and many others, illustrating the depth of taxonomic coverage.

## Notes on terminology and cross-references
- Vas_xxx entries indicate cross-references to alternative taxonomic concepts or external data centers, enabling integrated analyses across datasets.
- Some lines show multiple representations for the same taxon under a single code, underscoring the need to choose the appropriate variant for a given analysis or data integration task.
- The mappings also incorporate synonyms and closely related taxa to support flexible data harmonization.

## How to use
- Use the numeric species codes to quickly tag observations, then translate to scientific names via these mappings for reporting, modeling, or cross-dataset analyses.
- When combining datasets, leverage Vas_ cross-references to align taxonomy across sources.
- Be mindful of multiple variants per code; select the variant that matches your analysis context (e.g., canonical name vs. cross-reference ID).



# Explanatory Information: Quality Codes

## Overview
- The ECN dataset attaches quality codes to measurements to flag data quality issues encountered during sampling, handling, and laboratory processing.
- Quality codes are grouped by numeric ranges (e.g., 100–199, 200–299, 500s, 999) and are accompanied by descriptive text.
- A special code 999 denotes an unusual event, with details provided in a separate quality text resource (ECN_VF_qtext.csv).

## Key quality codes and meanings (highlights)
- 100, 101, 102, 103, 104, etc.: Various data issues such as no information, no sample taken, partial loss of sample, sample freezing, or debris in sample.
- 110–115, 118–139, 141–160, 170–183, 185–187, 189–191: Codes describing sample contamination, handling problems, equipment issues, environmental disturbances, and other in-field or sampling-process problems.
- 200–206, 210–216, 221–228: Weather-related or biological factors affecting sampling/recording, preserved material issues, or unusual field conditions.
- 501–508, 509–513: Laboratory-related notes such as no sample in lab, sample loss, contamination, or methodological concerns within the lab processing.
- 999: Unusual event (description provided in the quality text file).

## Usage notes
- Quality codes accompany data values to indicate reliability, traceability, and potential biases.
- The “quality text” (for 999) is stored separately and linked via ECN_VF_qtext.csv, enabling detailed contextual descriptions of unusual events.
- Proper QA workflows should filter or flag data points based on quality codes, and researchers should reference the accompanying metadata to interpret any limitations.

## Relationship to dataset and metadata
- These quality indicators are integral to data quality assurance, enabling analysts to assess data suitability for analysis, reporting, and modeling.
- The codes are designed to be used in conjunction with the dataset’s site and plot metadata to diagnose where issues occurred and how they might affect results.