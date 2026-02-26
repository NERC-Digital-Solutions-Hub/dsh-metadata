# WP2_Baseline_sample_data.csv

## Overview
- Data resource describing soil baseline measurements from eight UK agricultural sites collected in September–October 2022.
- Parameters include pH (H2O and CaCl2), moisture (fresh, air-dried, and oven-dried), stone content, bulk density (fine earth and whole sample), organic matter (LOI), soil texture, total carbon and nitrogen, and other supporting measurements.
- Samples processed at UK Centre for Ecology & Hydrology (UKCEH) Lancaster; some archived samples from Auchincruive analyzed by Thermo-Gravimetric Analysis (TGA) at UKCEH Bangor due to anomalously high carbon values.
- Project funded by the Department for Energy Security & Net Zero (formerly BEIS); baseline data collected before biomass crop establishment.

## Experimental Design and Sampling Regime
- Sampling locations predetermined across sites to align with planned biomass plots; replicate samples taken within each field block/plot.
- For three large demonstration blocks per site, six soil samples collected; for five smaller demonstration plots, three samples collected per site.
- Sampling grids adapted to plot shapes; six reference samples collected from unplanted field areas or adjacent fields.
- Geographic locations generated in GIS (QGIS 3.22.4, WGS84); GPS coordinates exported for sample points.
- Depths: cores collected to 0–15 cm and 15–30 cm (adjusted where necessary due to soil characteristics like stoniness).

## Field Methods and Sample Handling
- Field marking with flags prior to sampling; samples transported in cooled conditions and stored at 4°C at UKCEH until processing (within two weeks).
- Each sampling location: soil collected with Split tube sampler (~40 cm long, 48 mm diameter); samples split by depth into 0–15 cm and 15–30 cm increments; some subsoil horizons processed separately.
- Biomass crop plots included variety trials and reference plots; additional six reference samples per site from unplanted areas.

## Laboratory Processing and Analyses
- Subsamples prepared for pH (10 g in 25 mL water; measured again after CaCl2 addition).
- Moisture and LOI analyses: air-drying at 25°C for at least two weeks; sieving to 2 mm; LOI at 375°C after oven-drying to determine organic matter content.
- Bulk density calculations:
  - Fine earth density: based on ovendried weight, sample volume, and stone volume.
  - Whole-sample density: based on total core weight and sample volume.
- Total Carbon and Nitrogen: measured with LECO TruSpec CN; calibration and quality checks described (standards and blanks).
- Sub-sampling for microbial research: 10 g subsamples stored at -80°C.
- pH measurements in water and CaCl2 as described; document method calibration (pH buffers used).
- Texture (archived 0–15 cm samples) analyzed via hydrometer sedimentation method with dispersing agent (Na-HMP), including temperature corrections and ROCK prior steps; data plotted on SSEW soil texture triangle using the soiltexture R package.
- Texture data subset selection: 12–14 samples per site chosen to capture texture variation across plots.
- Thermo-Gravimetric Analyses (TGA): performed on Auchincruive (AUC) archived samples to account for anomalous carbon readings due to coal waste nearby; standard TGA procedure with multiple runs and internal standards.

## Data Quality Control and Governance
- Quality checks during data production and entry; e.g., flagged anomalies (e.g., airdried vs fresh weights) investigated against lab notebooks.
- Back-calculation used to estimate missing weights where possible; if unreasonable, data point left blank (QC_code indicates back-calculation status).
- Some missing weights or back-calculation needed for a few rows (e.g., fresh soil+tray, air-dried subsample+tray).
- Detailed documentation of QC codes and data adjustments provided with the dataset.

## Data Files and Structure
- WP2_Baseline_sample_data.csv
  - 29 columns, 694 rows.
  - Key fields include idn, id, section (0–15, 15–30, subsoil), site, plot_type, crop_type, species, sample_no, GPS coordinates (wgs_lat, wgs_long), sample_date, section_start, and numerous measurement columns (pH_H2O, pH_CaCl2, total_ovendried_soil_wt, perc_moisture_airdried, perc_moisture_ovendried, perc_total_moisture, stone_wt, stone_perc, bulk_density_FE, bulk_density_whole, perc_LOI, perc_nitrogen, perc_carbon, carbon_density, Cstock_sample_g, QC_code, etc.).
- WP2_Soil_Texture_Data.csv
  - 8 columns, 208 rows.
  - Fields include unique_id, sample_id, site, method (2-hour or 6-hour), clay, silt, sand, classification_SSEW.
- WP2_TGA_Auchincruive.csv
  - 11 columns, 79 rows.
  - Includes depth, W_Initial, W_105, W_375, W_650, W_1000, and various Loss_* percentages related to moisture, ignition, and CaCO3 estimation.
- Miscellaneous data and references to data provenance and measurement methods.

## Metadata, Versioning, and Calibration
- References include OSU Soil Fertility Laboratory (2020) and Moorberg & Crouse (2017) for texture methods.
- Truspec Carbon calibration summary provided, with calibration details, standards, and error metrics to support CN measurements and accuracy for baseline data.
- Project website: https://www.biomassconnect.org/

## Site and Crop Context
- Site codes: ABR (Aberystwyth), AUC (Auchincruive), BGI (Bio Global Industries), BGF (Boghall Farm), CPF (Cockle Park Farm), HHL (Headley Hall), HLS (Hillsborough), NWK (North Wyke).
- Crop codes reflect reference areas and biomass crops: Willow, Miscanthus giganteus (MI SG), Miscanthus athena (MI St), Eucalyptus, Poplar, etc. Variety trial plots and biomass crop plots included.

## Relevance for Monitoring Frameworks
- Provides baseline environmental health measures critical for monitoring policy impacts on soil health under deployment of biomass crops.
- Demonstrates end-to-end data lifecycle: planning, field sampling, laboratory analyses, data processing, QA, and data sharing.
- Highlights governance considerations (metadata completeness, data accessibility, data transformation needs, and public sharing requirements) typical of monitoring framework work.
- Includes documented data quality controls, handling of data gaps, and transparency around anomalies (e.g., coal-waste influence at AUC site via TGA).