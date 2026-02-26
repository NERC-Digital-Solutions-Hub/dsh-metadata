# Glastir Monitoring and Evaluation Programme (GMEP) Landscape and Habitat Area Features 2013-2016

## Overview and aims
- Wales-wide monitoring of the Glastir agri-environment scheme to track environmental effects, with a focus on biodiversity and woodland creation/management.
- Data contribute to evidence for reversing native biodiversity decline and meeting obligations under the Convention on Biological Diversity 2020.
- Provides independent estimates of semi-natural land change, linked to Well-Being of Future Generations Act 2015 indicators (Area of Healthy Ecosystems in Wales).

## Survey design and scope
- 4-year rolling survey cycle (2013–2016) to maximise site coverage while enabling year-on-year trend detection.
- Two components:
  - Wider Wales Component: baseline estimation, national trends, national reporting.
  - Targeted Component: links specifically to Glastir priority areas.
- Common spatial unit: 1 km square.
- Sample: 300 squares over the cycle; half randomly sampled from strata defined by the ITE Land Classification of Great Britain, the other half targeted at Glastir priorities.
- Exclusions: squares with >75% urban land or >90% sea (based on LCM2007 and census data).
- Spatial framework allows integration with previous surveys (e.g., Countryside Survey of GB).

## Data collection methods and features captured
- Within each 1 km square, areal, line, and point features are mapped on base maps using pre-defined codes.
- Data collection tools: electronic data capture with CS Surveyor software (CEH/Esri UK).
- Recorded information includes:
  - Biodiversity Broad/Priority Habitats (as per Jackson 2000; Maddock 2008).
  - Land use and management, vegetation species, and a wide range of descriptors (e.g., road verge widths, canopy/tree metrics, woodland structure, sward descriptions).
- Detailed methodologies documented in GMEP Field Mapping Handbooks (Maskell et al., 2016a, 2016b).
- Nomenclature and coding conventions follow established references (e.g., Stace 1997 for species).

## Data files and key variables
- Two primary CSV data files for 2013–2016:
  - GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURES_2013_16.csv
    - Core areas of Broad and Priority Habitats across the 300 squares.
    - Key columns include SQ_ID (1 km square code), POLY_ID (polygon ID), BHCODE/BHDESC (habitat codes and descriptions), AREA (polygon area), and coordinate/year fields (EASTING_10km, NORTHING_10km, YEAR, LC).
  - GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURE_ATT_2013_16.csv
    - Additional attributes for the same areas (linked via POLY_GUID).
    - Contains fields for theme, habitat name, mosaic-area proportion, primary qualifiers, and vegetation specifics (SPECIES, SPECIES_COVER, SWARD_COVER, SWARD_HEIGHT, etc.), plus LAND CLASS (LC) and YEAR.
- Data are complemented by field handbooks that define codes and categories; detailed definitions are provided within the handbooks (Maskell et al., 2016a,b).
- Species nomenclature follows Stace (1997).

## Quality assurance and data integrity
- Surveys conducted by experienced botanical teams; extensive pre-survey training ensures consistency.
- Electronic data capture reduces transcription errors; mandatory fields and prompts improve data completeness.
- Post-survey QC: a second team repeats surveys in whole or part of a square; findings fed back to improve recording.
- Data are promptly checked after collection to maintain data quality.

## Documentation, references, and accessibility
- Methodology and data quality are described in:
  - Field handbooks: Maskell et al. (2016a, 2016b).
  - Annual and final reports: Emmett et al. (2014, 2017) for the GMEP programme.
  - Glastir Monitoring & Evaluation Programme website: gmep.wales.
  - Supporting classifications and habitat descriptions (Bunce et al. 2007; Jackson 2000; Maddock 2008; Stace 1997).
- The document provides extensive references and links to datasets, including NERC CEH and related publications.

## Roles, responsibilities, and field teams
- Appendix 1 lists project roles (e.g., GMEP Lead Scientist, field team managers, data/database managers, GIS/IT support, vegetation experts) and assigns responsibilities.
- Field survey teams comprise numerous named individuals across roles, reflecting collaborative field data collection and management.

## Additional notes
- Figure 1 (distribution of 1 km squares) is provided for confidentiality (plotted at 10 km resolution).
- Data collection scales and integration considerations emphasize cross-study compatibility and future analyses with GB-wide surveys.
- The project emphasizes sharing discoverable datasets with metadata to support reuse and transparency.