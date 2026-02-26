# Landscape linear feature data 1990 [Countryside Survey], Great Britain

## Overview
- Dataset from the Countryside Survey (Great Britain) covering landscape linear features sampled in 1990 across 325 1km squares.
- Data asset credits: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Two main data blocks in the file:
  - Landscape linear features attributes for each feature event within a 1km square.
  - Species composition associated with each landscape linear feature event.

## Dataset structure and key fields
- Landscape linear features (per feature event):
  - SQUARE, YEAR, EVENT_ID (unique per year), LINEAR_ID (unique per year)
  - EVENT_FROM, EVENT_TO (start/end positions along the feature in metres)
  - THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
  - HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE
  - WIDTH, WIDTH_RANGE
  - MODAL_DBH, MODAL_DBH_RANGE
  - CONDITION, CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY, COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Species composition (per feature event):
  - SPECIES (code), SPECIES_NAME, PROPORTION, PROPORTION_RANGE
  - LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07
- Data organization emphasizes unique identifiers within each year and coded attribute fields that may rely on reference lists or metadata for interpretation.

## Data quality, provenance, and governance
- Unique identifiers:
  - LINEAR_ID and EVENT_ID are unique within a given year, enabling tracking of individual features across outputs of the survey.
- Coding and metadata considerations:
  - Many fields use codes with corresponding human-readable ranges or descriptions (e.g., THEME, HEIGHT, WIDTH, CONDITION). Users should reference code definitions and data dictionaries for correct interpretation.
- Data integrity and updates:
  - The dataset reflects conditions and attributes as recorded in 1990; timeliness and relevance may require linking to later surveys (e.g., ITE Land Classification updates) for longitudinal analyses.
- Acknowledgement and rights:
  - All use of Countryside Survey data must acknowledge the data as owned by NERC - Centre for Ecology & Hydrology; explicit acknowledgement language provided in the dataset documentation.

## Access, licensing, and interoperability
- Licensing/rights:
  - Countryside Survey data are © and ©/rights reserved by NERC-CEH; use requires proper acknowledgement.
- Data discoverability and standards:
  - Data references include links to methodology and classification systems (e.g., ITE Land Classification 2007). For interoperability, consider cross-walking LC07 codes and aligning with related environmental zone descriptors.
- Potential access barriers:
  - While not described as paywalled in this document, Data Leaders should be mindful of possible sector-wide barriers (paywalls, data protection) when planning broader access or distribution.

## References and context for data strategy
- Core sources and methodologies:
  - Countryside Survey website and documentation for project overview and methodologies.
  - ITE Land Classification of Great Britain (2007): framework for LC07 codes and interpretations.
  - Related guidance on biodiversity classifications (e.g., JNCC reports) for cross-domain compatibility.
- Key publications and links:
  - Bunce et al. 1996 and 2007 references detailing the Merlewood and GB land classification frameworks.
  - Jackson 2000 guidance on biodiversity broad habitat classifications.
  - doi/link references provided for deeper technical context and data lineage.

## Practical implications for data leadership
- Data discovery and utilization:
  - The dataset provides rich attribute fields for landscape features, enabling detailed analysis of linear features and associated species composition within GB landscapes.
  - Cross-reference with LC07 and EZ_DESC_07 to integrate with broader environmental classifications.
- Governance and stewardship:
  - Maintain clear provenance, versioning, and proper attribution in all outputs.
  - Ensure metadata completeness for accurate interpretation of coded fields (themes, attributes, conditions, management signals).
- Collaboration and standards:
  - Potential to align with wider data networks and communities of practice to address data standardization, discoverability, and reuse across partners.
  - Use in conjunction with updates or complementary surveys to support longitudinal data governance and impact assessment.