# A brief description/overview of the data being described

## Overview
- Soil data resource from eight UK sites collected in Sep–Oct 2022 to establish baseline soil characteristics before biomass crop establishment.
- Measured parameters: pH, soil moisture, stone content, bulk density, organic matter, soil texture, total carbon (C) and total nitrogen (N).
- Processing and analysis conducted mainly at UK Centre for Ecology & Hydrology (UKCEH) Lancaster; archived samples from Auchincruive analyzed by ThermoGravimetric Analyses (TGA) at UKCEH Bangor to investigate anomalously high carbon values.

## Experimental Design and Sampling
- Sampling locations selected across fields where biomass crops would be planted; replicates within each field block/plot to capture in-field variation.
- Large demonstration blocks: six soil samples per block at each site; five smaller demonstration plots per site: three samples per plot.
- Variety trial plots: one sample from middle of small plots; three samples from larger plots; six reference samples from non-planted field areas or adjacent fields.
- Sample locations mapped and generated via GIS (QGIS 3.22.4; WGS84); GPS coordinates captured with handheld devices; maps provided in Appendix B.

## Sample Collection
- Locations marked with flags; samples collected to 0–15 cm and 15–30 cm depths (adjusted for some sites due to stone content).
- Sampling tool: Split tube sampler (~40 cm long, 48 mm diameter).
- Post-collection handling: samples kept in insulated cool boxes, transported to UKCEH Lancaster, stored at 4°C until processing (within two weeks).

## Processing and Laboratory Methods
- Subsampling and initial processing:
  - 10 g subsamples for pH (0–15 cm; 0–15 and 15–30 cm where applicable); additional 10 g subsamples stored at -80°C for potential microbial analyses.
  - Subsoil horizons (if present) processed separately.
- Moisture and Loss-on-Ignition (LOI):
  - Air-dry at 25°C for at least two weeks; sieve to 2 mm; stones weighed; water displacement used to estimate stone volume.
  - 10 g subsamples dried at 105°C to determine bound moisture; LOI performed by heating to 375°C for 16 h.
- Calculations:
  - Total moisture (%): derived from air-dried vs. oven-dried weights.
  - Fine earth bulk density and whole-sample bulk density calculations.
  - LOI (%) calculated from oven-dried vs. air-dried weights.
- Total Carbon and Nitrogen (CN):
  - Measured with LECO TruSpec CN instrument; calibrated with blanks and standards (LECO soil standards, e.g., LECO 1018, 1011); multi-step QC including internal standards and repeated checks.
- Soil pH:
  - Measured in H2O (0–15 cm and other depths as applicable) and then in 0.01 M CaCl2 after initial pH in water.
- Soil Texture:
  - Subset of archived 0–15 cm samples analyzed by hydrometer sedimentation (2-hour or 6-hour method) after dispersion with 5% Na-HMP.
  - Calculations produce clay, silt, sand percentages; results plotted on SSEW texture triangle using R (soiltexture package).
- Thermo-Gravimetric Analyses (TGA):
  - Performed for Auchincruive (AUC) to account for unusually high carbon values; analyzes moisture, organic/inorganic content via controlled heating; performs mass-loss calculations including conversion to CaCO3 where relevant.
- Quality Control:
  - Data entry checks with conditional formatting; back-calculation of flagged values against lab notebooks; missing critical values replaced by calculated estimates where possible; flagged data left blank when unreliable.
  - QC_code records back-calculation status for each data point.
- Calibration:
  - Truspec carbon calibration summary indicates calibration and validation steps, including reference standards and performance metrics (e.g., LECO standard materials, calibration curves, RMS error).

## Data Files and Metadata
- WP2_Baseline_sample_data.csv
  - 29 columns, 694 rows; contains core sample-level data (identifiers, site/plot metadata, coordinates, sample depth, pH values, moisture, bulk density, LOI, carbon, nitrogen, Cstock, and QC_code).
  - Fields include unique identifiers (idn, id), sample positions (wgs_lat, wgs_long), sample_date, section_start, various moisture/density/chemical measurements, and metadata on plot_type and crop_type.
- WP2_Soil_Texture_Data.csv
  - 8 columns, 208 rows; contains texture estimation results per sample (method, clay%, silt%, sand%, and SSEW classification).
- WP2_TGA_Auchincruive.csv
  - 11 columns, 79 rows; contains TGA-derived data for Auchincruive samples (W_Initial, W_105, W_375, W_650, W_1000; Loss_Moisture and related loss fractions).
- Appendix references:
  - Site codes: ABR, AUC, BGI, BHF, CPF, HHL, HLS, NWK with corresponding site names.
  - Crop codes and partner institutes (e.g., IBERS, SRUC, NIAB, AFBI).
- Project website: https://www.biomassconnect.org/
- Additional references and methods:
  - OSU Soil Fertility Laboratory (2020) 2-Hour Hydrometer Method for soil texture.
  - Moorberg and Crouse (2017) Soils Laboratory Manual (K-State Edition).

## Data Governance and Access
- Data collection aligned with a larger biomass project framework; data are organized with explicit sampling designs, precise spatial coordinates, and depth-specific measurements to enable re-use and integration across networks.
- Metadata-rich CSV files with explicit column definitions and data provenance.
- Quality control measures documented to support data reliability and reproducibility.
- Carbon and nitrogen measurements include calibration and quality checks to address potential anomalies (notably at AUC site verified with TGA).

## Notes and References
- Data support materials include sampling maps, site codes, crop codes, and methodological references.
- The dataset is part of a broader effort to benchmark soil properties in biomass crop contexts and supports data-driven decisions for soil management and monitoring.