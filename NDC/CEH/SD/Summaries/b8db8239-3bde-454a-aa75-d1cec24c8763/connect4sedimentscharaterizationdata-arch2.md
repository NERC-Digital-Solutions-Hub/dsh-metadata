# SEDIMENTS CHARACTERISATION DATA FOR CONNECT4 PROJECT

- The dataset compiles sedimentological and geochemical analyses from sediment cores collected across four countries (Botswana, South Africa, Zimbabwe, Mozambique) for the Connect4 project.
- Each country section lists the number of files/cores, core identifiers, location details, depths, and the types of analyses performed (grain size distribution, organic matter content, LOI, and various geochemical elements).
- Sampling and data handling follow a consistent workflow: push corer collection from shore or boat, 50 mm diameter cores, storage at 4 °C, halved cores photographed and sub-sampled, and analyses focused on particle size, organic matter, and heavy metals (e.g., Cr, Fe, Ni, Cu, Zn, Pb; with additional elements in some cores).
- Quality control notes highlight potential measurement errors, data that fall below detection limits, negative values in CSVs, large standard deviations in some measurements, and incomplete geochemical data across certain cores.
- Data structure across cores typically includes depth columns, LOI calculations, organic matter percentages, grain size distributions in micrometres, and geochemical data (ppm) for selected elements, with some cores showing replicates and statistical summaries (average, standard deviation, relative standard deviation).

## Botswana

- Data folder contains 7 core files from Botswana dams.
- Cores include GC1 (Gaborone, 146 cm), GC2 (Gaborone, 81 cm), L11 (Lobatse, 58 cm), S5 (Shashe, 33 cm), S6 (Shashe, 92 cm), S7 (Shashe, 113 cm), S8 (Shashe, 84 cm).
- Content per core:
  - GC1/GC2: particle size distribution, organic matter content; no geochemical analysis for GC1/GC2.
  - L11, S5, S6, S7: particle size distribution, LOI, organic matter; varying geochemical data availability (S8 includes extensive geochemical results across multiple elements with replicates).
- Data structure details emphasize depth, LOI calculations, OM (%), grain size (micrometres), and geochemical data (ppm) where present.

## South Africa

- Data folder contains 10 core files from South Africa dams.
- Cores include H1 (Houtrivier, 51 cm), H2 (50 cm), H3 (70 cm), H5 (78 cm), M4 (33 cm), M7 (58 cm), M8 (33 cm), N4 (40 cm), N5 (60 cm), N7 (27 cm).
- Content per core:
  - H1/H2/H3: particle size distribution, LOI, organic matter; H2 includes geochemical data but notes no raw data; H3 contains geochemical raw data.
  - H5: includes particle size, LOI, OM; partial particle size data missing in some ranges.
  - M4: particle size and LOI; no geochemical data.
  - M7/M8: particle size, OM; M8 includes multiple geochemical datasets with average, SD, replicates for several elements.
  - N4/N5/N7: particle size, OM, LOI; geochemical results for multiple elements with replicate statistics where applicable.
- Data structure variations reflect differences in available data (some cores include full geochemical tables; others are limited to grain size and LOI).

## Zimbabwe

- Data folder contains 10 core files from Zimbabwe dams.
- Cores include B1 (Ripple Creek, 48 cm), B3 (Ripple Creek, 12 cm), B5 (Ripple Creek, 9 cm), B6 (Ripple Creek, 12 cm), Z1 (Zhovhe, 13 cm), Z2 (Zhovhe, 25 cm), Z3 (Zhovhe, 75 cm), Z5 (Zhovhe, 19 cm), Z6 (Zhovhe, 24 cm), Ripple Creek core set.
- Content per core:
  - Ripple Creek B1/B3/B5/B6: LOI, OM, grain size; some cores include geochemical analyses (ppm for trace elements) with full data structures for As, Cr, Cu, Mn, Ni, Pb, Zn.
  - Z1/Z2/Z3/Z5/Z6: similar structure with LOI, OM, grain size, and geochemical datasets; Z3/Z5/Z6 include raw geochemical data in some sections.
- Data structure details emphasize depth, LOI calculations, OM (%), grain size (micrometres), and geochemical results (ppm) with replicates and statistics where provided.

## Mozambique

- Data folder contains 10 core files from Mozambique dams.
- Cores include MA1 (67 cm), MA2 (26 cm), MA3 (26 cm), MA4 (38 cm), MA5 (49 cm) with MA5B (37 cm), MA7 (23 cm), MA10 (57 cm), OX1 (34 cm), OX2 (35 cm).
- Content per core:
  - MA1: grain size and OM; OM data partially missing (gaps noted); no geochemical analysis.
  - MA2/MA3/MA4/MA5/MA5B/MA7/MA10: grain size and LOI; varying presence of geochemical data; MA10 includes XRF data in addition to LOI/grain size with some missing sample intervals.
  - OX1/OX2: grain size and OM; no geochemical analysis reported for either core.
- Data structure details highlight depth, LOI, OM (%), grain size (micrometres), and, where present, geochemical data or XRF data; some cores include raw geochemical data or XRF datasets, and some have missing intervals.

## Sampling techniques (common across regions)

- Eight to ten cores per region were collected using a push corer with extension rods from shore or small boats.
- Cores are 50 mm in diameter, stored at 4 °C for water retention.
- Cores are split, photographed, and sub-sampled for grain size and geochemical analysis.
- Measured parameters consistently include particle size distribution, organic matter content, and concentrations of heavy metals (Cr, Fe, Ni, Cu, Zn, Pb), with additional elements or raw data included where available.

## Data structure and quality control (focus for Analysts Monitoring the Environment)

- Core data structures typically include:
  - Depth of sample (Column A)
  - LOI calculations (Columns B-H or equivalent)
  - Organic matter (%)
  - Grain size distribution (micrometres)
  - Geochemical data (ppm) for multiple elements, with averages, standard deviations, relative standard deviations, and replicates where provided.
- Quality control notes:
  - Potential measurement errors due to field notes or instrument malfunctions.
  - Some values fall below detection limits; negative values may appear in CSV exports.
  - Some cores lack complete geochemical analyses or raw data; missing intervals noted (e.g., in Mozambique MA1, MA10, OX1, OX2).
  - Large standard deviation ranges in some measurements require cautious interpretation.

## Key observations for data use and accessibility

- The dataset provides a standardized framework of metadata and core-specific data structures that facilitate cross-country environmental health monitoring and temporal policy performance assessments.
- Variability in data completeness across cores offers opportunities to link datasets with external environmental data or to target data gaps for future collection.
- Given the Focus on data accessibility, the descriptions imply the need to store and potentially upload datasets to appropriate portals, aligning with the aim of enabling access to underlying data used in final outputs.