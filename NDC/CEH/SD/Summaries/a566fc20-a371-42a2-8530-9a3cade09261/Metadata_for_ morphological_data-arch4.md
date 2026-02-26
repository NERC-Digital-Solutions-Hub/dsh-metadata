# Metadata for morphological data

- Three main sets of files form the dataset, with corresponding photographs available for the third set.
- For each specimen, 32 landmarks are collected; landmarks 23–32 are semi-landmarks requiring special handling during analysis.
- Landmarks are defined on a fish and can be opened in various morphometrics packages or viewed as plain text.

## Data sets and contents

- Data set 1: curveAppendedWildThenLabData.tps
  - Accompanying file: data file 1 categories.csv
  - Composition: wild-caught individuals followed by lab-reared F1s; the first 331 specimens are wild-caught, the next 320 are lab-reared.
  - Image names include population information.
  - The column 'popprecise' encodes population origin and habitat (examples: mw = Myvatn warm, mc = Myvatn cold, gts = Grettislaug, cs = Gardsvatn, sw = Saudarkrokur warm, sc = Saudarkrokur cold, stc = Steinstaddur cold, stw = Steinstaddur warm, ac = Ashildarholtsvatn cold, aw = Ashildarholtsvatn warm, rkrc = Reykholt ambient, rkrw = Reykholt geothermal).

- Data set 2: f2_ecomorph_crosses_temp_treatments.tps
  - Accompanying file: variables f2_ecomorph_crosses_temp_treatments.csv
  - Source: F2 generation lab-reared sticklebacks reared under two temperatures (12°C and 18°C).
  - Metadata includes population, treatments across F1 and F2 generations, along with pair, population, and thermal ecotype; each fish has an individual ID and an experimental unit (EU).

- Data set 3: Morphological data and images by treatment and population
  - Contains multiple JPEG files of F2 hybrid fish organized in master folders named by population: SKR (Saudarkrokur), MYV (Myvatn), ASNH (Ashildarholtsvatn).
  - Within each population folder are subfolders containing JPEG photos and corresponding tps data files with the same landmark schema as above.
  - Subfolders are named by temperature treatment: 12at12, 12at18, 18at12, 18at18.
    - 12at12, for example, denotes two generations at 12°C where both F1 parents and the current generation experienced 12°C. The other combinations follow the same convention.

## Landmarks and analysis considerations

- A total of 32 landmarks per specimen; semi-landmarks (23–32) require specialized processing in analyses.
- Landmark coordinates are stored in TPS format and can be analyzed in morphometrics software or viewed as text for verification.

## Metadata, provenance, and accessibility

- The data are organized with accompanying metadata files (CSV) that map populations, habitats, and treatment conditions, enabling discoverability and re-use.
- Population and habitat codes provide a clear lineage and environmental context (ambient vs. geothermal; warm vs. cold).
- The three datasets collectively enable comparisons across wild vs. lab-reared conditions, different thermal treatments, and multiple lakes/ponds, supporting cross-population and eco-morph comparisons.

## Relevance for data leadership and governance

- Clear data organization across datasets and a consistent landmark schema support data discoverability, interoperability, and reuse.
- The presence of metadata files for each dataset facilitates appropriate data stewardship, research planning, and prioritization of analyses by user needs.
- The dataset design enables co-ownership and collaboration across research groups by standardizing population codes, habitat context, and treatment design.
- Potential data access considerations include navigating folder structures for dataset 3 and ensuring appropriate handling of semi-landmarks in statistical workflows.