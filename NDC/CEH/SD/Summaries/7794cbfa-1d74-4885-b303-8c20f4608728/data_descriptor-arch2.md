# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Overview
- Dataset of photosynthetic pigment concentrations (µg L-1) in water from 20 Scottish lochs collected May–June 2022.
- Purpose: develop a calibration model to derive pigment concentrations from hyperspectral images taken with a mobile imager.
- Data file: pigment_results.csv. Columns include sampling dates, sampled lochs, sample IDs, replicate subsamples, and volumes for HPLC and spectrophotometry analysis.
- The first author (corresponding author) is responsible for data correctness and reliability.

## Data collection and storage
- Water samples collected by grab sampling from surface layers; samples stored at +4 °C and processed within 48 hours.
- Water temperature measured with a digital handheld thermometer.
- Coordinates (WGS84) provided via iPhone-derived data; sampling sites and Loch names are recorded to enable traceability.

## Sampling details
- Table 1 lists sampling dates and sites (e.g., Loch Leven, Airthrey Loch, Loch Lomond, etc.) with multiple sampling points per loch and precise coordinates.
- Sampling dates range across May 4 to June 9, 2022, with repeated visits to several lochs (e.g., Loch Leven and Airthrey Loch).

## Laboratory analysis: chlorophyll and carotenoid assessment
- Phytoplankton collected on GF/F filters; filters identified to match field data with pigment concentrations.
- Filters flash-frozen in liquid nitrogen and stored at -80 °C; shipped on dry ice to DHI (Denmark) for analysis.
- In the lab, pigments extracted with 95% acetone plus an internal standard (vitamin E).
- Extraction: 4 °C, 20 h, vortexing and sonication; filtered into HPLC vials (0.2 µm filter) and analyzed by HPLC (Shimadzu LC-10A) with LC Solution software.
- Pigments measured include chlorophylls a, b, c1, c2, pheophytins, zeaxanthin, beta-carotene, lutein, fucoxanthin, peridinin, and many others listed (a broad suite of chlorophylls, carotenoids, and related pigments).
- Data handling: samples stored at -80 °C with analyses conducted within 4–6 months of collection.

## Laboratory analysis: phycocyanin assessment
- Phycocyanin samples collected on GF/F filters; stored at -20 °C prior to shipping on dry ice to the analysis laboratory (and stored at -20 °C there) for 3–6 months before analysis.
- Extraction buffer prepared daily with precise phosphate stock solutions to achieve pH 6.7–6.8.
- Extraction: filters chopped, ground in buffer to a pulp, then subjected to repeated freezing/thawing and sonication on ice; centrifugation used to clarify extracts.
- Absorbance measured at 615 nm, 652 nm, and 750 nm using a Shimadzu UV-1800 spectrophotometer.
- Phycocyanin concentration calculated with the Bennett and Bogorad (1973) equation: Ce = [(A615 − A750) − 0.474 × (A652 − A750)] / 5.32.
- Reagents and extraction procedures documented for reproducibility.

## Data file and structure
- pigment_results.csv contains:
  - Column 1: sampling dates
  - Column 2: loch names
  - Column 3: sample identification numbers
  - Column 4: replicate subsamples
  - Columns 5–6: sample volumes for HPLC and spectrophotometry analyses

## Data quality and responsibilities
- Data quality assurance steps include data verification, cleaning, and transformation to standardised outputs suitable for environmental monitoring and policy assessment.
- Clear linkage between field sampling, laboratory analyses, and dataset to support traceability and reproducibility.

## Use for monitoring and policy
- Provides calibrated pigment measurements to support hyperspectral imaging-based monitoring, enabling broader environmental health assessments of Scottish lochs.
- Dataset can be combined with other environmental datasets to enhance monitoring value and support data accessibility and reuse by researchers and policymakers.

## References
- Bennett, A., and L. Bogorad. 1973. Complementary chromatic adaptation in a filamentous blue-green alga. J. Cell Biol. 58(2): 419-435.