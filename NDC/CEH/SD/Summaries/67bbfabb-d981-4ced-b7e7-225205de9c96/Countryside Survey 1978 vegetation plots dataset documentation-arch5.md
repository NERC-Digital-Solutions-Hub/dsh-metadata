# Countryside Survey 1978: vegetation plot data, Great Britain Dataset Documentation

## Overview
- Documentation for Countryside Survey vegetation data collected in 1978 (and 1977).
- Data consist of two CSV files: one with plot information and one with species lists.
- Dataset applies to Great Britain (England, Scotland, Wales) and uses standardized nomenclature and metadata conventions.

## File structure and key fields
- Vegetation Plot - Plot Information 1978.csv
  - YEAR: Year of survey
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - PLOT_TYPE: Type of plot
  - COUNTRY: ENG, SCO, or WAL
  - ENV_ZONE_2007: Environmental Zone number (2007 version)
  - EZ_DESC_07: Environmental Zone description (2007 version)
- Vegetation Plot - Species List 1978.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - AMALG_PTYPE: Plot type
  - BRC_NUMBER: Species identifier
  - BRC_NAMES: Species name
  - TOTAL_COVER: Percent cover in the whole plot
- Nomenclature: Species names follow Stace, C. (1997) New Flora of the British Isles.

## Taxonomy, metadata, and standards
- Uses Stace (1997) taxonomy for species names.
- Environmental zones referenced via ENV_ZONE_2007 with corresponding description in EZ_DESC_07 (2007 version).
- Plot-level and species-level data captured in separate files to aid data management and reuse.
- Metadata and field references aligned with Field Handbook 1978 for methodological context.

## Data governance, usage rights, and acknowledgments
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data rights and copyright apply to all copies, publications, reports, and presentations.

## Provenance and references
- Data source: Countryside Survey, vegetation species recorded from plots in 1978 (and 1977).
- Primary references and resources include:
  - Countryside Survey Website (general overview and methodologies)
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Countryside Survey: Environmental Zones (metadata and data documentation)
  - Field Handbook 1978 (Grange-over-Sands, UK) and related links
- Related metadata and field-handbooks available via provided links and repositories.

## Data stewardship considerations
- Data quality and consistency:
  - Two-file structure (plot information and species list) supports clear data governance and traceability.
  - Standardized fields for year, location, plot type, country, and environmental zoning enhance interoperability.
- Discoverability and reuse:
  - Clear identifiers (SQUARE_ID, PLOT_ID) facilitate dataset discovery and linkage with other Countryside Survey datasets.
  - Explicit taxonomic standard and metadata references aid cross-study comparability.
- Update and provenance:
  - Versioned Dataset Documentation (Version 1, 28/2/2014) indicates a defined documentation baseline; provenance traces back to 1978 fieldwork with 2007 environmental zone mapping.
- Potential challenges for data stewards:
  - Data reflect historical surveys (1978/1977) and may require careful interpretation for current analyses.
  - Environmental zone mapping (ENV_ZONE_2007) implies a legacy alignment that may need re-evaluation for new analyses or harmonization with newer zoning schemes.
  - Acknowledgement requirements must be consistently applied across all outputs.

## Practical implications for data users
- When using the data, cite Countryside Survey and include the specified acknowledgement text.
- Use BRC_NUMBER and BRC_NAMES for species-level analyses, applying the Stace (1997) nomenclature.
- Reference environmental zone context via ENV_ZONE_2007 and EZ_DESC_07 to interpret ecological context of plots.
- Consult Field Handbook 1978 for methodological specifics and ensure alignment with the versioned dataset documentation.