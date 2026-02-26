# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

- The dataset collection focuses on estimating and comparing litter and root production and decay over a complete annual cycle to understand carbon accumulation dynamics in peatlands of the Pastaza-Marañón Basin, Peru.
- Two primary study plots: NYO-03 (peatland pole forest) and VEN-02 (palm swamp); with selected datasets extended to additional sites for contextual comparison.
- In addition to contemporary productivity measures, the data include downcore peat core analyses for palaeoecological context (radiocarbon dating, Pb-210 dating, C/N, and pollen records).

## Datasets included (ten CSV files)

- CSAP_3.1_Decomposition_bags.csv
  - Litter decomposition rates for different materials; bags installed at various depths, with planned multi-year retrieval; final masses recorded.
- CSAP_3.2_CWD.csv
  - Coarse woody debris data along four transects per plot; includes palm frond material and wood, with fresh and subsample masses and size classifications.
- CSAP_3.3_Littertraps.csv
  - Litter collected from 1 x 1 m traps raised above ground; monthly collections over 12 months; includes mass by component (leaves, woody, reproductive, etc.).
- CSAP_3.4_Root_ingrowth_cores.csv
  - Eight ingrowth cores per plot; three-monthly collection; total dry mass of roots extracted per core.
- CSAP_3.5_Dendrometer_bands.csv
  - Short-term tree diameter growth via dendrometer bands; includes installation, notching dates, initial diameters, and growth by census.
- CSAP_3.6_Palm_heights.csv
  - Palm height measurements on two census dates; canopy-to-ground distances measured from marked trunks.
- CSAP_3.7_14C.csv
  - Radiocarbon dating dates (70 dates total) used to estimate peat initiation ages and construct down-core age models; NEIF pre-treatment data.
- CSAP_3.8_210Pb.csv
  - Lead-210, Pb-214, and Cs-137 activities for top peat cores to develop age-depth models; gamma spectroscopy details and detection limits provided.
- CSAP_3.9_C_N.csv
  - Total carbon and total nitrogen concentrations in peat cores; sample preparation and analysis procedure described.
- CSAP_3.10_Pollen.csv
  - Subfossil pollen counts from peat cores; data used to reconstruct ecological change over time; taxonomy aligned with published keys and reference databases.

## Study sites and scope

- NYO-03: Nueva York peatland pole forest (peatland site).
- VEN-02: Veinte de Enero, palm swamp (palm-dominated wetland).
- Geographic focus: Pastaza-Marañón Basin, Peru; data cover both surface productivity metrics and downcore palaeoecological indicators.

## Collection, processing, and QA methods

- General approach: standardized field protocols, replication, and documentation on installation, collection dates, and depths.
- Specific practices:
  - Decomposition bags: standardized litter types, surface placement or deeper depths, weekly to biannual retrievals, drying and weighing for mass change.
  - CWD: transect-based collection, immediate wet weighing, subsampling for dry mass estimation.
  - Littertraps: monthly collections, component separation, dry weighing.
  - Root ingrowth cores: uniform core design, quarterly collection, hand-picking of roots, drying and weighing.
  - Dendrometer bands: regular census-based growth measurement after initial notch, with notes on disturbances and replacements.
  - Palm heights: climbing-based measurements on two dates with canopy-born marks.
  - Radiocarbon and Pb-210 dating: standard pre-treatment and analysis protocols (NEIF, BGS), including age-model construction and gamma spectroscopy.
  - C and N analyses: prepared cores, drying, milling, and elemental analysis with appropriate blanks/standards.
  - Pollen: standard preparation (washing, acetolysis, heavy liquid), pollen counting, and taxonomy referencing published keys and databases.
- Quality control highlights:
  - Replicates and standardized field sheets across datasets.
  - Data curation excludes unreliable census data (e.g., VEN-02 2019 census); missing data flagged as NAs.
  - Disturbed or destroyed dendrometer bands removed from the dataset.
  - Pollen and chemical analyses accompanied by reference standards and calibration steps.

## Data structure, units, and recording

- File format: UTF-8 encoded, comma-separated values; variables as columns, records as rows; missing data indicated as NA.
- Common structure elements:
  - Site codes, plot/transact identifiers, collection dates, and census numbers.
  - Quantitative measurements (e.g., masses in grams, diameters in mm, heights in cm, depths in cm).
  - Geospatial coordinates provided where relevant (latitude/longitude for core samples and pollen).
- Example variable types by dataset:
  - Decomposition bags: initial and end masses, depth, time period, percentage remaining.
  - Littertraps: total mass and component masses (leaves, woody, reproductive, etc.).
  - Root ingrowth cores: total root mass per collection.
  - Dendrometer bands: initial diameters, growth increments, census dates.
  - Palm heights: ground-to-canopy, canopy-to-leaf base, total height.
  - Radiocarbon and Pb-210: age estimates, activity measurements, densities, and uncertainties.
  - C/N: carbon and nitrogen weight percentages.
  - Pollen: counts by taxa, depth, core, and sampling details.

## Potential uses for environmental monitoring and policy analysis

- Cross-site comparison of litter production, decay rates, and root production within Amazonian peatlands and palm swamps.
- Estimation of peat carbon accumulation dynamics and total carbon stocks over annual cycles.
- Integration of radiometric dating data with contemporary productivity to contextualize carbon sequestration over longer timescales.
- Palaeoecological reconstruction of vegetation change and ecosystem responses to climatic or hydrological shifts.
- Data interoperability and reuse through standardized QA procedures and documented metadata, enabling broader synthesis with other monitoring datasets.

## Data format and accessibility

- Data are provided as structured CSV files with detailed metadata in the accompanying documentation, following established protocols (RAINFOR, Honorio & Baker; NEIF/Genie 2000s references).
- Documentation includes data structure descriptions, variable definitions, and quality control notes to support reproducibility and reuse.