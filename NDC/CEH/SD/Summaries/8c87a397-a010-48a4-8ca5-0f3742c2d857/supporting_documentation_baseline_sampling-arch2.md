# WP2 Baseline Sample Data

## Overview
- Soil baseline data collected from eight UK agricultural sites in September–October 2022 to support biomass crop trials.
- Measurements cover pH (H2O and CaCl2), soil moisture, stone content, bulk density, organic matter (LOI), soil texture, and total carbon and nitrogen.
- Processing and initial analyses performed at UKCEH Lancaster ( Sept 2022–Aug 2023); archived samples from Auchincruive analysed by Thermo-Gravimetric Analyses (TGA) at UKCEH Bangor due to anomalous carbon values.
- Funded by the Department for Energy Security & Net Zero (formerly BEIS) (Client reference CEH-303).
- Data resources include three CSV datasets and accompanying documentation; QA processes implemented during data production and entry.

## Experimental Design and Sampling
- Predetermined sampling locations across sites, aligned with biomass plots; replicates sized to plot area to capture within-plot variation.
- Large demonstration blocks: six soil samples per block at each site; five smaller demonstration plots: three samples per plot.
- For variety plots, one sample from small plots (middle) or three from larger plots; six reference samples from unplanted field areas or nearby fields.
- Exact sample locations generated in GIS (QGIS 3.22.4, WGS84; exported as GPS exchanges, collected with Garmin GPSMap 66s).
- In-field plots and maps provided in Appendix B.

## Sample Collection and Processing
- Sampling to 30 cm depth, split into 0–15 cm and 15–30 cm (with site-specific depth adjustments due to stone content).
- Split-tube sampler used; samples kept cool and transported to UKCEH Lancaster, stored at 4°C until processing within two weeks.
- Subsamples taken for pH (10 g fresh soil; 25 ml deionised water; also CaCl2 dilution for pH), and 10 g subsamples stored at -80°C for microbial DNA analyses.
- Processing includes: air-drying, sieving to 2 mm, weighing, moisture determination, LOI (organic matter) after 375°C incubation, and stone content by displacement.

## Laboratory Methods
- pH measurements: pH in water and post-CaCl2 dilution using calibrated pH meter.
- Organic matter: LOI performed on sieved, oven-dried subsamples.
- Carbon and nitrogen: total C and N measured with LECO CN analyzer; blanks and standards used for calibration and quality checks.
- Texture analyses: subset of archived 0–15 cm samples analysed by hydrometer sedimentation method (with Na-HMP dispersant) and subsequent calculations for clay, silt, and sand; results plotted on a soil texture triangle.
- Thermo-Gravimetric Analyses (TGA): used on Auchincruive archived samples to partition moisture, organic/inorganic content, and CaCO3; conducted at Bangor with staged heating (105, 375, 650, 1000 °C) and mass loss recorded.
- Quality Control: data flagged for anomalies (e.g., inconsistent weights); back-calculation used to resolve issues where possible; flagged data either corrected or left blank if not resolvable.

## Calculations
- Moisture content: gravimetric moisture calculated from air-dried and oven-dried weights.
- Fine earth bulk density: calculated from core weight, sample volume, and stone volume; bulk density for whole samples also calculated.
- LOI: percentage loss during LOI procedure.
- Carbon and nitrogen: analyzed via LECO CN instrument with calibration standards and blanks.
- Texture: hydrometer readings corrected for temperature and blank, yielding percentages of clay, silt, and sand; classifications mapped using SSEW scheme via R.

## Quality Control and Data Management
- Conditional formatting in data entry to detect errors (e.g., airdried vs fresh weights); cross-checked against lab notebooks; back-calculation to validate values; unresolved critical data left blank.
- QC_code documented for back-calculation handling (e.g., missing fresh weight or airdried weight).
- Data files and associated metadata stored as CSVs with defined schemas; project documentation and appendices provide site and crop code dictionaries.

## Data Files and Schema
- WP2_Baseline_sample_data.csv: 29 columns, 694 rows; core sample metadata and measured values (e.g., pH, moisture, stone content, bulk density, LOI, CN, C_stock, QC_code).
- WP2_Soil_Texture_Data.csv: 8 columns, 208 rows; texture fractions (clay, silt, sand) and SSEW classification.
- WP2_TGA_Auchincruive.csv: 11 columns, 79 rows; TGA outputs including moisture, organic/inorganic losses, and CO2-derived CaCO3 estimates.
- Datasets include site codes, plot types, crop types, sample numbers, GPS coordinates (WGS84), sample dates, depth ranges, and QC indicators.

## Site and Crop Codes
- Sites: Aberystwyth (ABR), Auchincruive (AUC), Bio Global Industries (BGI), Boghall Farm (BGH/BHF), Cockle Park Farm (CPF), Headley Hall (HHL), Hillsborough (HLS), North Wyke (NWK).
- Crops: G (grassland), PG (perennial grass), SRC (short rotation forestry - willow), SRF (short rotation forestry), A (arable), MISg (Miscanthus giganteus), MISt (Miscanthus athena), Willow, Poplar, Eucalyptus.

## Access and References
- Project website: https://www.biomassconnect.org/
- References for methods include OSU Soil Fertility Laboratory (2-Hour Hydrometer Method) and Soils Laboratory Manual (K-State Edition).