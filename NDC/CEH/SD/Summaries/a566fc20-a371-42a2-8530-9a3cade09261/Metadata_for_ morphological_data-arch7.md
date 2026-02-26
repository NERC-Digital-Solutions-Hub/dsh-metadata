# Metadata for morphological data

## Overview
- Three data sets of morphometric data for threespine sticklebacks, with corresponding photos for the third set.
- Each specimen has 32 landmarks; landmarks 23–32 are semi-landmarks requiring specialized handling.
- Specimens originate from lakes and ponds listed in the document; exact locations and chemistry measures are in Supplement Table 1.
- Data can be used in morphometrics packages or opened as text, enabling integration with GIS for spatial analysis of populations and habitats.

## Data sets

- Data set 1: curveAppendedWildThenLabData.tps
  - Accompanying file: data file 1 categories.csv
  - Content: Wild-caught and F1 lab-reared threespine sticklebacks; first 331 are wild, next 320 lab-reared.
  - Image names encode population information.
  - Metadata in categories.csv includes: population, thermal habitat, lab or wild status, and pair.
  - The column 'popprecise' specifies the exact population codes (e.g., mw, mc, gts, cs, sw, sc, stc, stw, ac, aw, rkc).

- Data set 2: f2_ecomorph_crosses_temp_treatments.tps
  - Accompanying file: variables f2_ecomorph_crosses_temp_treatments.csv
  - Content: Morphology from F2 lab-reared sticklebacks reared under two temperatures (12°C and 18°C).
  - Metadata includes: population, treatment in F1 and F2, pair, EU (experimental unit), and individual ID.

- Data set 3: Morphology images and data (folders)
  - Located in master folders SKR (Saudarkrokur), MYV (Myvatn), and ASNH (Ashildarholtsvatn).
  - Subfolders named by temperature treatment: 12at12, 12at18, 18at12, 18at18.
  - Each folder contains JPEG images and corresponding TPS data files with the same landmarks as above.

## Landmarks and analysis notes
- 32 landmarks captured per specimen.
- Landmarks 23–32 are semi-landmarks and require special consideration during analysis.

## Data provenance and sampling
- Locations and habitat data refer to lakes/ponds including:
  - Ashildarholtsvatn (AshnC ambient, AshnW geothermal)
  - Myvatn (MyvC ambient, MyvW geothermal)
  - Gardsvatn (CSWY ambient)
  - Grettislaug (GTS geothermal)
  - Saudarkrokur (SkrC ambient, SkrW geothermal)
  - Steinstaddur (stnstW geothermal, stnstC ambient)
  - Reykholt (rkrc ambient, rkrw geothermal)

## Data formats and access
- TPS files: contain x,y coordinates; readable by multiple morphometrics tools or as plain text.
- JPEG files: accompany the 3rd data set for visual references.
- CSV files: provide population, habitat, treatment, lab/wild status, and other metadata necessary for analysis and data linking.

## GIS-analytical opportunities and integration
- Link specimen morphometrics to geographic origins by associating population codes with lake coordinates.
- Use habitat type (ambient vs geothermal) and temperature treatment as spatially-referenced attributes for comparative mapping.
- Combine with environmental layers (chemistry measures from Supp Table 1) to explore spatial morphometric variation.
- Leverage semi-landmarks with appropriate alignment to study shape changes across populations and treatments.

## Important considerations for use and quality
- Semi-landmarks (23–32) require careful processing to ensure meaningful comparisons.
- Data are distributed across three datasets with separate file types; ensure consistent identifiers (e.g., popprecise) when joining data.
- Distinguish wild-caught vs lab-reared individuals to avoid confounding analyses unless explicitly intended.