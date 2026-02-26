# Experimental Field Sites.

## Overview
- A field experiment assessing interactions between oak trees (Quercus robur), insect herbivores, and powdery mildew across two UK sites: Hucking (Kent) and Hartshorne (Derbyshire).
- Part of TreeDivNet, a global network of tree diversity experiments.
- Focuses on provenance and mixed-provenance treatments to understand how tree genetics and community context influence pest/pathogen dynamics.

## Study Setting and Plant Material
- Sites and coordinates:
  - Hucking, Kent: 51°17'47.5"N, 0°37'58.2"E
  - Hartshorne, Derbyshire: 52°47'41.1"N, 1°30'58.8"W
- Tree species and provenances:
  - Focal species: Quercus robur (oak)
  - Other broadleaved species planted in the trial: wild cherry, sweet chestnut, ash, and oak
  - Provenances for oak include Local UK (Kent), UK regional Local, French, and Italian (Tuscany and Ravenna) sourced from climate-matched regions or native seed zones
- Experimental design context:
  - Trials include monocultures and various mixtures of provenances and species
  - Provisions for comparing local/adapted stock with climate-matched provenances

## Experimental Design and Treatments
- Plot structure:
  - Monocultures and mixed-provenance plots laid out in two sizes:
    - Monocultures and simple mixtures: 12 m x 12 m plots with 36 trees per plot (4 m spacing)
    - Mixed species/mixed provenance plots: 36 m x 32 m with 288 trees (16 rows x 18 trees)
- Proportion and composition of provenance treatments (for oak):
  - Monocultures of Local, French, and Italian provenances
  - 50:50 and 75:25 mixes (Local with French or Local with Italian)
  - 33:33:33 mix of Local:French:Italian
  - MixSp: mixed species plots containing Local and Italian provenances
- Planting and establishment:
  - Trials established with two-year-old saplings
  - Proximity and arrangement designed to mix different provenances or species within plots, and to avoid identical types adjacent to each other

## Study System and Target Organisms
- Insect herbivore guilds on oak:
  - Gallwasps (cynipid) – specialist on Quercus
  - Leaf miners
  - Leaf manipulators (free-feeding, including generalists and specialists)
- Pathogen:
  - Oak powdery mildew, caused by species of Erysiphe (cryptic complex), with E. alphitoides commonly infecting leaves, E. quercicola infecting buds/leaves
- Temporal dynamics:
  - Insect herbivory peaks on primary shoot leaves in late spring (April–May)
  - Powdery mildew infection occurs on lammas shoots (second flush) from June–August
  - Susceptibility declines after bud burst, allowing clear separation of herbivory vs. mildew observations

## Data Collection and Measurements
- Tree selection and sampling:
  - At each site, nine oak trees of each provenance per plot selected for recording both powdery mildew and herbivory
  - Sampling proceeded from plot core outward
  - Data collected in 2016 (Hucking only) and 2017 (Hucking and Hartshorne)
  - Totals: Hartshorne 411 trees; Hucking 420 (2016) and 416 (2017)
- Powdery mildew (oak) measurements:
  - Timing: August (2016 at Hucking; 2017 at both sites)
  - Sampling: 10 lammas shoots per tree, randomly across height and aspects
  - Scoring: 0–3 infection severity scale based on percent leaf material infected
  - Covariate: lammas shoot length (mm)
- Insect herbivore measurements:
  - Timing: August (2016 at Hucking; 2017 at both sites)
  - Sampling: 10 primary shoots per tree
  - Metrics: counts of leaf mines, galls, and incidences of leaf skeletonisers, leaf rollers, and leaf webbers
  - Covariate: primary shoot length (mm)
- Tree height and apparency:
  - End of August 2017: measured height of focal trees and 27 additional randomly selected trees per plot
  - Apparency index defined as: (Height focal tree − Average plot height) / Average plot height × 100
- Data structure and units:
  - Columns cover site, year, provenance, block, plot, treatment, tree number, shoot lengths, infection/severity scores, insect counts, and height/apparency
  - Units:
    - PShootLength, LShootLength: mm
    - LShootPM (powdery mildew): 0–3 severity scale
    - TreeHeight, MeanHeight: cm
    - Apparency: dimensionless percentage
  - Provisions for describing provenance codes (Local_UK2404, UK provenance 404, Local_Kent, French QR0100, Italy_Tuscany, Italy Ravenna)

## Data Structure: Key Variables
- Site, Year, Provenance, Block, Plot, Treatment, Tree Number
- PShootLength (mean primary shoot length, mm)
- LShootLength (mean lammas shoot length, mm)
- LShootPM (mean oak powdery mildew severity on lammas shoots)
- Leaf.Manip, Leaf.Gallers, Leaf.Miners (counts per tree across 10 shoots)
- TreeHeight (height in cm)
- MeanHeight (average height of 28 trees per plot)
- Apparency (percentage, based on focal vs. plot mean height)

## Data Access and References
- Data are associated with TreeDivNet, a network for tree diversity experiments
- Key literature and methodological references underpinning measurements, phenology, and interpretation of host–pathogen–herbivore interactions (e.g., Ayres & Edwards 1982; Barsoum 2015; Marçais & Desprez-Loustau 2014; Sinclair et al. 2015)

## Data Governance and Relevance for Data Leaders
- Integrated, multi-site provenance and treatment structure enabling robust cross-site analyses
- Rich metadata: site coordinates, plot/block structure, provenance codes, treatment types, and derived covariates
- Clear measurement protocols with standardized scales and covariates, facilitating comparability and reproducibility
- Data management implications:
  - Importance of consistent metadata (provenance codes, plot design, measurement methods)
  - Use of derived covariates (shoot lengths, apparency) for controlling confounding in analyses
  - Facilitation of cross-site collaboration and data integration within a broader data-sharing network (TreeDivNet)

## References (Selected)
- Ayres, Edwards (1982); Barsoum (2015); Bert et al. (2016); Castagneyrol et al. (2018); Desprez-Loustau et al. (2018); Hayward & Stone (2005); Herbert et al. (1999); Marçais & Desprez-Loustau (2014, 2009); Moore et al. (1991); Nieukerken & Johansson (2003); Sinclair et al. (2015)