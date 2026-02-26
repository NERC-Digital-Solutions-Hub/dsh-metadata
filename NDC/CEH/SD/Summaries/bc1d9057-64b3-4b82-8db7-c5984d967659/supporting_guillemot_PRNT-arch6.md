# Data Collection

## Overview
- NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Scotland (56.2° N, 2.6° W) chosen for its large, accessible common guillemot population.
- Aim: quantify strain-specific seroprevalence of Great Island virus (GIV) within the guillemot population.
- Full dataset tests up to 12 GIV strains; serology conducted to detect virus-specific neutralising antibodies.

## Study design and sampling
- 144 common guillemots captured between 1993 and 1995; blood collected on filter paper.
- Plaque reduction neutralisation tests (PRNT) performed to detect virus-specific neutralising antibodies.
- Part of dataset described in Nunn et al. (2006). Detailed methods follow the publication, with two methodological variations labeled MAN and KMW.

## Assay methods (high level)
- Virus isolation via tick-derived material on BHK21 and Vero cells; BRDV from a tick pool in St Abbs Head.
- Blood on filter paper discs eluted in PBST (phosphate-buffered saline with Tween 20 and antibiotics).
- Serum-virus mixtures prepared and incubated before adding to Vero cells; plaque assays conducted with carboxymethylcellulose overlay.
- Results expressed as average fold decrease in virus titre relative to controls (virus incubated in PBST or control chicken blood eluate).
- Each sample assayed multiple times (MAN: 4 replicates; KMW: 4 replicates with slightly different volumes/dilutions).

## Data structure and variables
- BTO_Ring: Unique ID for each bird.
- Collection_date: Date of blood sample collection.
- Subcolony: Site of capture.
- Sex: Sex of the bird.
- Status: Biological status (PB = pre-breeding; B = breeding).
- Virus_strain: Strain tested (MDNV, CBNV, COYV, BRDV, AMDV; includes Maiden virus, Colony B North, Colony virus, Broadhaven virus, Above Maiden virus).
- Sample_PFUx: Number of plaque-forming units (PFU) in the well containing the bird’s blood sample.
- Sample_PFU_av: Mean PFU across replicates for the bird/sample.
- Control_PFU_av: Mean PFU in control wells (PBST or chicken blood eluate).

## Data provenance, notes, and considerations
- Differences between MAN and KMW methods noted; slight methodological variations exist across parts of the dataset.
- Dataset includes multiple assay repeats per sample to support reliability.
- BRDV isolate provenance differs from the Isle of May tick-derived strains (from St Abbs Head), which may affect comparative analyses.

## Potential data products and use
- Seroprevalence estimates by virus strain, stratified by collection date, subcolony, sex, and breeding status.
- Data products enabling self-service exploration of associations between host factors and serological responses.
- Baseline data for studies on host-pathogen dynamics in colonial seabirds and cross-study methodological comparisons.