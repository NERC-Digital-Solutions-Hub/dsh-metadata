# Data on bait use of arboreal ants from an experiment in Malaysian Borneo, 2015-2018. (2019) Law, S.J. and Parr, C.L.

## Overview
- Dataset: BaitUseData.csv recording ant abundance at baited traps at 5 m vertical intervals across 12 trees in lowland tropical rainforest.
- Baits: Carbohydrate (honey/oats) and protein (tuna); traps logged as canopy (above first branch) or trunk (below first branch).
- Purpose: Describe patterns of bait use and species co-occurrence in arboreal ant assemblages.
- Sampling timeframe and context: Collected Feb–May 2016 across four plots; part of the UK NERC-funded Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.
- Experimental background: Data come from control plots within a larger experimental setup that included ant suppression and termite suppression treatments established in Oct 2014 and maintained until Oct 2017.

## Experimental design
- Study site: Lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Plot setup: Twelve plots within a 42-ha area (50 x 50 m plots, with 15 m buffer; central 50 x 50 m sampled to avoid edge effects).
- Treatments: 4 control, 4 ant suppression, 4 termite suppression plots; placed at least 100 m apart.
- Ant suppression: Two bait types (Synergy Pro® with hydramethylnon and pyriproxyfen; and a Whiskas®-based sugar solution bait with imidacloprid).
- Termite suppression: Physical mound removal plus soil treatment with imidacloprid; additional poisoned toilet paper rolls and tea bags treated with fipronil; maintained semi-annually.
- Focus of dataset: Data for bait use collected only from the four control plots.

## Methods and data collection
- Ant sampling period: February–May 2016.
- Tree and trap setup: 12 trees; traps arranged vertically every 5 m from ground to canopy; 28–44 traps per tree (416 traps total; 208 carbohydrate, 208 protein).
- Trap pairing: Each sampling station had two pairs of traps on opposite sides of the trunk; each pair included one carbohydrate trap and one protein trap; traps left open for 24 hours.
- Strata: Traps categorized as Canopy (above first branch) or Trunk (below first branch).
- Specimen handling: After collection, ants preserved in 70% ethanol; specimens identified to genus and morphospecies; voucher specimens stored at University of Liverpool and Universiti Malaysia Sabah.
- Personnel: S.J. Law conducted data collection; Law & Parr responsible for interpretation.
- Access method: Canopy access via single rope technique with safety line.

## Data structure and fields (BaitUseData.csv)
- Plot: Experimental plot of data collection.
- Tree code: Unique identifier for each sampled tree.
- Tree genus / Tree species: Taxonomic identification of sampled tree.
- Height: Vertical height above ground of each trap (meters).
- Bait: Type of bait per trap: 'C' = carbohydrate; 'P' = protein.
- Repetition: Indicates which trap pair (1 or 2) within the sampling station.
- Sample: Unique identifier for each baited trap.
- Strata: Location of trap: 'Trunk' or 'Canopy'.
- Subfamily / Genus / Morphospecies / Ant species: Ant identification information; species names correspond to morphospecies (Genus + morphospecies ID).
- Abundance: Number of individuals of each species in a trap.

## Provenance and access
- Data contribution: UK NERC-funded BALI consortium.
- Voucher specimens: Stored at the University of Liverpool and Universiti Malaysia Sabah.

## Practical implications for data use and stewardship
- Rich, harmonized metadata for each trap enable analyses of vertical stratification (canopy vs trunk) and bait preference (carbohydrate vs protein).
- Data supports examination of co-occurrence patterns among arboreal ants and their responses to experimental context (even though bait-use data here is from control plots).
- Clear documentation of units, trap timing, and identification level supports reproducibility and integration with other datasets.
- Consideration for data leaders: verify data scope (control plots only for this dataset), data completeness, and potential integration with broader BALI datasets for cross-study comparisons.