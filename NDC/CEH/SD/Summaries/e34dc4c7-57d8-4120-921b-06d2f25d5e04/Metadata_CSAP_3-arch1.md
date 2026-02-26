# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

- Two study plots in Peru’s Pastaza-Marañón Basin: NYO-03 (peatland pole forest) and VEN-02 (palm swamp)
- Aim: estimate and compare litter and root production and decay across an annual cycle; understand carbon accumulation dynamics in peat; provide palaeoecological context with downcore data
- Ten CSV datasets (3.1–3.10) with complementary measurements to build a comprehensive view of ecosystem productivity and peat development
- Some datasets extend to additional sites for contextual interpretation; pollen and radiometric data enable temporal reconstruction of vegetation and peat formation

## Datasets and content

- CSAP_3.1 Decomposition_bags
  - Litter types (palm leaf, hardwood leaf/root/stem), depth, time_period, replicates, sample and bag identifiers
  - Measurements: initial and final mass, mass remaining, installation/collection dates, subplots, and nearest-tree linkage
- CSAP_3.2 Coarse_woody_debris (CWD)
  - NYO_03 and VEN_02 transects; palm litter included
  - Variables: date, collection month, category/size class, fresh mass, subsample masses, and volumes
- CSAP_3.3 Littertraps
  - Ten subplots per plot; 1x1 m traps, 1 mm mesh; monthly collections for 12 months
  - Components: total mass and breakdowns (leaves, woody, reproductive, miscellaneous)
- CSAP_3.4 Root_ingrowth_cores
  - Eight replicates per plot; 50 cm long, 6 cm diameter cores filled with site peat
  - Collection every three months; root dry mass per core
- CSAP_3.5 Dendrometer_bands
  - Tree-by-tree growth via notch movement; initial diameter recorded; quarterly censuses
  - Census data with band status, some data later missing or bands replaced
- CSAP_3.6 Palm_heights
  - Palm height measurements on two census dates; climbing-based measurements from ground to canopy and leaf base
  - Data quality: VEN-02 2019 census deemed unreliable and excluded; repeated in 2020
- CSAP_3.7 Radiocarbon (14C)
  - 70 dates from peat cores; used to estimate peat initiation age and construct down-core age models
  - NEIF pre-treatment and SUERC analysis; sample naming includes core and depth information
- CSAP_3.8 Lead-210 (210Pb)
  - Top 39 cm of two peat cores; activities for 210Pb, 214Pb, and 137Cs
  - Gamma spectroscopy and BEGe detector used; age-depth modelling support
- CSAP_3.9 Carbon and Nitrogen (C and N)
  - Five sites; dried and milled peat samples analyzed for total C and N by elemental analyzer
- CSAP_3.10 Pollen
  - Subfossil pollen counts from peat cores; depth-ferred downcore data
  - Taxonomy aligned with published keys and reference databases

## Study design and sites

- Geographical coordinates span roughly -4.07 to -5.88 latitude and -73.27 to -74.83 longitude for pollen-related samples
- NYO-03 and VEN-02 form the core comparison, with additional context from other sites for palaeo analyses
- Datasets together enable linking contemporary production/decay processes with peat formation history and vegetation change

## Methods and quality control

- Field methods follow established protocols (e.g., RAINFOR for CWD; Honorio & Baker for litter traps)
- Replication: multiple replicates per treatment and plot (e.g., eight replicates for bags and root cores)
- Quality control notes:
  - Excluded data: VEN-02 palm-height data from 2019 due to unreliability
  - Disturbed/missing data removed or flagged (e.g., dendrometer bands disturbed by animals)
  - Cross-checks against field sheets; standardized data collection sheets used
- Sample processing:
  - Litter and CWD samples dried at ~65°C; masses measured with precision balances
  - 14C and Pb dating performed with standardized pre-treatment, instrumentation, and calibration procedures
  - Pollen processed using established washes, sieving, acetolysis, and heavy-liquid flotation

## Data structure and units

- Files are UTF-8 encoded, comma-separated; variables in columns, observations in rows; NA indicates missing data
- Common formats:
  - Masses in grams (g) or dry mass (g)
  - Depths in centimeters (cm)
  - Diameters in millimeters (mm)
  - Heights in centimeters (cm)
  - Dates in dd/mm/yyyy
  - Radiometric data in activity units (Bq kg^-1) or age in years BP
- Each dataset includes site codes, core and plot identifiers, collection dates, and measurement-specific fields

## Potential analyses and applications

- Quantify litter and root production/decay rates across sites and time
- Link decomposition and CWD dynamics to carbon accumulation in peat
- Build age models for peat initiation and peat layer dating using 14C and 210Pb
- Reconstruct past vegetation dynamics with pollen data and relate to peat formation
- Integrate multiple data streams (biomass production, growth, radiometric dating) to model carbon balance in Amazonian peatlands
- Use standardized QC and metadata to ensure datasets are findable and reusable for replication or comparative studies

## Funding and attribution

- Funded by UKRI-NERC (grant NE/R000751/1)
- Principal Investigator: Dr Ian Lawson
- Data and methods compiled to support ecosystem productivity assessments in Amazonian wetland contexts