# A brief description/overview of the data being described

- Soil data from eight agricultural sites across the UK, collected in September–October 2022, with measurements of pH, soil moisture, stone content, bulk density, organic matter content, soil texture, and total carbon and nitrogen.
- Sampling used a Split tube sampler; processing conducted at UKCEH Lancaster (Sept 2022–Aug 2023); archived samples from one site analysed by Thermo-Gravimetric Analyses (TGA) at UKCEH Bangor.
- Baseline data for biomass crop projects; funded by the Department for Energy Security & Net Zero (formerly BEIS) (Client reference CEH-303).

## Experimental Design and Sampling

- Pre-determined sampling locations across sites, with replicate samples within each field block/plot; six samples for large demonstration blocks per site; three samples for smaller demonstration plots; six reference samples from unplanted areas or adjacent plots.
- Locations generated in GIS (QGIS 3.22.4) using WGS84 (EPSG:4326); GPS coordinates captured; maps provided in Appendix B.
- Depths: 0–15 cm and 15–30 cm (adjusted at some sites, e.g., BGI); exact locations recorded; sampling planned to capture plot-specific and field-wide variation.
- Plot shapes sometimes irregular; sample grids adapted accordingly.
- For variety trial plots, sampling from specific middle points; reference soil samples taken from unplanted field areas.

## Sample Collection and Processing

- Field procedures: flags used to mark locations; sampling at 30 cm depth; samples split into 0–15 cm and 15–30 cm (with site-dependent adjustments); 30 cm cores collected using Split tube sampler; samples transported to UKCEH Lancaster and stored at 4°C until processing (within ~2 weeks).
- Processing and subsampling: remove fresh soil, homogenize; 10 g subsamples for pH in H2O, and 10 g subsamples stored at -80°C for potential microbial analyses.
- Moisture and LOI: air-drying at 25°C for at least two weeks; sieved to 2 mm; stone volume measured; 10 g subsamples for LOI (105°C) and subsequent combustion at 375°C for organic matter content.
- Calculations performed for: gravimetric moisture, fine earth bulk density, organic matter (LOI), and total carbon and nitrogen (via LECO CN instrument with standard calibration procedures).
- pH measurements: pH in water and after CaCl2 addition (0.125 M CaCl2) to approximate soil pH in mild saline conditions.
- Texture analysis: a subset of archived 0–15 cm samples analysed by hydrometer sedimentation using Na-HMP dispersant; particle size fractions (sand, silt, clay) calculated and texture classified (SSEW method) using R.
- Thermo-Gravimetric Analyses (TGA): performed on Auchincruive (AUC) samples due to anomalously high total carbon values; analysis at Bangor with staged heating (105°C, 375°C, 650°C, 1000°C) to partition moisture, organic/inorganic content and CaCO3 formation.
- Quality control and data handling: automated formatting checks; flagged values cross-checked against lab notebooks; back-calculation used to address missing data where possible; unresolved or critical values left blank; QC codes recorded for traceability.

## Data Files and Metadata

- WP2_Baseline_sample_data.csv
  - 29 columns, 694 rows; includes identifiers (idn, id, site, plot_type, crop_type, sample_no), coordinates (wgs_lat, wgs_long), depth section, pH (H2O, CaCl2), moisture, bulk density (fine earth and whole), LOI, nitrogen, carbon, stone metrics, Cstock, and QC_code (for back-calculation notes).
  - Describes sample sections (0–15 cm, 15–30 cm, subsoil) and site-specific metadata.
- WP2_Soil_Texture_Data.csv
  - 8 columns, 208 rows; method (2-hour or 6-hour sedimentation), estimated clay/silt/sand percentages, and SSEW classification.
- WP2_TGA_Auchincruive.csv
  - 11 columns, 79 rows; temperatures and corresponding masses (W_Initial, W_105, W_375, W_650, W_1000) and derived losses (Loss_Moisture, Loss_105to375, Loss_375to650, Loss_650to1000) with CaCO3 conversion.
- Data dictionaries and column definitions are included within the files.
- Data provenance: sample collection methods, laboratory processing steps, and calibration/quality-control details documented; notes on site-specific issues (e.g., coal waste at AUC) and data completeness.

## Access, Documentation and References

- Project website: https://www.biomassconnect.org/
- References and methods:
  - OSU Soil Fertility Laboratory (2020) 2-Hour Hydrometer Method for Soil Texture
  - Moorberg, C.J. & Crouse, D.A. (2017) Soils Laboratory Manual – K-State Edition
- Site codes: ABR (Aberystwyth), AUC (Auchincruive), BGI (Bio Global Industries), BHF (Boghall Farm), CPF (Cockle Park Farm), HHL (Headley Hall), HLS (Hillsborough), NWK (North Wyke)
- Crop codes and Appendix B (Partner Institute Acronyms): IBERS, BGI, SRUC, NIAB, AFBI
- Additional notes: plot relocation at Hillsborough; carbon calibration summary for Truspec provided in the annex.