# LAC Project Sediment Core Multi-proxy Datasets

- A set of seven CSV datasets from the LAC project containing multi-proxy sediment core data across several lakes.
- Datasets cover 1 cm and 2 cm resolution cores for different lakes; core sequences collected from the deepest part of each lake; depth profiles constructed from overlapping sections with running depth definitions.
- Proxies include LOI (loss on ignition), diatoms, biogenic silica, isotopes, XRF geochemistry, macrofossils, chironomids, cladocerans, pigments, and pollen, among others.
- Data are intended for GIS-based visualization and analysis of sedimentary proxies to support interpretation of past environmental change.

## Datasets Included

- LAC_Ruppert_1cm_dataset.csv
- LAC_Ruppert_2cm_dataset.csv
- LAC_WBP_dataset.csv
- LAC_Nor1_dataset.csv
- LAC_Nor3_dataset.csv
- LAC_AT2_1cm_dataset.csv
- LAC_AT2_2cm_dataset.csv

- Datasets share authorship from multiple institutions (primarily Geography and Environment, University of Southampton; University College London; University of Nottingham; Loughborough University; others) with detailed affiliations listed in the source.

## Sampling Design and Core Processing

- One sediment sequence per lake, collected at the deepest part, using overlapping drives.
- Cores subjected to XRF scanning before subsampling; subsampling performed to 1 cm or 2 cm resolution depending on proxy (macrofossils, chironomids, and Cladocera at 2 cm; most analyses at 1 cm; XRF at 200–400 μm).
- Surface of cores cleaned before division; continuous 1 cm and 2 cm sections prepared for analyses.
- Running depth profiles (top and bottom) created by correlating LOI profiles across overlapping sections.
- Some lake sequences were not completely analyzed for all proxies.

## Proxies and Analytical Methods

- LOI (Loss on Ignition): 1 cm resolution; determines organic matter and carbonate contents; densities and weights recorded.
- Diatoms: fossil diatom preparation and counting with species-level identification where possible; counts converted to percent abundance and concentration per gram dry mass.
- Biogenic Silica (BSi): dissolved silica measured via alkaline digestion; concentrations estimated and validated with reference standards.
- Isotopes: δ13C and δ15N, plus %C and %N; standardized against known references; isotope measurements via BEIF facility.
- XRF Scanning: element counts (cps) normalized by total cps to produce 1 cm-binned element patterns (e.g., Ca, Fe, Ti, Zr, Fe:Mn).
- Macrofossils: counts and abundances of plant and animal macrofossils (size fractions >400 μm and >200 μm); taxonomic identifications supported by literature and references.
- Chironomids: preparation and identification of head capsules and invertebrate remains; counts and volumes recorded for abundance and flux analyses.
- Cladocera: processing and identification; counts and volumes recorded for abundance and concentration calculations.
- Pigments: HPLC measurement of algal pigments (Chl a, Chl b, carotenoids, and derived pigments) for composition of algal communities.
- Pollen: standard pollen preparation; counts and percent abundances (taxonomy to family/species where possible).
- Geochemistry: absolute and relative concentrations (e.g., Biogenic Si, C, N, d13C, d15N, Fe/Mn ratios, etc.) with data normalized for compatibility with 1 cm sequencing.
- Data are provided with detailed variable definitions and units (see Table 2 in the source for complete column-by-column definitions).

## Data Format, Structure, and Units

- Stored as comma-separated values (CSV) with depth-related variables such as:
  - Running_top_cm: top depth of the section (cm)
  - Running_bot_cm: bottom depth of the section (cm)
  - SubID: unique sample barcode
- Proxies provided as concentrations, percentages, or counts per unit mass/volume, with explicit units (e.g., %dw, g/cm3, valves/g dw x 10^8, nmol/g organic mass, % abundance, count/100 ml, etc.).
- Extensive tables of column headings, abbreviations, and units are available in Table 2 of the source document; data files include many proxy-specific fields (e.g., LOI, Dtm/Chrys, Diatom_conc, δ13C, δ15N, Bio_Si, etc.).

## Quality Control and Data Provenance

- Multiple quality checks implemented as data are generated; comparisons against detection limits and prior samples; use of blanks and reference standards in isotopic and geochemical analyses.
- XRF data normalized to total counts to minimize variability; cross-core section comparisons where cores overlap.
- Taxonomic identifications cross-validated with established keys and references; uncertain identifications flagged in metadata (e.g., “cf” or unID markers).
- Pollen identifications supported by pollen atlases and literature; macrofossil identifications supported by standard references and online resources.

## Format, Access, and References

- Data are provided in CSV format with standardized units (SI units for concentrations; percentages for abundances; counts for taxa).
- The dataset includes a comprehensive list of references for methodologies and identifications (LOI, diatoms, isotopes, XRF, pollen, macrofossils, chironomids, cladocera, pigments, etc.), as well as data handling and quality-control practices.
- Detailed methodological references include Battarbee & Kneen (diatom analysis), Conley & Schelske (Biogenic Silica), Renberg (diatom slide preparation), Moore et al. (pollen analysis), and several taxonomic keys for diatoms, Cladocera, Chironomidae, and macrofossil identifications.

## GIS-Relevant Considerations for Data Products

- The multi-proxy, depth-resolved data enable construction of 3D or layered GIS products (lake/basin-scale maps with depth-enabled proxies).
- Potential uses:
  - Visualizing spatial-temporal patterns of organic content, diatom communities, and elemental proxies across lakes.
  - Creating depth-time slices to compare proxy changes across lakes with consistent depth bins (1 cm or 2 cm).
  - Integrating with lake shapefiles and basemap layers to analyze spatial relationships in environmental change reconstructions.
- Standardization notes:
  - For GIS analyses, harmonize depth resolution to a common bin (e.g., 1 cm) where possible.
  - Use the Running_top_cm and Running_bot_cm fields to generate continuous depth profiles and to align proxies across lakes.

- Key caveats:
  - Some sequences were not analyzed for all proxies; respect missing data in GIS layers.
  - Data quality and proxy availability vary by lake and core; consult the metadata and data management notes for each dataset.