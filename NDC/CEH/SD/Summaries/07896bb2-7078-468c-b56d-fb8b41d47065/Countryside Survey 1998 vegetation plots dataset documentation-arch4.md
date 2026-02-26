# Countryside Survey 1998: vegetation plot data, Great Britain Dataset Documentation Version: 1: 28/2/2014 Countryside Survey data © NERC - Centre for Ecology & Hydrology

- Purpose and scope
  - Documentation for Countryside Survey vegetation data collected in 1998 (and 1999) across Great Britain.
  - Data are composed of two CSV files: one with plot information and one with species lists per plot.

- Data files and structure
  - Vegetation Plot - Plot Information 1998.csv
    - YEAR: survey year
    - SQUARE_ID: survey square identifier
    - PLOT_ID: plot identifier
    - PLOT_TYPE: plot type
    - COUNTRY: ENG, SCO, or WAL
    - ENV_ZONE_2007: Environmental Zone number (2007 version)
    - EZ_DESC_07: Environmental Zone description (2007 version)
  - Vegetation Plot - Species List 1998.csv
    - YEAR: survey year
    - SQUARE_ID: survey square identifier
    - PLOT_ID: plot identifier
    - AMALG_PTYPE: plot type (amalgamated)
    - BRC_NUMBER: species identifier
    - BRC_NAMES: species name
    - NEST_LEVEL: nest species first recorded in
    - FIRST_COVER: percent cover in first nest
    - TOTAL_COVER: percent cover in whole plot
  - Nomenclature follows Stace, C. (1997) New flora of the British Isles.

- Provenance and publication context
  - Data owned by NERC - Centre for Ecology & Hydrology; dataset documentation version 1 (2014).
  - Related publications and references include:
    - Countryside Survey website (general project overview and methodologies)
    - Carey et al. (2008) Countryside Survey: UK Results from 2007
    - Countryside Survey Environmental Zones (GB-wide zoning based on environmental characteristics)
    - Barr (1998) Countryside Survey 2000 Field Handbook (3rd Draft)
  - Metadata and additional documentation accessible via the Countryside Survey site and associated metadata links.

- Usage, rights, and attribution
  - All use of Countryside Survey data requires explicit acknowledgement.
  - Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright noted.
  - Data are ©/NERC-Centre for Ecology & Hydrology; all rights reserved.

- Data quality, standards, and discoverability
  - Environmental zones exist, with 2007 version descriptors; users should align analyses to EZ_07 descriptors when applicable.
  - Species nomenclature follows a standard taxonomic reference (Stace, 1997), supporting consistency across analyses.
  - Metadata covers plot-level information and species composition, enabling reproducibility and cross-study comparisons.

- Relevance for data leaders
  - Demonstrates a clear data system: separate metadata (plot information) and content (species list), with linkages via YEAR, SQUARE_ID, and PLOT_ID.
  - Highlights the importance of documenting data provenance, nomenclature standards, and licensing/acknowledgement requirements for data products.
  - Provides guidance for discoverability through external references and metadata portals (Countryside Survey website) and emphasizes the need for consistent metadata (environmental zones, plot types, and species coding).
  - Illustrates common governance considerations: data ownership, rights, and mandatory attribution, which influence data sharing and collaboration across networks.

- Practical considerations for use and integration
  - Ensure correct interpretation of environmental zone codes using the 2007 EZ_DESC_07 details.
  - Align species identifiers (BRC_NUMBER) and names (BRC_NAMES) with the Stace nomenclature for compatibility with other GB flora datasets.
  - Plan for proper attribution in any publications, presentations, or derivative products.
  - Leverage referenced field handbooks and UK results reports to inform methodology and contextual understanding of the dataset.