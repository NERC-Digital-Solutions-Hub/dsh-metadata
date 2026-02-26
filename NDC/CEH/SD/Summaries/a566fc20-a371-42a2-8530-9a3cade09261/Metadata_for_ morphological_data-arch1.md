# Metadata for morphological data

- Overview
  - A morphometrics dataset comprising three sets of files with corresponding photographs for the third set.
  - Each tps file contains x,y shape coordinates for 32 landmarks per specimen; landmarks 23–32 are semi-landmarks requiring special handling.
  - Data supports analysis of morphological variation (shape) across populations, habitats, and temperature treatments.

- Data set 1: curveAppendedWildThenLabData.tps
  - Accompanying file: data file 1 categories.csv
  - Composition: wild-caught individuals followed by lab-reared F1 individuals (first 331 wild, next 320 lab-reared).
  - Image names encode population information.
  - categories.csv provides: population, thermal habitat, lab/wild status, and pairing information.
  - 'popprecise' column lists population codes (examples include mw/Myvatn warm, mc/Myvatn cold, gts/Grettislaug, cs/Gardsvatn, sw/Saudarkrokur warm, sc/Saudarkrokur cold, stc/Steinstaddur cold, stw/Steinstaddur warm, ac/Ashildarholtsvatn cold, aw/Ashildarholtsvatn warm, rkc/Reykholt ambient, rkrw/Reykholt geothermal).

- Data set 2: f2_ecomorph_crosses_temp_treatments.tps
  - Accompanying file: variables f2_ecomorph_crosses_temp_treatments.csv
  - Description: morphological data from F2 generation lab-reared sticklebacks reared under two temperatures (12°C and 18°C).
  - Variables include: population, thermal ecotype, pair, individual ID, and experimental unit (EU).

- Data set 3: F2 hybrids and treatments (folders with images and data)
  - Master folders: SKR, MYV, ASNH corresponding to Saudarkrokur, Myvatn, and Ashildarholtsvatn populations.
  - Within each folder: subfolders for temperature treatments; contain JPEG photos and tps data files with the same landmarks as above.
  - Folder naming by temperature treatment: 12at12, 12at18, 18at12, 18at18, indicating generational exposure (F1 parents and current generation), with temperatures 12°C or 18°C.

- Specimens, locations, and metadata
  - Lakes and ponds used: Ashildarholtsvatn, Myvatn, Gardsvatn, Grettislaug, Saudarkrokur, Steinstaddur, Reykholt (see supp Table 1 for exact locations and chemistry measures).
  - Habitat codes indicate ambient vs geothermal environments (e.g., AshnC ambient, AshnW geothermal; MyvC ambient, MyvW geothermal; rkrc ambient, rkrw geothermal, etc.).

- Data formats and accessibility
  - Landmark data can be opened in various morphometrics software or as plain text.
  - 32 landmarks per specimen; semi-landmarks (23–32) require special processing.
  - Data links across sets allow analyses of wild vs lab-reared individuals, temperature treatments, and inter-population comparisons.
  - Supp Table 1 provides location and chemical measures relevant for ecological context.

- Potential uses for analysts
  - Identify morphological correlations with habitat type (ambient vs geothermal) and thermal treatments.
  - Compare wild and lab-reared phenotypes and track effects across generations.
  - Analyze cross-population (ecotype) differences using F2 data and temperature treatments.
  - Build predictive models of shape variation under environmental conditions; merge datasets while accounting for the 32-landmark structure and semi-landmarks.