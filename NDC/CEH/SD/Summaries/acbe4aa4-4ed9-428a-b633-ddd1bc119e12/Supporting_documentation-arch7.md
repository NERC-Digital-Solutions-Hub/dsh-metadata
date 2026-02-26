# Feather isotope ratios and sexing of oystercatchers breeding in Iceland

## Study context
- Conducted across south, west, north-west and north-east Iceland during summers 2013–2017.
- Aimed to understand migratory strategies of oystercatchers (Haematopus ostralegus) via feather isotope analysis and molecular sexing.
- Feathers reflect diet and habitat during the wintering period when they were grown.

## Data collection and sampling
- Capture: incubating oystercatchers were trapped at nests and uniquely marked with metal rings and color rings.
- Sampling:
  - 4–5 chest feathers collected per individual for stable isotope analysis (driven by winter moult location).
  - Blood samples collected for a subset to determine sex molecularly.
- Sample scope:
  - 552 individuals with feather isotope data (breeding in Iceland; lowland south and west Iceland).
  - 321 individuals with DNA-based sexing data (same population).

## Laboratory analysis and isotopes
- Isotope methodology:
  - Feathers washed in 2:1 chloroform/methanol, dried, cut into fragments.
  - Samples weighed (~0.45–0.55 mg) and analyzed by combustion elemental analysis coupled to an isotope ratio mass spectrometer.
  - Isotopes reported as δ13C (V-PDB standard) and δ15N (AIR-N2 standard).
- Quality and precision:
  - Internal standard (collagen) replicates show measurement errors of 0.2‰ for δ13C and 0.1‰ for δ15N.

## Data files and columns
- OystercatcherFeatherIstotopes.csv
  - Year of feather collection (2013–2017)
  - Individual ID (ring-based)
  - d15N (feather δ15N)
  - d13C (feather δ13C)
  - Status (Migr ant, Unknown, or Resident)
  - WinterLocation (country observed during winter)
- OystercatcherSexing.csv
  - Individual ID (ring-based)
  - DNA-derived sex (based on Fridolfsson & Ellegren 1999 method)

## GIS relevance and potential applications
- Enables map-based exploration of migratory strategies by linking isotope signatures with wintering locations.
- Visualize spatial distribution of migratory vs. resident individuals and across wintering countries.
- Combine with other spatial datasets (e.g., habitat, climate, ringing data) for enhanced migratory ecology analyses.
- Temporal dimension (2013–2017) allows investigation of interannual variation in migration and habitat use.
- Data are in CSV format with clear identifiers for integration into GIS workflows and data products.

## Data quality, provenance, and limitations
- Provenance tied to a standardized sampling protocol and lab analysis pipeline; explicit measurement errors reported.
- Individual identification via a consistent ringing scheme supports traceability across datasets.
- Sexing data available for a subset; not all individuals have molecular sex information.
- Feather isotope data reflect winter moult period and may not capture annual short-term dietary changes.