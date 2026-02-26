# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Data from two Amazonian Peru wetland sites in the Pastaza-Marañón Basin: NYO-03 (peatland pole forest) and VEN-02 (palm swamp).
- Aim: estimate and compare litter and root production and decay over a full year to understand carbon accumulation dynamics; includes downcore peat core data for palaeoecology.
- Ten CSV files cover multiple components of ecosystem productivity and palaeoecology, with context datasets extending to other sites for comparison.

## Datasets Included
- CSAP_3.1_Decomposition_bags.csv: litter decomposition rates by material type.
- CSAP_3.2_CWD.csv: coarse woody debris mass along transects (and palm fronds).
- CSAP_3.3_Littertraps.csv: monthly litter trap collections.
- CSAP_3.4_Root_ingrowth_cores.csv: root production via ingrowth cores.
- CSAP_3.5_Dendrometer_bands.csv: short-term tree diameter growth measurements.
- CSAP_3.6_Palm_heights.csv: palm height growth records.
- CSAP_3.7_14C.csv: radiocarbon dates for peat initiation and age models.
- CSAP_3.8_210Pb.csv: Pb-210, Pb-214, Cs-137 activities for peat dating.
- CSAP_3.9_C_N.csv: total carbon and total nitrogen concentrations in peat.
- CSAP_3.10_Pollen.csv: subfossil pollen counts for palaeoecological reconstruction.

## Methods and Collection
- Field sites: NYO-03 and VEN-02; materials installed or collected on surface to various depths as appropriate.
- Litter bags: dried, weighed before/after, with various litter types; multiple replicates per treatment.
- CWD: collected along transects with wet and dry mass measurements; palm components categorized separately.
- Littertraps: 1 x 1 m, 1 mm mesh, ~monthly collections for a year.
- Root ingrowth cores: plastic mesh cores installed, collected every three months; roots dried and weighed.
- Dendrometer bands: spring-loaded bands to measure diameter growth at multiple censuses.
- Palm heights: two census measurements climbing palms, recording canopy heights.
- Radiocarbon dating: 14C samples processed per NEIF standards for peat initiation and downcore modeling.
- Pb-210 dating: 210Pb, 214Pb, and 137Cs activities measured to build age-depth models.
- C and N: carbon and nitrogen concentrations measured on peat cores.
- Pollen: subfossil pollen analysis following established pollen processing and identification references.

## Quality Control
- CSAP_3.1: homogenous litter material; eight replicates where possible.
- CSAP_3.2: standardized field data collection; use of field booking sheets.
- CSAP_3.3: adherence to reference manual; ten replicates per plot; cross-check total mass vs components.
- CSAP_3.4: eight cores per plot; standardized processing.
- CSAP_3.5: disturbed data removed; field data quality checked against field sheets.
- CSAP_3.6: data checked against field sheets; note that VEN-02 2019 census deemed unreliable and excluded (repeated in 2020).
- CSAP_3.7–3.10: standardized lab QA, calibration checks, and reference standards; blanks and standards analyzed with each batch; pollen taxonomy based on published keys and databases.

## Data Structure and Units
- Files are UTF-8 encoded CSVs; variables in columns, samples/objects in rows; NA indicates missing data.
- Common fields across datasets include: Site_code, Core_Code, Depth_cm (where applicable), Date_collected, Collection_month, and metric-specific measurements (e.g., mass_g, Diameter_mm, Height_cm, etc.).
- Examples of representative fields:
  - Decomposition bags: site, litter_type, depth_cm, initial_mass_g, end_mass_g, percentage_remaining, installation_date, replicate, latitude/longitude.
  - Littertraps: site_code, subplot, collection_month, start_date, date_collected, total_mass_g, leaves_g, woody_material_g, etc.
  - Dendrometer bands: site_code, tag_no, initial_diameter_mm, dband_growth_mm, census_date, census_no.
  - 14C and Pb-210: site/core details, depths, conventional ages, isotopic measurements, calibration data.
  - Pollen: core_code, depth_cm, counts by taxa, geographic coordinates.
- Geospatial coordinates provided for sample sites (approx. lat -4.07 to -5.88, lon -73.27 to -74.83).

## Provenance, Context, and Funding
- Project: CSAP-DAD; UKRI-NERC funding (grant NE/R000751/1).
- Principal investigator: Dr Ian Lawson.
- Data collected 2018–2020; methods reference established protocols (RAINFOR, Honorio & Baker, 2010) and NEIF/Geoscience lab procedures.
- Palaeoecological context provided through downcore radiocarbon dating, Pb-210 dating, C/N analyses, and pollen records.

## Access, Reuse, and Documentation
- High level metadata and method details are included to support discovery, reuse, and replication.
- Data are organized by clear dataset-specific schemas with explicit field definitions and units.
- Where applicable, data include notes on reliability (e.g., VEN-02 2019 census exclusion) and data provenance to aid proper interpretation.

## Data Stewardship Considerations and Recommendations
- Ensure consistent metadata mapping across all files to support interoperability and cross-dataset analyses.
- Maintain clear cross-references using Core_Code and Site_code to enable data linking and provenance tracking.
- Preserve and document data processing steps (e.g., drying temperatures, sample preparation, calibration standards) for reproducibility.
- Use controlled vocabularies for categorical fields (e.g., litter_type categories, palm vs. hardwood components).
- Version datasets and provide data quality notes, including exclusions or revisions (e.g., unreliable census data).
- Consider publishing a data dictionary and data lineage that captures laboratory methods, QA procedures, and data transformations.
- Provide licensing and access details for data portals; include contact points for data requests and updates.
- Plan for updates or additions (e.g., future collections, reprocessing) with clear versioning and changelogs.