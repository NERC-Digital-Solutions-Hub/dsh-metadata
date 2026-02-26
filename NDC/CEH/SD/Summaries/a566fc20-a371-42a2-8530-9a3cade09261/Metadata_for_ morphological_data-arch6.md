# Metadata for morphological data

- Overview
  - Describes three data sets of morphometric data (landmark-based) for threespine sticklebacks.
  - Data types include tps landmark coordinate files, accompanying CSV metadata, and JPEG photographs (for the third data set).
  - Landmarks: 32 per specimen; landmarks 23–32 are semi-landmarks requiring special treatment during analysis.
  - Specimens originate from multiple lakes and ponds, with ambient and geothermal habitats represented.

- Datasets at a glance
  - Data set 1: curveAppendedWildThenLabData.tps
    - Accompanying file: data file 1 categories.csv
    - Structure: first 331 specimens wild-caught, next 320 lab-reared (F1). Image names encode population.
    - Metadata captured: population, thermal habitat, lab/wild status, and pair (with precise population codes, e.g., mw=Myvatn warm, mc=Myvatn cold, gts=Grettislaug, etc.).
  - Data set 2: f2_ecomorph_crosses_temp_treatments.tps
    - Accompanying file: variables f2_ecomorph_crosses_temp_treatments.csv
    - Details: morphometrics from F2 generation lab-reared under two temperatures (12°C and 18°C).
    - Metadata included: pair, population (pop), thermal ecotype, individual ID, and experimental unit (EU).
  - Data set 3: F2 hybrid data with images and tps data
    - Content: JPEG photos plus tps data files containing the same landmark set.
    - Organization: master folders SKR (Saudarkrokur), MYV (Myvatn), ASNH (Ashildarholtsvatn).
    - Within each population folder: subfolders named by temperature treatment (12at12, 12at18, 18at12, 18at18) describing the temperature history of parental generations and the current generation.

- Landmarks and semi-landmarks
  - 32 landmarks per specimen; semi-landmarks (23–32) require specialized processing during morphometric analysis.

- Populations and sampling context
  - Lakes/ponds and habitat labels:
    - Ashildarholtsvatn: AshnC (ambient), AshnW (geothermal)
    - Myvatn: MyvC (ambient), MyvW (geothermal)
    - Gardsvatn: CSWY (ambient)
    - Grettislaug: GTS (geothermal)
    - Saudarkrokur: SkrC (ambient), SkrW (geothermal)
    - Steinstaddur: stnstW (geothermal), stnstC (ambient)
    - Reykholt: rkrc (ambient), rkrw (geothermal)
  - The population codes are detailed in Data set 1’s categories.csv (e.g., mw, mc, gts, cs, sw, sc, stc, stw, ac, aw, rkc, rkrw).

- Data formats and accessibility
  - File types:
    - .tps: coordinate landmark data (can be opened by morphometrics software or as text).
    - .csv: metadata and experimental design information.
    - .jpg/.jpeg: photographs (dataset 3).
  - The third data set includes photographs corresponding to the landmark data; photographs are provided for visual reference of specimens.

- Usage implications and potential analyses
  - Enables cross-condition morphometric comparisons:
    - Wild vs. lab-reared (Data set 1) across multiple populations and habitats.
    - Temperature treatments across generations (Data sets 2 and 3) to study plasticity and heritable shape changes.
    - Hybrid and ecomorph comparisons across populations (Data set 2 and 3).
  - Suitable analyses:
    - Generalized Procrustes analysis, shape variation assessment, and allometry studies.
    - PCA/cluster analyses to identify population- or habitat-associated shape differences.
    - Semilandmark processing to analyze curvature and outlines, with careful handling of the semi-landmarks (23–32).
  - Data integration possibilities:
    - Combine population/habitat metadata with morphometric measurements for exploratory data products (dashboards, reports) to support policy or research discussions.
    - Cross-reference temperature history (treatments) with morphological outcomes to evaluate plastic responses.

- Practical notes
  - Supplementary Table 1 (not provided here) contains exact locations and water chemistry measures for the sampled sites.
  - Clear labeling conventions for populations and temperature histories are essential when merging across datasets (e.g., 12at18 vs. 18at12 in Data set 3).