# Metadata for morphological data

## Overview
- Morphological data for threespine sticklebacks collected across multiple lakes and ponds, organized into three data sets.
- Each specimen has 32 landmarks; landmarks 23–32 are semi-landmarks that require special consideration during analysis.
- Data can be opened in morphometrics software or as plain text; accompanying data files provide contextual variables.

## Data Sets at a glance

- Data set 1: curveAppendedWildThenLabData.tps
  - Accompanying file: data file 1 categories.csv
  - Composition: wild-caught individuals followed by lab-reared F1 generation; first 331 specimens are wild-caught, next 320 are lab-reared.
  - Population information is encoded in image names.
  - Variables in categories.csv include population, thermal habitat, lab or wild status, and pair.
  - Population codes include: mw (Myvatn warm), mc (Myvatn cold), gts (Grettislaug), cs (Gardsvatn), sw (Saudarkrokur warm), sc (Saudarkrokur cold), stc (Steinstaddur cold), stw (Steinstaddur warm), ac (Ashildarholtsvatn cold), aw (Ashildarholtsvatn warm), rkc (Reykholt ambient).

- Data set 2: f2_ecomorph_crosses_temp_treatments.tps
  - Accompanying file: variables f2_ecomorph_crosses_temp_treatments.csv
  - Composition: morphological data from F2 generation lab-reared sticklebacks reared under two temperatures (12°C and 18°C).
  - Variables include pair, population (pop), thermal ecotype, individual ID, and experimental unit (EU).

- Data set 3: image and landmark collection
  - Contents: JPEG images of F2 hybrid fish organized in folders by population/treatment.
  - Master folders: SKR (Saudarkrokur), MYV (Myvatn), ASNH (Ashildarholtsvatn).
  - Subfolders named by temperature treatment: 12at12, 12at18, 18at12, 18at18 (denoting parental and current-generation temperatures).

## Landmarks and analysis considerations
- Each specimen has 32 landmarks; landmarks 23–32 are semi-landmarks, requiring special handling during analysis.
- Landmark data (tps format) can be used directly in morphometrics software or opened as text for inspection.
- Dataset 3 provides corresponding images to aid in visual interpretation alongside the tps landmark data.

## Sampling locations and habitat context
- Fish were captured or bred from lakes/ponds with distinct thermal habitats:
  - Ashildarholtsvatn: AshnC = ambient habitat, AshnW = geothermal habitat
  - Myvatn: MyvC = ambient, MyvW = geothermal
  - Gardsvatn: CSWY = ambient
  - Grettislaug: GTS = geothermal
  - Saudarkrokur: SkrC = ambient, SkrW = geothermal
  - Steinstaddur: stnstW = geothermal, stnstC = ambient
  - Reykholt: rkrc = ambient, rkrw = geothermal
- Supplementary Table 1 provides exact locations and water chemistry measures.

## Relevance for environmental monitoring and data use
- The standardized, multi-factor design (wild vs. lab, ambient vs. geothermal, and temperature treatments) supports cross-study comparisons of morphology under environmental variation.
- Data are structured to enable verification, quality assurance, and transformation into outputs suitable for monitoring environmental health and policy performance over time.
- Accompanying metadata and population codes facilitate reproducibility and integration with other datasets, aiding transparency and broader access to underlying data.