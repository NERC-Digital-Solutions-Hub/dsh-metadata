# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Dataset of ecosystem productivity measurements from two main plots in the Pastaza-Marañón Basin, Peru: NYO-03 (peatland pole forest) and VEN-02 (palm swamp).
- Aim: estimate and compare litter and root production and decay across a full annual cycle to understand carbon accumulation dynamics in peat; includes context rows from additional sites and downcore peat core data for palaeoecology.
- Timeframe: field measurements collected during 2018–2020; supplementary downcore data extend palaeoecological interpretation.

## Data Files
The dataset comprises ten CSV files (UTF-8, comma-separated) with standardized site and measurement fields:
- CSAP_3.1_Decomposition_bags.csv: litter decomposition rates for palm and hardwood materials across depths and subplots.
- CSAP_3.2_CWD.csv: coarse woody debris (CWD) data, including palm fronds, along four transects per site.
- CSAP_3.3_Littertraps.csv: monthly litter trap collections (1 m x 1 m, 1 mm mesh) across ten subplots per plot.
- CSAP_3.4_Root_ingrowth_cores.csv: eight root ingrowth cores per plot, collected every three months.
- CSAP_3.5_Dendrometer_bands.csv: dendrometer band growth measurements on selected trees (notches and census records).
- CSAP_3.6_Palm_heights.csv: palm height measurements from two censuses (climb-based).
- CSAP_3.7_14C.csv: radiocarbon dating data (70 dates across cores) for peat age modeling.
- CSAP_3.8_210Pb.csv: Pb-210, Pb-214, and Cs-137 activities for top peat core sections for age-depth modeling.
- CSAP_3.9_C_N.csv: total carbon and nitrogen concentrations in peat samples.
- CSAP_3.10_Pollen.csv: subfossil pollen counts from selected peat cores for vegetation history.

Common structure across files:
- Site_code (NYO_03 or VEN_02), plot/subplot/designation, dates (start/collection census), depths (cm), masses (g), diameters (mm), heights (cm), and location coordinates (decimal degrees).
- Several files contain multiple replicates; some measurements follow established protocols (RAINFOR-derived methods for CWD; Honorio & Baker carbon cycle monitoring protocols).

## Methods and Site Details
- Sites and plots:
  - NYO-03: Nueva York, peatland pole forest.
  - VEN-02: Veinte de Enero, palm swamp.
- Collection and measurement approaches:
  - Litter decomposition bags: placed at or near surface, sometimes at depth; dried and weighed to determine mass loss.
  - Coarse woody debris (CWD): transects along plot margins; field weighing with subsamples dried to estimate dry mass.
  - Littertraps: monthly collections for 12 months; components separated and weighed.
  - Root ingrowth cores: eight cores per plot; peat-filled; collected every three months; roots hand-picked, dried, weighed.
  - Dendrometer bands: installed in 2018; growth tracked via notch movement; some data lost to disturbance; notches recorded.
  - Palm heights: two census dates; palms climbed for trunk height measurements and canopy leaf base distances.
  - Radiocarbon dating (14C): 70 dates; used to model peat initiation age and downcore ages; NEIF/SUERC pre-treatment and AMS dating.
  - Lead-210 (210Pb) dating: top 39 cm of peat cores; gamma spectroscopy for age-depth modeling; includes 214Pb and Cs-137 as context.
  - Carbon and nitrogen (C & N): dry- masses and elemental analysis to obtain C and N concentrations.
  - Pollen: subfossil pollen counts from peat cores; methods aligned with established pollen preparation and analysis protocols.
- Quality control/validation:
  - Replication: multiple replicates per treatment (e.g., eight replicates for some measurements).
  - Field data handling: standardized field booking sheets; experienced fieldworkers.
  - Method alignment: adherence to established protocols (RAINFOR, Honorio & Baker).
  - Data reliability notes: VEN-02 2019 palm census deemed unreliable and omitted; some dendrometer data removed due to disturbance; overall emphasis on data validation and traceability.

## Data Structure and Units
- Data are organized as CSV files with:
  - UTF-8 encoding; variables in columns; observations in rows; missing data as NA.
  - Common descriptive fields include Site_code, Collection_date, Depth_cm, Mass_g (or related mass fields), Diameter_mm, Height_cm, Subplot, Replicate, Census_no, and coordinates (Latitude, Longitude).
- Example data elements:
  - Decomposition bags: initial and end masses (Initial_sample_mass_g, End_mass_g_contents_only), Depth_cm, Time_period (months), Percentage_remaining.
  - CWD: Fresh_mass_g, Subsample_dry_mass_g, Diameter_class, Category, Transect, Subsample_Volume.
  - Littertraps: Total_mass_g, Leaves_g, Woody_material_g, Reproductive_parts_g, Miscellaneous_g.
  - Root ingrowth cores: Core_number, Collection_month, Root_mass_g.
  - Dendrometer bands: Initial_diameter_mm, Dband_growth_mm, Census_date, Census_no.
  - Palm heights: Height_ground_to_canopy_cm, Height_canopy_to_leaf_base_cm, Total_height_cm.
  - 14C: Conventional_14C_age_BP, Carbon_content_pc, d13CVPDB_pmille.
  - 210Pb: Pb210A_activity_Bq_kg, Pb214_activity_Bq_kg, Cs137_activity_Bq_kg, Bulk density.
  - C/N: C_pc, N_pc.
  - Pollen: taxon counts by depth (Depth_cm, Core_Code, Taxa columns).

## Quality Control and Documentation
- Quality checks include:
  - Data cross-checks against field sheets and standard templates.
  - Replicate checks and mass balance consistency where applicable.
  - Exclusion of unreliable census data and removal of disturbed measurements.
  - Documentation of lab methodologies, calibration procedures, and standards used (e.g., reference standards for elemental analysis and gamma spectroscopy).
- Documentation notes provide provenance, lab processing steps, and contextual references for pollen and dating methodologies.

## Uses and Context
- Primary uses:
  - Quantify litter production and decay, root production, and above/below-ground growth dynamics.
  - Build carbon and peat age models through radiocarbon and Pb-210 dating.
  - Compare productivity and decomposition dynamics between peatland pole forest (NYO-03) and palm swamp (VEN-02).
  - Integrate with pollen data to interpret historical vegetation and ecosystem change.
  - Support palaeoecological reconstructions and carbon cycle assessments in Amazonian peatlands.
- Considerations for data users:
  - Be aware of data quality notes (e.g., 2019 VEN-02 palm census excluded) and missing census periods.
  - Units and collection intervals vary by dataset; refer to the individual file metadata for specifics.
  - Geographical context covers latitudes approximately -4.07 to -5.88 and longitudes -73.27 to -74.83.

## Access and Metadata
- Project and funding context:
  - Funded by UKRI-NERC, grant NE/R000751/1, with P.I. Dr Ian Lawson.
- Data format and access:
  - Ten CSV files with structured variables and sample metadata.
  - Detailed methodological notes and pollen taxonomy references provided within the dataset descriptions.