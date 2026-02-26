# Countryside Survey 1990: vegetation plot data, Great Britain Dataset Documentation

- Overview
  - Dataset comprises two CSV files from Countryside Survey 1990: Vegetation Plot - Plot Information 1990 and Vegetation Plot - Species List 1990.
  - Collected in Great Britain (England, Scotland, Wales) in 1990; documentation version 1, dated 28/02/2014.
  - Data owned by NERC - Centre for Ecology & Hydrology (CEH).

- Data structure and key fields
  - Vegetation Plot - Plot Information 1990.csv
    - YEAR: survey year
    - SQUARE_ID: survey square identifier
    - PLOT_ID: plot identifier
    - PLOT_TYPE: type of plot
    - COUNTRY: ENG/SCO/WAL
    - ENV_ZONE_2007: environmental zone number (2007 version)
    - EZ_DESC_07: environmental zone description (2007 version)
  - Vegetation Plot - Species List 1990.csv
    - YEAR: survey year
    - SQUARE_ID: survey square identifier
    - PLOT_ID: plot identifier
    - AMALG_PTYPE: plot type
    - BRC_NUMBER: species identifier
    - BRC_NAMES: species name
    - NEST_LEVEL: nest species first recorded in
    - FIRST_COVER: percent cover in first nest
    - TOTAL_COVER: percent cover in whole plot
  - Species nomenclature follows Stace, C. (1997) New Flora of the British Isles.

- Provenance and standards
  - Data derived from Countryside Survey projects; references include Barr (1990/1991) Field Handbook for survey methodologies.
  - Environmental zones linked to 2007 metadata version.
  - Cross-references to related publications and portals (Countryside Survey Website; Carey et al. 2008 UK results; environmental zones metadata).

- Licensing, rights, and acknowledgments
  - All use of Countryside Survey data must be acknowledged.
  - Acknowledgement text to be used: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Acknowledgments apply to copies, publications, reports, and presentations.

- Data quality and stewardship considerations
  - Data quality relies on standardization across two linked files (plot information vs. species list) via YEAR, SQUARE_ID, and PLOT_ID.
  - Metadata indicates standard nomenclature and references to established field handbooks and environmental zone classifications.
  - Documentation implies potential need for ongoing metadata alignment if datasets are updated or integrated with other systems.

- Access, sharing, and discovery
  - Dataset is documented for discovery and reuse; data should be uploaded to relevant portals with proper metadata and the required acknowledgement.
  - Considerations for data sharing include maintaining the two-file linkage, consistent plotting identifiers, and version control if updates occur.

- References and related materials
  - Countryside Survey Website (overview and methodologies)
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Countryside Survey Environmental Zones (GB-wide zoning)
  - Barr, C.J. (1991/1990) Countryside Survey Field Handbook
  - Barr et al. (1991) field handbook link and resources

- Data stewardship actions for this dataset
  - Preserve and clearly document the linkage between plot information and species lists (YEAR, SQUARE_ID, PLOT_ID).
  - Maintain versioned metadata, ensuring the 2007 environmental zone references remain consistent with current usage.
  - Enforce the required acknowledgment text in all disseminations.
  - Validate species nomenclature against Stace (1997) reference during any re-annotation or integration.
  - Ensure accessibility through appropriate portals and provide user guidance on dataset structure and fields.