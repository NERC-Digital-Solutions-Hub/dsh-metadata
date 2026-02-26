# Data Collection

## Overview
- Part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Scotland, chosen for its large, accessible common guillemot population.
- Primary aim: quantify strain-specific seroprevalence of Great Island virus (GIV) within the guillemot population.

## Study Site and Samples
- 144 individual common guillemots captured between 1993 and 1995 on the Isle of May.
- Blood samples collected on filter paper.

## Laboratory Methods
- Plaque reduction neutralisation tests (PRNT) performed to detect virus-specific neutralising antibodies.
- Virus isolated from tick material; assays performed on Vero cells after preparation steps (details include cell lines, volumes, dilutions, and incubation times; two procedural variants noted as MAN and KMW).
- Results expressed as average fold decrease in virus titre relative to controls.
- Controls included virus incubated in PBST or chicken blood eluted from filter paper.

## Dataset Scope and Strains
- Virus strains tested in this dataset: Maiden virus (MDNV), Colony B North virus (CBNV), Colony virus (COYV), Broadhaven virus (BRDV), Above Maiden virus (AMDV); maximum of 12 strains tested.

## Data Structure and Fields
- BTO_Ring: Unique bird identifier.
- Collection_date: Date of blood sample collection.
- Subcolony: Site of bird observation.
- Sex: Bird's sex.
- Status: Breeding status (PB = pre-breeding, B = breeding).
- Virus_strain: Strain tested (as listed above).
- Sample_PFUx: Plaque forming units (PFU) per ml in the blood sample well.
- Sample_PFU_av: Mean PFU value for the sample.
- Control_PFU_av: Mean PFU in control wells.

## Data Provenance and References
- Part of data described in Nunn et al. (2006) Parasitology 132: 233-240.
- Detailed method excerpted from the publication; slight methodological differences between MAN and KMW noted.