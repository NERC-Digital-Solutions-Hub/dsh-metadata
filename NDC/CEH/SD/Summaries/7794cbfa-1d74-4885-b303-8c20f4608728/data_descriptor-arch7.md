# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Overview
- Dataset of photosynthetic pigment concentrations (µg L-1) from water samples across 20 Scottish lochs collected May–June 2022.
- Aim: develop calibration models to derive pigment concentrations from hyperspectral images captured with a mobile imager.
- Data integrity: first author (corresponding author) is responsible for correctness and reliability.

## Dataset structure
- Stored in pigment_results.csv.
- Columns include:
  - Sampling dates
  - Loch names
  - Sample identification numbers
  - Replicate subsample identifiers
  - Sample volumes for each replicate (HPLC and spectrophotometry)
- Includes extensive geospatial and temporal metadata for each sampling event.
- Table 1 (provided in text) lists sampling dates, lochs, sampling sites, coordinates (WGS84, from iPhone GPS).

## Sampling and field collection
- Method: grab sampling from the surface water layers (pelagic to littoral zones) at listed lochs.
- Handling: samples stored at +4 °C; analyzed within 48 hours of collection.
- In-field measurements: water temperature recorded with a digital handheld thermometer.
- Sampling sites cover diverse locations (e.g., buoy/pelagial, harbour basins, littoral zones, dam/jetties) across lochs such as Loch Leven, Airthrey Loch, Loch Lomond, and others.

## Laboratory analysis
- Chlorophylls and carotenoids:
  - Phytoplankton collected on GF/F filters, identifiers linked to field data.
  - Filters flash-frozen in liquid nitrogen and stored at -80 °C; shipped on dry ice to DHI, Denmark.
  - Extraction with 95% acetone; HPLC analysis (Shimadzu LC-10A) to quantify a broad suite of pigments (e.g., chlorophylls a/c, b, pheophytins, carotenoids, xanthophylls, etc.).
- Phycocyanin:
  - Filtered samples stored at -20 °C; shipped for analysis.
  - Extraction buffer prepared fresh; samples ground and treated with ultrasound; centrifuged to obtain supernatant.
  - Absorbance measured at 615, 652, and 750 nm; concentration calculated using Bennett and Bogorad (1973) equation Ce = [(A615 - A750) - 0.474*(A652 - A750)] / 5.32.
- Reference method details and pigment list are provided.

## Geospatial aspects
- Coordinates for sampling sites are given in Table 1 (WGS84; iPhone-derived).
- Data enable spatial visualization of pigment concentrations across lochs and sampling points.
- Suitable for integrating with loch boundaries, catchment data, and water quality GIS layers to create map-based insights.

## Data quality and provenance
- Field data linked to laboratory analyses via filter-based identifiers and sampling IDs.
- Temporal window: May 4 to June 9, 2022, with multiple sampling events per loch.
- Long-term storage before analysis is noted (4–6 months for pigment analysis; phycocyanin up to 3–6 months).
- Explicit note of responsibility for data correctness by the corresponding author.

## Potential GIS use cases
- Create point-based pigment concentration maps across lochs for May–June 2022.
- Visualize spatial patterns and temporal trends in chlorophylls, carotenoids, and phycocyanin.
- Join pigment data to loch shapefiles for regional comparisons and policy-facing visualization.
- Support calibration models by linking field pigment measurements to hyperspectral image data from mobile platforms.

## References
- Bennett, A., and L. Bogorad. 1973. Complementary chromatic adaptation in a filamentous blue-green alga. J. Cell Biol. 58(2): 419-435.