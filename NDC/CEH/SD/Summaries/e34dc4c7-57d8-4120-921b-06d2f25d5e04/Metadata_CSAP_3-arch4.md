# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Two forest census plots in Peru: NYO-03 (peatland pole forest) and VEN-02 (palm swamp), located in the Pastaza-Marañón Basin.
- Primary aim: estimate and compare litter and root production and decay rates over a full annual cycle to understand carbon accumulation dynamics in peat; includes downcore data for palaeoecological context.
- Ten CSV datasets accompany the core data, providing measurements from multiple complementary approaches (decomposition, litterfall, root production, tree growth, peat dating, and palaeoecology).

## Data assets (ten CSV files)
- CSAP_3.1_Decomposition_bags.csv: litter decomposition rates for different materials.
- CSAP_3.2_CWD.csv: coarse woody debris (and large palm litter) along transects.
- CSAP_3.3_Littertraps.csv: monthly collections of litter in 1x1 m traps.
- CSAP_3.4_Root_ingrowth_cores.csv: root production estimates from ingrowth cores.
- CSAP_3.5_Dendrometer_bands.csv: short-term tree diameter growth from dendrometer bands.
- CSAP_3.6_Palm_heights.csv: palm height growth from two census dates.
- CSAP_3.7_14C.csv: radiocarbon dates for peat age and downcore age models.
- CSAP_3.8_210Pb.csv: Lead-210 dating data for near-surface peat and age-depth modeling (includes Pb-214 and Cs-137 where measured).
- CSAP_3.9_C_N.csv: total carbon and nitrogen concentrations in peat cores.
- CSAP_3.10_Pollen.csv: subfossil pollen counts for palaeoecological reconstruction.

## Collection, generation, and methods
- NYO-03 and VEN-02 sites were used for most measurements; NYO-03 is peatland forest, VEN-02 is a palm swamp.
- Decomposition bags (3.1): placed at various depths (mostly surface) in subplots; dried and weighed after retrieval.
- Coarse woody debris (3.2): collected along four transects; palm fronds recorded; wet mass followed by subsampling and dry mass determination.
- Littertraps (3.3): 1x1 m, elevated traps with 1 mm mesh; monthly collections for a year; material separated into components and dried/ weighed.
- Root ingrowth cores (3.4): eight cores per plot; filled with root-free peat; installed in peat; collected quarterly; roots dried and weighed.
- Dendrometer bands (3.5): spring-loaded bands set at ~1.3 m; initial diameter recorded; growth tracked across census dates.
- Palm heights (3.6): measured by climbing palms; two census dates with distances from base to canopy and leaf base.
- Radiocarbon dating (3.7): 70 dates across nine sites for peat initiation ages and downcore age models; NEIF pre-treatment and AMS analysis.
- Pb-210 dating (3.8): top 39 cm of peat cores analyzed for Pb-210, Pb-214, and Cs-137 to build age-depth models; gamma spectroscopy performed at BGS.
- Carbon and nitrogen (3.9): total C and N on cores; samples dried, milled, and analyzed with elemental analyzer.
- Pollen (3.10): subfossil pollen from peat cores; standard preparation and microscopy; taxa counts for vegetation history.

## Quality control and data integrity
- Replicates and standardized field procedures applied across datasets; field data collected by experienced staff using standardized sheets.
- Quality checks include cross-checks against field sheets, separation of components in litter traps, and removal/replacement of data from disturbed or unreliable measurements (e.g., VEN-02 2019 palm heights deemed unreliable; census repeated in 2020).
- Protocols align with established guidelines (RAINFOR for CWD, Honorio & Baker for litter traps) and NEIF/other standards for dating work.
- Data are provided with clear metadata, units, and data structure (UTF-8 CSV with NA as missing).

## Data structure and metadata
- Each file uses comma-separated values with descriptive column names, including site code, collection date, depth, mass/length measurements, and taxonomic or material classifications.
- Spatial coordinates are included where relevant (decimal degrees, WGS84).
- Time references are recorded in consistent formats (dates and elapsed months since start).
- Documentation notes standardization and data provenance, including laboratory methods and QA steps.

## Use cases and governance for Data Leaders
- Comprehensive view of ecosystem productivity and carbon dynamics in two contrasting Amazonian wetland habitats, enabling cross-site data integration and regional comparisons.
- Facilitates data-driven policy and management discussions around peat carbon accumulation and palaeoecological context.
- Demonstrates robust data governance: multiple data streams with explicit QA, standardized methods, traceable provenance, and clear documentation of any data gaps or unreliable measurements.
- Potential for extending analyses through metadata-rich linkage to other networks (e.g., cross-referencing with RAINFOR-style datasets or other carbon cycle studies) and for informing data standards in mixed-field datasets.