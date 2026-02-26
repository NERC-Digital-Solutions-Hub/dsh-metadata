# Data on bait use of arboreal ants from an experiment in Malaysian Borneo, 2015-2018.

## Overview
- Dataset of arboreal ant abundance at baited traps set at 5 m vertical intervals across 12 trees in a lowland tropical rainforest.
- Traps used two baits: carbohydrate and protein; ants identified to morphospecies with abundance recorded.
- Data collected to describe patterns of bait use and species co-occurrence in arboreal ant assemblages.
- Location: Maliau Basin Conservation Area, Sabah, Malaysia; sampling in 2016 (February–May).
- Contribution from the UK NERC-funded Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.

## Experimental design
- Study area: old-growth dipterocarp rainforest; 12 experimental plots within a 42-ha area, each 50 x 50 m with a 15 m buffer (total treated area 80 x 80 m). Sampling focused on the central 50 x 50 m to avoid edge effects.
- Plot treatment (not all data come from all treatments): 4 control, 4 ant-suppression, 4 termite-suppression plots; treatments applied Oct 2014–Oct 2017.
- Ant suppression used two poison baits; termite suppression used physical mound removal plus poisoned baits.
- For the bait-use investigation, data were collected only from the four control plots.

## Methods
- Sampling: February–May 2016; 12 trees per study area; vertically along each tree from ground to canopy in 5 m intervals.
- Traps: 416 baited traps in total (208 carbohydrate, 208 protein); sampling stations comprised two pairs of traps per height interval, each pair on opposite sides of the trunk.
- Baits: carbohydrate (honey and oats) and protein (tuna).
- Procedure: traps left open for 24 hours; specimens preserved in 70% ethanol.
- Identification: ants identified to genus and morphospecies; voucher specimens deposited in a reference collection at the University of Liverpool and Universiti Malaysia Sabah.
- Canopy access: via single rope technique with safety line for climbers.
- Responsibilities: S.J. Law collected data; S.J. Law and C.L. Parr handled interpretation.

## Data structure and contents
- Data file: BaitUseData.csv (CSV format).
- Columns and meanings:
  - Plot: experimental plot identifier.
  - Tree code: unique tree identifier.
  - Tree genus / Tree species: taxonomic information for the tree.
  - Height: vertical height of the trap above ground (in meters).
  - Bait: C = carbohydrate; P = protein.
  - Repetition: which trap pair (1 or 2) within a sampling station.
  - Sample: unique trap identifier.
  - Strata: Trunk or Canopy (below/above first branch).
  - Subfamily / Genus / Morphospecies / Ant species: ant identification details (morphospecies-based naming; genus+morphospecies ID).
  - Abundance: count of individuals for each morphospecies within the trap.
- Sampling details: 416 traps across 12 trees; two bait types per trap; each trap pair recorded separately.

## Data provenance, quality, and access
- Part of the BALI consortium data collection; vouchers stored at University of Liverpool and Universiti Malaysia Sabah.
- Data collected under controlled field conditions with standardized protocols to enable comparability across plots and times.
- Metadata include trap position, bait type, stratum, and taxonomic details, supporting reuse in ecological monitoring and policy evaluation.
- Data focus: four control plots; provides baseline patterns for bait use and species co-occurrence in arboreal ant communities.

## Potential uses for monitoring and policy decisions
- Baseline characterization of arboreal ant assemblages across canopy and trunk strata in tropical rainforest.
- Evaluation of bait-type preferences and how resource placement affects ant assemblages, informing monitoring protocols for arthropod activity.
- Analysis of spatial patterns (vertical stratification, across-tree variation) and species co-occurrence networks to monitor ecosystem function and health.
- Data governance and metadata planning for monitoring frameworks: demonstrates importance of clear data structure, voucher retention, and accessible specimen records to enable transparent, open data sharing.
- Provides a template for linking ecological observations (abundance, diversity) with environmental context (plot treatment status, canopy heights) to inform decisions on sampling design, data management, and reporting.

## Limitations and considerations
- Data for this descriptor come from four control plots only; may limit generalization across treatments.
- Taxonomic resolution is to morphospecies level; finer species-level identifications may be needed for certain policy analyses.
- Temporal scope is 2016 (February–May); may not capture interannual variability or longer-term trends.
- Bait-based sampling may reflect immediate foraging responses rather than permanent community structure.