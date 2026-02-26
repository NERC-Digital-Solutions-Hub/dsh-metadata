# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

## Overview
- A long-term field experiment assessing Scots pine phenotypes across multiple sites in Scotland.
- Seed sourced from ten trees per population across 21 native Scottish P. sylvestris populations; seeds collected March 2007 and germinated in 2007.
- Populations chosen to represent Scotland’s native range; three populations from each of seven seed zones.
- Seedlings grown in three nurseries (NW, NG, NE) and transplanted in 2012 to three field sites: Yair (FS, south Scotland), Glensaugh (FE, east Scotland), and Inverewe (FW, west Scotland).
- Experimental design includes randomized blocks, with 168 trees per site (one tree from eight of ten families per 21 populations per block). Guard rows planted around the periphery.
- Data file comprises one dataset: FieldTraits.txt.

## Experimental Design and Data Collection
- Planting and growth:
  - Seeds undergo dormancy-breaking treatments; transplanted into 8 cm x 8 cm x 9 cm pots and later into field sites in 2012.
  - Allocation: FS and FE blocks with four blocks each; FW with three blocks.
  - At each site, blocks contain 1 individual from each of eight of the ten families from each of the 21 populations.
  - Some replacements occurred at FS due to insufficient trees for certain families.
- Measurements and timelines:
  - Height: measured at end of each growing season (FE and FW: 2013–2020; FS: 2014–2020).
  - Basal stem diameter: measured end of each season (FE and FW: 2013–2020; FS: 2020 only).
  - Phenology: spring assessments annually 2015–2019; 2020 assessments not possible due to COVID-19.
- Locations and coordinates:
  - Field sites: Yair (FS), Glensaugh (FE), Inverewe (FW). Each site has defined geographic coordinates.

## Data File and Variables
- File: FieldTraits.txt
- Core structure:
  - PopulationCode, Description
  - Family, Description
  - FieldSite, Description
  - FieldCode (tree-level code; site-specific ranges)
  - Block, Row, Column (randomised block layout and planting position)
- Traits and year-structured variables (example naming):
  - Height: HA13, HA14, ..., HA20 (mm; height after 7th–14th growing seasons depending on year/site)
  - Height increments: HI13, HI14, ..., HI20 (mm; yearly height increase)
  - Base stem diameter: DA13, DA14, ..., DA20 (mm)
  - Diameter increments: DI13, DI14, ..., DI20 (mm)
  - Budburst duration: BD15, BD16, BD17, BD18, BD19 (days; 2015–2019)
  - Budburst timing: BT15_4, BT15_5, BT15_6, BT16_4, BT16_5, BT16_6, BT17_4, BT17_5, BT17_6, BT18_4, BT18_5, BT18_6, BT19_4, BT19_5, BT19_6 (days since 31 March, or days to reach specific budburst stages)
- Metadata specifics:
  - Units provided for key measurements (e.g., Height in mm; BD in days; DA/DI in mm).
  - Some fields are NA where not applicable (e.g., FieldCode not transplanted).
  - FieldCode ranges are site-specific (e.g., Inverewe 5001–5672, 6001–6004, 7001–7672).

## Data Quality, Gaps, and Access
- Data provenance:
  - Clear lineage from seed collection to field planting and yearly phenotypic measurements.
  - Detailed site and block structure supports replication and cross-site comparisons.
- Potential limitations:
  - 2020 phenology data not collected due to COVID-19 restrictions.
  - Some family representations varied by site due to transplantation constraints; nine families were replaced at FS.
  - Data are stored in a single primary file (FieldTraits.txt); future analyses may benefit from additional derived data files or documentation to facilitate interoperability.
- Discoverability and reuse considerations:
  - Rich, year-structured trait naming enables longitudinal analyses across sites.
  - Consistent metadata naming for PopulationCode, Family, FieldSite, and FieldCode supports cross-study integration, but users may need to align year-specific variable naming across sites.

## Use and Implications for Data Leaders
- Use cases:
  - Cross-site comparisons of growth and phenology and their genetic associations (population and family level).
  - Genotype-by-environment analyses and climate adaptation studies.
  - Longitudinal tracking of growth increments and budburst dynamics across years.
- Data governance and stewardship implications:
  - Ensure documentation covers site-specific differences in measurement timing and protocols.
  - Implement data versioning and clear provenance when integrating FieldTraits.txt with other datasets (nursery records, transplantation logs).
  - Consider standardizing phenotype terminology and units for broader interoperability with forestry phenotypic datasets.
- Data strategy considerations:
  - Maintain and expand metadata to capture measurement protocols, observer identifiers, and any site-specific procedures.
  - Provide data access controls and licensing to support broad but governed reuse.

## Key Data Management Considerations for Data Leaders
- Align user needs with the dataset’s capabilities:
  - Support researchers interested in cross-site growth and phenology and those studying genetic structure across populations.
- Address data gaps and standardization:
  - Document any deviations in measurement timing due to site-specific constraints or external factors (e.g., COVID-19).
  - Continue efforts to harmonize units and variable naming across years and sites to enhance comparability.
- Ensure data accessibility and discoverability:
  - Maintain the FieldTraits.txt file with robust metadata and, if possible, provide a machine-readable data dictionary.
  - Consider adding DOIs or persistent identifiers and creating a data cookbook or landing page for easier reuse by data scientists and policy colleagues.