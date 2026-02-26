# Data on bait use of arboreal ants from an experiment in Malaysian Borneo, 2015-2018.

## Overview

- Dataset name: BaitUseData.csv containing ant abundance at baited traps.
- Study system: arboreal ants in lowland tropical rainforest.
- Key variables: bait type (carbohydrate vs protein), trap location height (5 m intervals), canopy vs trunk stratum, and morphospecies-level identifications with abundance per trap.
- Timeframe: data collected February–May 2016; part of a larger project conducted 2014–2017 within 2015–2018 reporting.
- Purpose: describe patterns of bait use and species co-occurrence in arboreal ant assemblages.

## Study site and experimental design

- Location: Maliau Basin Conservation Area, Sabah, Malaysia (lowland old-growth dipterocarp rainforest).
- Layout: 12 experimental plots (50 x 50 m) within a 42-ha area, plus a 15 m buffer; total treated area 80 x 80 m.
- Treatments (established Oct 2014): four control plots, four ant-suppression plots, four termite-suppression plots; maintained through Oct 2017.
- For this dataset: data derived from the four control plots (no insecticide treatments affecting ants present in the sampling period).
- Context: part of the UK NERC-funded Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.

## Data collection and methods

- Sampling design: ants collected from February–May 2016 across 12 trees.
- Trap deployment: vertical sampling stations every 5 m from ground to canopy; each tree had 28–44 traps (mean 35 ± 6); total traps: 416 (208 carbohydrate, 208 protein).
- Trap pairs: each station had two pairs of traps on opposite sides of the trunk; each pair contained one carbohydrate trap and one protein trap, separated by ~20 cm.
- Trap exposure: traps left open for 24 hours; specimens preserved in 70% ethanol; canopy access via single rope technique.
- Taxonomic resolution: specimens identified to genus and morphospecies (unique morphospecies ID within each genus); voucher specimens stored at University of Liverpool and Universiti Malaysia Sabah.
- Data stewardship: S.J. Law led data collection; Law and Parr handled interpretation.

## Data structure and contents

- File: BaitUseData.csv with the following columns:
  - Plot: experimental plot identifier.
  - Tree code: unique tree identifier.
  - Tree genus / Tree species: tree identification.
  - Height: vertical height above ground of trap (meters).
  - Bait: 'C' = carbohydrate; 'P' = protein.
  - Repetition: pair number (1 or 2) indicating which trap pair on the trunk.
  - Sample: unique trap identifier.
  - Strata: 'Trunk' or 'Canopy' (location relative to first branch).
  - Subfamily: ant taxonomic subfamily.
  - Genus: ant genus.
  - Morphospecies: morphospecies ID within genus.
  - Ant species: formal species name corresponding to morphospecies.
  - Abundance: count of individuals for that morphospecies in the trap.

## Data quality, provenance, and access

- Standardised collection and identification procedures support cross-site comparisons and temporal monitoring.
- Voucher specimens are stored with collaborating institutions, enabling verification and replications.
- Dataset is framed within a controlled monitoring context and linked to broader BALI research on tropical ecosystem function.

## Utility for environmental monitoring

- Enables analysis of spatial (canopy vs trunk) and vertical distribution of bait use by arboreal ants.
- Supports investigations into species co-occurrence and responses to bait types across a standardised sampling regime.
- Provides a reproducible data structure suitable for integration with other environmental monitoring datasets and time-series analyses.