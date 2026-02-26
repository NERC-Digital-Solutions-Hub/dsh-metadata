# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Dataset describing ecosystem productivity at two Peruvian wetland sites (NYO-03 peatland pole forest and VEN-02 palm swamp) in the Pastaza-Marañón Basin.
- Aims to estimate and compare litter and root production and decay over a full annual cycle to understand carbon accumulation dynamics in peat; includes palaeoecological information from peat cores.
- Ten CSV datasets cover a range of measurements, with some datasets extended to additional sites for context.

## Data files and what they measure
- 3.1 Decomposition bags: litter decomposition rates for different materials and treatments.
- 3.2 Coarse woody debris (CWD): mass and categories of newly fallen woody material; includes palm fronds.
- 3.3 Littertraps: monthly collections of litter; components separated (leaves, woody, reproductive, miscellaneous).
- 3.4 Root ingrowth cores: estimates of root production from ingrowth cores.
- 3.5 Dendrometer bands: short-term tree diameter growth (notched bands, quarterly censuses).
- 3.6 Palm heights: growth measurements for selected palms across two census dates.
- 3.7 Radiocarbon (14C): downcore peat dating for age models and initiation ages.
- 3.8 Lead-210 (210Pb): age-depth models for near-surface peat; includes 214Pb and Cs-137 data.
- 3.9 Carbon and Nitrogen (C and N): bulk C and N concentrations in peat cores.
- 3.10 Pollen: subfossil pollen counts for palaeoecological reconstruction.

## Study sites and period
- NYO-03: Nueva York peatland pole forest.
- VEN-02: Veinte de Enero palm swamp.
- Region: Pastaza-Marañón Basin, Peru.
- Timeframe: data collected 2018–2020 (with some datasets linking to surrounding contexts); additional ages via radiocarbon dating extend historical perspective.

## Collection and methods (high-level)
- Decomposition bags: surface and deeper peat placements; dried to constant weight; regular retrievals planned up to two years.
- CWD: transects along plot margins; mass weighed in field, subsamples dried; palm litter categorized separately.
- Littertraps: 1 x 1 m, 1 mm mesh, raised 1 m, monthly collections for a year; components dried and weighed.
- Root ingrowth cores: eight per plot; filled with peat; collected quarterly; roots hand-picked, dried, weighed.
- Dendrometer bands: spring-loaded bands installed in 2018; growth inferred from notch movement at census dates.
- Palm heights: two census dates; measurements taken from mark to canopy/base of highest leaf after climbing.
- 14C dating: 70 dates total across peat cores; pre-treated and analysed for age modelling.
- 210Pb dating: top 39 cm of cores analysed via gamma spectroscopy for age-depth models.
- C and N: dried peat composites milled and analysed for carbon and nitrogen contents.
- Pollen: standard palynology from peat cores; preparation and counting following published protocols.

## Quality control and data integrity
- Replicates included and field-standardized procedures followed (field sheets, standardized booking).
- Some data limited by field disturbances; certain censuses or measurements flagged as unreliable and excluded (e.g., VEN-02 2019 palm heights; some dendrometer data).
- Instruments and protocols aligned with established frameworks (RAINFOR for CWD; Honorio & Baker methods for litter and dendrometer work).
- QA includes separate mass measurements for checks (e.g., total vs. component masses in littertraps), blanks and standards for C/N analyses, and appropriate calibration steps for radiometric measurements.

## Data structure and units
- Files are UTF-8 encoded CSVs; variables defined per dataset; missing values indicated as NA.
- Key structural elements by dataset (examples):
  - Site_code, depth, installation and collection dates, replicates, and mass measurements for decomposition bags.
  - Category, diameter_class, fresh/dry mass, and subsample metrics for CWD.
  - Collection_month, start date, end date, and component masses for littertraps.
  - Core and collection metadata (core_number, collection_month/date, root_mass_g for ingrowth cores).
  - Dendrometer: tag numbers, installation/measurement dates, initial diameter, growth, census date.
  - Palm heights: tag numbers, census numbers/dates, height measurements.
  - 14C: sample identifiers, site, depths, conventional ages, enrichment, etc.
  - 210Pb: core_code, depths, activities, uncertainties, MDAs.
  - C/N: site, core, depth, %C, %N.
  - Pollen: core_code, depth, counts by taxa.
- Spatial coverage: latitude and longitude provided for radiocarbon dataset; overall site coordinates within approximately -4.07 to -5.88 S and -73.27 to -74.83 W.
- Data provenance and project context included (CSAP project, UKRI-NERC funding).

## Governance, openness, and reproducibility considerations
- Protocol transparency: references to established manuals and protocols (RAINFOR, Honorio & Baker) enhance comparability and reproducibility.
- Metadata depth: detailed variable definitions, units, sample handling, and processing steps documented.
- Data sharing and openness: dataset emphasizes sharing underlying data and metadata; transparent QA and method documentation support policy-relevant evaluation and future reuse.
- Data gaps and reliability: explicit notes on unreliable measurements and planned future collections highlight the need for ongoing data governance and update plans.

## Relevance for monitoring frameworks
- Demonstrates a comprehensive, multi-method approach to ecosystem productivity monitoring in tropical peatlands, aligning with policy-relevant indicators of carbon cycling and peat formation.
- Provides standardized data structures and QA practices that support cross-site comparisons, trend analysis, and integration with palaeoecological context for long-term environmental health assessment.
- Highlights practical data governance considerations—metadata completeness, data provenance, replication, and handling of imperfect data—that policy teams and monitoring teams must manage when deploying environmental health measures.
- Useful as a model for structuring monitoring datasets with clear documentation, reproducible methods, and explicit notes on data limitations to inform decision-making and future data collection planning.