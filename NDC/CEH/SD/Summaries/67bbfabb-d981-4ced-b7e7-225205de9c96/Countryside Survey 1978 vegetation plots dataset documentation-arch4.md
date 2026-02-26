# Countryside Survey 1978: vegetation plot data, Great Britain Dataset Documentation Version: 1: 28/2/2014

## Overview
- Dataset originating from the Countryside Survey, owned by NERC - Centre for Ecology & Hydrology (CEH).
- Covers vegetation plots from 1977 and 1978 in Great Britain.
- Consists of two CSV files: one with plot information, one with species lists.
- Column definitions are referenced in Field Handbook 1978.

## Dataset structure
- File 1: Vegetation Plot - Plot Information 1978.csv
- File 2: Vegetation Plot - Species List 1978.csv

## Plot Information file columns
- YEAR (number) - Year of Survey
- SQUARE_ID (text) - Square identifier
- PLOT_ID (text) - Plot identifier
- PLOT_TYPE (text) - Type of plot
- COUNTRY (text) - England (ENG), Scotland (SCO) or Wales (WAL)
- ENV_ZONE_2007 (number) - Environmental Zone number (2007 version)
- EZ_DESC_07 (text) - Environmental Zone description (2007 version)

## Species List file columns
- YEAR (number) - Survey Year
- SQUARE_ID (text) - Survey square identifier
- PLOT_ID (text) - Plot identifier
- AMALG_PTYPE (text) - Plot type
- BRC_NUMBER (number) - Species identifier
- BRC_NAMES (text) - Species name
- TOTAL_COVER (number) - Percent cover in whole plot

## Nomenclature
- Species names follow Stace, C. (1997). New flora of the British Isles.

## Usage and rights
- All Countryside Survey data must be acknowledged.
- Required acknowledgement and copyright notice for all copies, publications, reports, and presentations:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Access, references, and metadata
- Countryside Survey Website: General overview and links to relevant documents and methodologies.
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- Carey et al. (2008): Countryside Survey: UK Results from 2007 (background to dataset and project)
- Carey et al. (2008): Countryside Survey: UK Results from 2007 (alternative listing)
- Countryside Survey Environmental Zones: Metadata and zone descriptions
  - Metadata view: http://eidchub.ceh.ac.uk/metadata/0cfd454a-d035-416c-80dc-803c65470ea2/data_documentation_envzones/view
- Field Handbook 1978: Field survey handbook
  - Handbook view: http://eidchub.ceh.ac.uk/metadata/67bbfabb-d981-4ced-b7e7-225205de9c96/field-handbook-1978/view

## Metadata considerations for data leaders
- Data is organized by plots across Great Britain with environmental zoning context (2007 version).
- Clear separation between plot metadata and species abundance data enhances discoverability and reuse.
- Nomenclature standardization (Stace, 1997) supports interoperability with other British flora datasets.
- Historical nature of dataset (1977–1978) may influence granularity and updates; plan for provenance tracking and proper attribution.