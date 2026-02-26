# Experimental Field Sites.

## Overview
- Location: Climate Match tree diversity experiment, planted 2011, at two UK sites — Hucking, Kent (South East England) and Hartshorne, Derbyshire (East Midlands).
- Focus: Oak (Quercus robur) provenance experiments within a broader tree-diversity trial (TreeDivNet).
- Provenances examined: Local UK, UK Kent (Local), French, Italian (Tuscany and Ravenna) with climate-matched selections for future UK climates (2050, 2080).
- Design scope: Three experimental blocks per site; multiple provenance treatments (monocultures and mixtures) applied to oak plots, plus some mixed-species plots.

## Experimental Design and Study System
- Treatments for oak plots include:
  - Monocultures of Local, French, Italian provenances
  - 50:50 and 75:25 mixtures (Local:French; Local:Italian)
  - 33:33:33 all-provenance mixture
  - Mixed-species plots containing Local and Italian provenances
- Plot and tree layout:
  - Monocultures and 50/75 mixtures: 12 m x 12 m plots with 36 trees
  - Mixed-species/mixture plots: 36 m x 32 m with 288 trees
  - Planting: Two-year-old saplings, regular spacing to mix different provenances/species
- Sampling focus: Oak-associated insect herbivores and powdery mildew disease
  - Insect guilds: Gall wasps, leaf miners, leaf manipulators (free-feeding herbivores)
  - Pathogen: Powdery mildew (oak Erysiphe spp.), primarily E. alphitoides suspected in UK
- Study scope across sites/years:
  - Powdery mildew and herbivory measured in 2016 (Hucking only) and 2017 (both sites)
  - Sample sizes: 411 trees at Hartshorne; 416–420 trees at Hucking across years (mortality affected counts in 2017)

## Measurements and Data Collected
- Powdery mildew (powdery mildew infection on lammas shoots):
  - Timing: August
  - Sampling: 10 lammas shoots per tree, across height and aspects
  - Scale: 0–3 severity (0 = 0%, 1 = <50%, 2 = 51–75%, 3 = 76–100%)
  - Covariate: Lammas shoot length (mm)
- Insect herbivores:
  - Timing: August
  - Sampling: 10 primary shoots per tree
  - Metrics: Counts of leaf mines, galls, and incidences of leaf skeletonisers, leaf rollers, leaf webbers
  - Covariate: Primary shoot length (mm)
- Tree height and apparency:
  - Height: End of August 2017 for focal trees; additional 27 random trees per plot
  - Apparency index: (Height of focal Q. robur − Average height in plot) / Average height in plot × 100
- Data collection context:
  - Sites: Hartshorne (Derbyshire) and Hucking (Kent)
  - Years: 2016 and 2017 (as above)
  - Proxies used: Covariates (PShootLength, LShootLength, TreeHeight, MeanHeight) to adjust for size effects

## Data Structure and Variables
- Data frame columns and meanings:
  - Site: Hartshorne or Hucking
  - Year: 2016 or 2017
  - Provenance: Local_UK2404, UK_provenance_404, Local_Kent, French, Italy_Tuscany, Italy_Ravenna
  - Block: Experimental block (nested within site)
  - Plot: Plot (nested within block, within site)
  - Treatment: Diversity treatment code (Mono; P1P2_50; P1P2_75; P1P3_50; P1P3_75; 30:33:33; MixSp)
  - Tree Number: Tree number within the plot
  - PShootLength: Mean primary shoot length (mm) across 10 shoots
  - LShootLength: Mean lammas shoot length (mm) across 10 shoots
  - LShootPM: Mean powdery mildew infection score across 10 lammas shoots
  - Leaf.Manip: Sum of leaf manipulator abundance across 10 shoots
  - Leaf.Gallers: Sum of leaf galler abundance across 10 shoots
  - Leaf.Miners: Sum of leaf miner abundance across 10 shoots
  - TreeHeight: Height of focal tree (cm)
  - MeanHeight: Average height of 28 trees per plot (including focal)
  - Apparency: Apparency index as defined above
- Provenance and treatment codes provide a structured means to analyze provenance effects, mixtures, and their interaction with pests and diseases.

## Data Use and Context
- The dataset enables analyses of how tree provenance and mixture designs influence susceptibility to powdery mildew and herbivory on oak.
- Includes standardized measurements and covariates to account for tree size and vertical positioning, facilitating cross-site comparisons.
- References provide methodological grounding for disease and herbivore scoring and relevant ecological context.