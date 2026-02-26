# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Woodland (VW)

## Overview and aims
- Provides long-term environmental health measures to scrutinise and evaluate policy related to woodland vegetation changes.
- Aims to inform future decision-making through standardized monitoring of woodland vegetation structure and composition.

## Dataset origin, governance, and access
- Originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Owners: ECN programme sponsored by a consortium of UK government departments and agencies (e.g., Defra, Natural England, Environment Agency, and others).
- Data sharing: Users must acknowledge data use and provide one reprint of any publication citing the dataset.
- Protocol and metadata: Access is governed by ECN protocols and accompanying metadata documentation; data provenance and usage transparency are emphasized.

## Protocol, sampling design, and data structure
- Plot designs:
  - Two plot types: coarse-grain vegetation surveys and a nested 10 m x 10 m plot for trees and shrubs (centered on a 2 m x 2 m plot); seedlings, dbh, tree height, and dominance are recorded.
- Revisit schedule:
  - Coarse-grain vegetation protocol repeated every nine years.
  - Diameter at breast height (DbH) measurements every three years.
- Data organization:
  - Core data stored in two Oracle tables per site:
    - D1VW_xxx: Vegetation data (plots, trees, species, diameters, heights, etc.).
    - D2VW_xxx: Plot-related data (plot identifiers, sampling dates, height, dbh, seedling measures, etc.).
  - Key fields include SITECODE, SYEAR, PLOTPID, TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE, etc.
- Metadata and quality: Rich metadata and quality annotations accompany data; guidance on data provenance, transformation, and interpretation is provided.

## Site coverage
- T08: Wytham (1993–2012).
- T09: Alice Holt (1994–2011).
- Sites are identified by codes (e.g., T08, T09) and have site-specific metadata.

## Data quality, metadata, and standardisation
- Metadata: Core metadata are maintained; datasets include quality information and provenance guidance.
- Data quality: Emphasises quality assurance, data cleaning/transformations, and clear presentation of results; data are shared with appropriate governance.
- Species codes mapping:
  - A comprehensive mapping exists between numeric species codes and taxonomic names, including synonyms and cross-references (e.g., multiple entries linking codes to Salix species and related taxa, with corresponding Latin/common names and synonyms).
  - This mapping supports consistent species-level analyses across sites and studies.
- Quality codes:
  - ECN site managers assign standardized quality codes to indicate factors affecting data quality.
  - Codes cover a wide range of issues (e.g., No information available, sample lost, partial loss, equipment issues, environmental disturbances, sampling conditions, laboratory problems).
  - A special code 999 denotes an unusual event requiring separate text description.
  - The code list provides a structured framework for annotating data quality concerns and unusual occurrences.

## How this supports monitoring, evaluation, and policy decisions
- Long-term, site-based indicators of woodland vegetation structure and composition enable trend analysis and policy scrutiny.
- The nested plot design and repeated measurements facilitate assessment of canopy, tree growth, seedling recruitment, and species dynamics over multi-year cycles.
- Standardized protocols, comprehensive metadata, and explicit data governance support transparency, reproducibility, and informed decision-making.
- Data access is managed through the ECN Data Centre with attribution and publication requirements; users should consult metadata and quality documentation for correct interpretation.

## Key takeaways for policy evaluation and decisions
- The ECN VW dataset provides robust, long-term metrics of woodland vegetation suitable for policy analysis and trend monitoring.
- Standardized data collection and rich metadata enhance cross-site comparability and reliability of findings.
- Awareness of data quality codes and the extensive species-code mappings is essential for accurate analysis and interpretation.
- Data governance, provenance, and sharing considerations are integral to responsible use and dissemination of outputs.