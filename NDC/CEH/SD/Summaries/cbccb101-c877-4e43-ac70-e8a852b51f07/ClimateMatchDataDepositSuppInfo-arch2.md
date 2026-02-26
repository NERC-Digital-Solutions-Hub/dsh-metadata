# Experimental Field Sites

- This study examines oak (Quercus robur) herbivory and powdery mildew within a climate-matched, provenance-diversity trial that is part of TreeDivNet, a global network of tree diversity experiments.
- Objectives align with environmental monitoring aims: document biotic stress factors on a standardised framework to enable assessment of environmental health and policy-relevant performance over time.

## Location, Design, and Trial Setup

- Sites: two UK locations – Hucking, Kent (SE England) and Hartshorne, Derbyshire (East Midlands).
- Trial framework: three experimental blocks per site; plots within blocks; focus on treatments containing oak among multiple species.
- Plot types and sizes:
  - Oak provenance monocultures and mixed-provenance plots (12 m x 12 m) with 36 trees per plot.
  - Mixed-species plots (36 x 32 m) containing multiple provenances of oak and other species.
- Plant material: two-year-old saplings of oak (Quercus robur) plus other broadleaved species; climate- and locality-informed provenance selections.
- Sampling years: 2016 (Hucking only), 2017 (both sites); 9 oak trees per provenance per plot were monitored.

## Provenances Observed

- Local_UK2404
- UK provenance, region 404 (Local_Kent)
- French provenance (QR0100 North West)
- Italian Provenances:
  - Italy_Tuscany (San Rossore)
  - Italy_Ravenna (Ravenna)
- Note: Due to geographic differences between sites, oak provenances varied by site with only French provenance common to both.

## Measured Biotic Factors and Covariates

- Powdery mildew on oak:
  - Target: lammas shoots (second flush) in August.
  - Measurement: infection scored on a 0–3 scale (0 = 0%, 1 = <50%, 2 = 51–75%, 3 = 76–100% infected).
  - Covariate: lammas shoot length (mm).
- Insect herbivores:
  - Target: primary shoots in August.
  - Measurements: counts of leaf mines, galls (on leaves and buds), and incidences of leaf skeletonisers, leaf rollers, and leaf webbers.
  - Covariate: primary shoot length (mm).
- Tree apparency and size:
  - End-of-season height for sampled trees and 27 additional randomly chosen trees per plot.
  - Apparency index calculated as: (height of focal tree – plot average height) / plot average height × 100.

## Data Structure and Variables

- Site: Hartshorne or Hucking.
- Year: 2016 or 2017.
- Provenance: coded provenance for each surveyed tree (e.g., Local_UK2404, Local_Kent, French, Italy_Tuscany, Italy_Ravenna).
- Block, Plot: hierarchical plot identifiers within site.
- Treatment: provenance-based and mixed-provenance schemes (e.g., Mono, P1P2_50, P1P2_75, P1P3_50, P1P3_75, Thirty-33:33:33, MixSp).
- Tree Number: within-plot tree identifier.
- PShootLength: mean primary shoot length (mm).
- LShootLength: mean lammas shoot length (mm).
- LShootPM: mean powdery mildew infection score on lammas shoots.
- Leaf.Manip: total abundance of leaf manipulators across sampled shoots.
- Leaf.Gallers: total abundance of gallwasps across sampled shoots.
- Leaf.Miners: total abundance of leaf miners across sampled shoots.
- TreeHeight: height of focal tree (cm).
- MeanHeight: average height of 28-tree sample per plot.
- Apparency: calculated apparency index for the focal tree.

## Data Collection and Quality Context

- Data collection followed standardised protocols for assessing insect herbivory and fungal infection, with covariates (shoot length, tree height) incorporated to account for size-related effects.
- Sampling was designed to capture spatial and temporal variation across two sites and multiple provenances, supporting analyses of provenance, diversity, and environmental interactions on pest and disease dynamics.

## Context for Analysis and Use

- Data support analyses of how tree provenance and mixed-planting treatments influence oak pest pressures and powdery mildew risk under varying UK climates.
- Outputs suitable for reporting include clear formats such as datasets and charts; data are structured for integration into dashboards and maps to monitor environmental health over time.
- The dataset aligns with broader monitoring aims of enabling data access and re-use, and contributes to environmental policy performance evaluation within a standardised, repeatable framework.