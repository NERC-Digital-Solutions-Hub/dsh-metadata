# Data on bait use of arboreal ants from an experiment in Malaysian Borneo, 2015-2018. (2019) Law, S.J. and Parr, C.L.

## Overview
- Dataset: BaitUseData.csv, recording ant abundance at baited traps across 12 trees in lowland tropical rainforest.
- Baits: carbohydrate (honey/oats) and protein (tuna); traps paired per height, with canopy vs trunk strata noted.
- Purpose: describe patterns of bait use and species co-occurrence in arboreal ant assemblages.
- Timeframe: data collected February–May 2016; part of a broader study conducted 2014–2017 within Maliau Basin, Sabah, Malaysia.
- Source: UK NERC-funded Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.

## Experimental design and sampling
- Study area: lowland old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah.
- Plot setup: twelve 50×50 m experimental plots (Oct 2014) within a 42-ha area; central 50×50 m used to avoid edge effects; four plots each for control, ant suppression, and termite suppression.
- Treatments: ant suppression with two baits (Synergy Pro® and imidacloprid in cat-food sugar solution); termite suppression with poisoned wood-based baits (TPRs and tea bags with fipronil). Suppression maintained until Oct 2017.
- Focus dataset: data collected exclusively from the four control plots (i.e., no insecticide treatment).
- Sampling on each tree: 12 trees sampled; vertical sampling stations every 5 m from ground to canopy; traps per tree ranged 28–44 (mean ~35).
- Trap pairs: at each height, two pairs of baited traps (four traps total) on opposite sides of the trunk; each pair includes one carbohydrate and one protein trap; traps left open for 24 hours.
- Collection and preservation: traps collected and ants preserved in 70% ethanol.
- Taxonomic work: ants identified to genus and morphospecies; voucher specimens housed at University of Liverpool and Universiti Malaysia Sabah.
- Access and safety: canopy access via single rope technique with safety line; data collection attributed to S.J. Law; interpretation by S.J. Law and C.L. Parr.

## Data content and structure
- File: BaitUseData.csv containing a single dataset.
- Columns and meanings:
  - Plot: experimental plot identifier.
  - Tree code: unique identifier for each sampled tree.
  - Tree genus: genus of the sampled tree.
  - Tree species: species name of the tree.
  - Height: vertical height above ground of each trap (in meters).
  - Bait: type of bait; 'C' = carbohydrate, 'P' = protein.
  - Repetition: which trap pair at each height (1 or 2).
  - Sample: unique trap identifier.
  - Strata: vertical location of trap; 'Trunk' or 'Canopy'.
  - Subfamily: ant subfamily classification.
  - Genus: ant genus.
  - Morphospecies: morphospecies ID within genus.
  - Ant species: genus plus morphospecies ID (as a species label concept).
  - Abundance: count of individuals of each morphospecies captured in the trap.
- Data characteristics:
  - 416 traps across 12 trees (208 carbohydrate, 208 protein).
  - Each trap yields counts by morphospecies within a trap.
  - Canopy vs trunk classifications are explicitly recorded.

## Provenance, curation, and contributing teams
- Custodians: S.J. Law (data collection) and C.L. Parr (interpretation); BALI consortium contributor.
- Data lineage: field collection February–May 2016; part of a broader project (2014–2017) examining insecticide-based suppressions.
- Voucher specimens: deposited in reference collections at University of Liverpool and Universiti Malaysia Sabah.
- Documentation: dataset includes explicit definitions for all columns and measurement units.

## Usage notes, limitations, and potential applications
- Intended use: analyze bait preferences and co-occurrence patterns among arboreal ants; assess how trap stratum (canopy vs trunk) and bait type relate to ant assemblages.
- Limitations:
  - Only control plots used for this bait-use analysis; results may not generalize to ant- or termite-suppressed plots.
  - Temporal scope limited to Feb–May 2016; seasonal effects not captured.
  - Morphospecies-level identification (not all specimens may map to formal species names); interpret as genus-level patterns with morphospecies resolution.
  - Data reflect presence/abundance in traps over a 24-hour window; may not capture longer-term foraging dynamics.
- Considerations for data management and reuse:
  - Ensure consistent interpretation of Bait (C vs P), Strata (Trunk vs Canopy), and Repetition.
  - Treat Abundance as count data per morphospecies per trap; suitable for occupancy or abundance analyses with appropriate zero-inflation handling.
  - Acknowledge provenance and preservation status of voucher material when cross-referencing species identifications.

## Related resources
- Project context: Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.
- Data and repository references: BaitUseData.csv; can be linked to the broader BALI dataset and study outputs.