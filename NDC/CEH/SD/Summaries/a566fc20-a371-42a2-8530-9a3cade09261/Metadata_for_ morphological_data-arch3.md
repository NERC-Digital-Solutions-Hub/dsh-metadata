# Metadata for morphological data

## Overview
- Describes three data sets of morphometric data for threespine sticklebacks, including associated photographs for the third data set.
- Each TPS file contains x,y shape coordinates for 32 landmarks per specimen; landmarks 23–32 are semi-landmarks requiring special handling.
- Data can be opened in various morphometrics packages or viewed as text.
- Cases involve wild-caught samples and lab-reared (F1/F2) generations from multiple lakes, enabling comparisons across natural and controlled environments.

## Data sets and structure
- Data set 1: curveAppendedWildThenLabData.tps
  - Accompanying file: data file 1 categories.csv
  - Composition: first 331 specimens wild-caught, next 320 lab-reared
  - Accompanying variables: population (precise codes like mw, mc, gts, cs, sw, sc, stc, stw, ac, aw, rkc), thermal habitat, source (lab or wild), and pair
  - Population origins listed: Myvatn, Grettislaug, Gardsvatn, Saudarkrokur, Steinstaddur, Ashildarholtsvatn, Reykholt
- Data set 2: f2_ecomorph_crosses_temp_treatments.tps
  - Accompanying file: f2_ecomorph_crosses_temp_treatments.csv
  - Composition: F2 generation, lab-reared across two temperatures (12°C and 18°C)
  - Variables: populations, treatments in F1 and F2, pair, population code, individual ID, and experimental unit (EU)
- Data set 3
  - Comprised of jpeg images of F2 hybrids organized into master folders by population: SKR (Saudarkrokur), MYV (Myvatn), ASNH (Ashildarholtsvatn)
  - Within each, subfolders named by temperature treatment (e.g., 12at12, 12at18, 18at12, 18at18), reflecting parental generation temperature and current generation temperature
  - Contains corresponding TPS data files with the same landmark set as above

## Data formats and accessibility
- Landmark data: 32 coordinates per specimen (x,y), stored in TPS format; can be processed in morphometrics software or accessed as plain text.
- Metadata: accompanying CSV files provide population, thermal habitat, origin (lab or wild), and pairing information to complement the morphometric data.
- Photos: corresponding images available for the third dataset to accompany the morphometric data.

## Metadata details and provenance
- Field collection sites (from lakes and ponds) include Ashildarholtsvatn, Myvatn, Gardsvatn, Grettislaug, Saudarkrokur, Steinstaddur, Reykholt; exact locations and chemistry measures are documented in supplementary Table 1.

## Relevance for monitoring frameworks
- Offers multiple generations and temperature treatments to study environmental impacts on morphology, enabling cross-study comparisons if standardized.
- Demonstrates transparent data sharing with explicit metadata and open formats (TPS, CSV, JPEG), aiding reproducibility and integration into monitoring dashboards.
- Highlights practical governance aspects: consistent naming schemes, preservation of raw coordinates, and explicit linkage between metadata and morphometric data.

## Considerations for data governance and use
- Standardization: harmonize population codes, treatment labels, and file naming to facilitate interoperability across projects.
- Metadata completeness: ensure all datasets include clear definitions for variables (e.g., population codes, habitat categories, EU, and pairings).
- Data access and formats: maintain availability of both raw TPS data and human-readable metadata; manage image data alongside numerical data.
- Data quality and processing: semi-landmarks require careful analysis; establish guidelines for their handling and documentation of processing steps.
- Long-term stewardship: ensure that data formats remain readable and that provenance (sampling, rearing conditions, and timing) is well documented for future monitoring and re-use.