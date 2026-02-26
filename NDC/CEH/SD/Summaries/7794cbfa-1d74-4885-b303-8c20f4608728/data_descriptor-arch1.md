# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Purpose and scope
- Dataset of photosynthetic pigment concentrations (µg L-1) in water samples from 20 Scottish lochs, collected May–June 2022.
- Collected to develop a calibration model to estimate pigment concentrations from hyperspectral images taken with a mobile imager.
- Data integrity: first author responsible for correctness and reliability.

## Data structure and content
- Primary data file: pigment_results.csv.
- Column details:
  - Column 1: sampling dates.
  - Column 2: sampled loch names.
  - Column 3: sample identification numbers.
  - Column 4: replicate subsamples sampled in the laboratory.
  - Columns 5 and 6: sample volumes for each replicate for High Performance Liquid Chromatography (HPLC) and spectrophotometry assessments.

## Sampling protocol
- Grab sampling from surface water layers of the listed lochs.
- Samples stored at +4 °C and processed within 48 hours.
- Water temperature measured with a digital handheld thermometer.
- Table 1 documents sampling dates and sites, spanning 04 May to 09 June 2022, with coordinates provided for each site.

## Laboratory analysis: chlorophyll and carotenoids (HPLC)
- Phytoplankton collected on GF/F filters; each filter uniquely identified to match field data.
- Filters flash-frozen in liquid nitrogen and stored at -80 °C; shipped on dry ice to DHI (Denmark) and analyzed within 4–6 months.
- Extraction: filters placed in 6 mL of 95% acetone with vitamin E internal standard; vortexed, ice sonicated, extracted at 4 °C for 20 hours, then filtered into HPLC vials.
- Instrumentation: Shimadzu LC-10A HPLC system with LC Solution software; 5:2 solvent ratio for injection after a pre-treatment step.
- Pigments analyzed include a broad suite of chlorophylls (e.g., chlorophyll a, b, c1, c2, pheophytins) and carotenoids (e.g., lutein, zeaxanthin, fucoxanthin, canthaxanthin, astaxanthin) among others.

## Laboratory analysis: phycocyanin
- Filters stored at -20 °C before dry-ice shipment; analyzed within 3–6 months of collection.
- Extraction: filters ground in extraction buffer prepared from phosphate salts to pH 6.7–6.8, with fresh preparation daily.
- Process: grinding, mixing to a pulp, freezing/thawing, sonication, centrifugation; supernatant filtered (0.2 µm) and injected into a quartz cuvette.
- Measurement: absorbance at 615 nm, 652 nm, and 750 nm using a Shimadzu UV-1800 spectrophotometer.
- Phycocyanin concentration (C) calculated with Ce = [(A615 − A750) − 0.474 × (A652 − A750)] / 5.32 (Bennett and Bogorad, 1973).

## Data quality, provenance, and timing
- Laboratory processing windows stated: chlorophyll/carotenoids analyzed within 4–6 months of collection; phycocyanin analyzed within 3–6 months.
- Procedures include strict sample identification, cold-chain handling, and standardized extraction/instrumentation to support reproducibility.

## Uses, limitations, and context for analysis
- Primary use: calibrate hyperspectral imaging-based pigment estimation against ground-truth concentrations.
- Strengths: detailed sampling dates, precise site coordinates, replicate subsamples, and comprehensive pigment suite.
- Limitations and considerations for analysts:
  - Local-scale, multi-site data; integration with hyperspectral data requires careful alignment of sampling times and conditions.
  - Data may involve a wide range of pigment types with varying detectability; ensure accounting for instrumental and extraction efficiencies.
  - Metadata such as site-specific environmental conditions beyond temperature are not listed here, which may influence pigment concentrations.

## References
- Bennett, A., and L. Bogorad. 1973. Complementary chromatic adaptation in a filamentous blue-green alga. J. Cell Biol. 58(2): 419-435.