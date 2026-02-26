# Data on bait use of arboreal ants from an experiment in Malaysian Borneo, 2015-2018. (2019) Law, S.J. and Parr, C.L.

## Overview of the dataset
- Dataset records ant abundance at baited traps placed at 5 m vertical intervals across 12 trees in lowland tropical rainforest.
- Bait types: carbohydrate vs protein; ants identified to genus and morphospecies; abundance recorded per trap.
- Trap location strata: canopy (above the first branch) or trunk (below the first branch).
- Data collected February–May 2016, focusing on four control plots (part of a larger insecticide-treatment experiment conducted 2014–2017).
- Part of the UK NERC-funded Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.

## Experimental design context
- Study site: old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Experimental plots: 12 plots (50 x 50 m) with 4 control, 4 ant-suppression, 4 termite-suppression plots; maintained 2014–2017.
- Ant suppression used two bait types: Synergy Pro® and a sugar solution with imidacloprid; termite suppression used imidacloprid and fipronil treatments.
- For the bait-use analysis reported here, data are drawn from the four control plots (no ant or termite suppression affecting those plots).

## Data collection and methods
- Ant sampling: February–May 2016, across 12 trees.
- Sampling stations: on each tree, traps set vertically every 5 m from ground to canopy; 28–44 traps per tree (mean 35 ± SD 6); total traps across trees = 416 (208 carbohydrate, 208 protein).
- Trap pairs per station: each station had two pairs of traps on opposite sides of the trunk; each pair contained one carbohydrate trap (honey/oats) and one protein trap (tuna); traps left open for 24 hours.
- Processing: specimens preserved in 70% ethanol; ants identified to genus and morphospecies; voucher specimens stored at the University of Liverpool and Universiti Malaysia Sabah.
- Access and safety: canopy sampling via single rope technique with safety line.

## Data file and structure
- Data file: BaitUseData.csv
- Columns and meanings:
  - Plot: experimental plot identifier.
  - Tree code: unique ID for each sampled tree.
  - Tree genus: genus of the sampled tree.
  - Tree species: species of the sampled tree.
  - Height: vertical height above ground where the trap was set (in meters).
  - Bait: type of bait in the trap: 'C' = carbohydrate; 'P' = protein.
  - Repetition: which trap pair on the trunk (1 or 2).
  - Sample: unique trap identifier.
  - Strata: trap location stratum: 'Trunk' or 'Canopy'.
  - Subfamily: ant subfamily classification.
  - Genus: ant genus.
  - Morphospecies: morphospecies ID within a genus.
  - Ant species: species designation (genus plus morphospecies ID); corresponds to morphospecies.
  - Abundance: number of individuals of this morphospecies observed in the trap.

## Data provenance and availability
- Data collection: S.J. Law.
- Data interpretation: S.J. Law and C.L. Parr.
- Voucher specimens: lodged in reference collections at the University of Liverpool and Universiti Malaysia Sabah.
- Context: part of the BALI consortium; related project information available at the Bali consortium site.

## How this dataset can be used
- Analyze patterns of bait preference (carbohydrate vs protein) among arboreal ants.
- Examine species co-occurrence and community structure across canopy vs trunk habitats.
- Enable self-service exploration through the provided trap-level abundance data across multiple trees and height intervals.
- Integrate with other BALI-related datasets to assess broader biodiversity and habitat-function relationships.