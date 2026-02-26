# Data Collection

## Overview
- NERC-funded PhD project studying interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W), chosen for its large, accessible common guillemot population.
- Aim: quantify strain-specific seroprevalence for Great Island virus (GIV) within the guillemot population.
- Partial dataset previously presented in Nunn et al. (2006) Parasitology 132: 233-240.

## Field Sampling and Dataset
- 144 individual common guillemots captured between 1993 and 1995 on the Isle of May.
- Blood samples collected on filter paper; plaque reduction neutralisation tests (PRNT) used to detect virus-specific neutralising antibodies.
- Up to 12 Great Island virus strains tested in the full dataset.
- Detailed methods follow the publication by Nunn et al.; some differences between parts of the dataset are indicated by initials MAN and KMW.

## Laboratory Methods (Virus Isolation and PRNT)
- Virus isolation: clarified tick homogenate applied to BHK21 cells; two rounds of plaque picking on Vero cells.
  - Broadhaven virus (BRDV) isolated from a pool of nymphal ticks from St Abbs Head, Scotland; other strains from single ticks on Isle of May.
- Preparation: 2 × 10^5 Vero cells in 0.5 ml RPMI with 6% fetal bovine serum per well in a 24-well plate.
- Blood sample processing: discs (1.8 cm²) punched from filter-paper blood spots, eluted overnight at 4 °C in PBST (PBS with 0.05% Tween 20, antibiotics).
- Assay setup: predetermined volumes of eluted blood mixed with virus dilutions, incubated, then added to Vero cells.
  - MAN: 10 µl of sample with 10 µl of virus dilution; incubations differ (30 °C, 2 h) and later steps.
  - KMW: 7 µl of sample with 7 µl of virus dilution; different incubation times (30–37 °C, 2–4 h) and plating details.
- Plaque assay: after infection, overlay with carboxymethylcellulose; incubate several days, fix, and stain with crystal violet.
- Replicates: each blood sample assayed 4 times (MAN) or per KMW protocol (4 replicates implied).

## Data and Measurements
- Results expressed as average fold decrease in virus titre relative to controls.
- Controls: virus incubated in PBST or in chicken blood eluted from filter paper; controls assayed at least 2 times.
- Primary outputs per test: plaque-forming units (PFU) values with respect to virus strains and samples.

## Data Structure (Variables)
- BTO_Ring: Unique ID for each bird.
- Collection_date: Date of blood sample collection.
- Subcolony: Site within the island where the bird was found.
- Sex: Sex of the bird.
- Status: Bird status (PB = pre-breeding; B = breeding).
- Virus_strain: Strain tested (MDNV = Maiden virus, CBNV = Colony B North virus, COYV = Colony virus, BRDV = Broadhaven virus, AMDV = Above Maiden virus).
- Sample_PFUx: Number of PFU or PFU per ml in well with the blood sample.
- Sample_PFU_av: Mean PFU value for the sample.
- Control_PFU_av: Mean PFU value in control wells.