# Landscape point feature data 1990 [Countryside Survey], Great Britain

## Overview
- Dataset describing landscape point features from 451 1km squares across Great Britain, sampled in 1990.
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Version: 1, dated 04-02-2016.

## Data schema and fields
- SQUARE (text) - 1km square sampling site code
- YEAR (number) - Year of survey
- ID (number) - Landscape point identifier (unique within a year)
- THEME (number) - Theme code
- THEME_NAME (text) - Theme
- PRIMARY_ATTRIBUTE (number) - Primary Attribute code
- PRIMARY_ATTRIBUTE_NAME (text) - Primary Attribute
- SPECIES (number) - Species code
- SPECIES_NAME (text) - Species name
- PROPORTION (number) - Species cover code
- PROPORTION_RANGE (text) - Species cover value
- USE (number) - Use code
- USE_NAME (text) - Structures theme land use
- MODAL_DBH (number) - Modal DBH code
- MODAL_DBH_RANGE (text) - Modal diameter at breast height (DBH)
- LC07 (text) - ITE Land Class 2007
- LC07_NUM (number) - ITE Land Class 2007 code
- COUNTRY (text) - Country (England ENG, Scotland SCO, Wales WAL)
- COUNTY07 (text) - County or Council (as applicable)
- EZ_DESC_07 (text) - Countryside Survey Environmental Zone description (see linked document)

## Provenance, licensing and acknowledgement
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement statement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Copyright: Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved.
- Documented sources and references provided for methodology and classifications.

## Access, use and citation guidance
- Data is provided with code tables (THEME, PRIMARY_ATTRIBUTE, SPECIES, USE, LC07, etc.) alongside descriptive names to support interpretation and reuse.
- Environmental classifications and classifications methods referenced (ITE Land Classification, Biodiversity Broad Habitats) with links to supporting publications.
- Public references include the Countryside Survey website and major methodological papers (e.g., Bunce et al., Jackson 2000).

## Data stewarding considerations
- Ensure metadata includes variable definitions, code mappings (codes to names), sampling design, and year-specific context (1990 snapshot).
- Maintain consistent acknowledgement wording in all outputs (datasets, publications, presentations).
- Track lineage and provenance for each dataset copy; monitor for updated or revised code tables or method notes.
- Facilitate interoperability by aligning with standard land classification and habitat classification references cited in the accompanying publications.
- Be mindful of the year-specific uniqueness of IDs (ID unique within a year; cross-year matching requires careful handling).

## References and resources
- Countryside Survey Website (overview and methodologies)
- Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
- Bunce et al. (2007) ITE Land Classification of Great Britain 2007
- Jackson (2000) Guidance on Biodiversity Broad Habitat Classification
- Related Merlewood and R&D documents (links and DOIs provided in the dataset documentation)