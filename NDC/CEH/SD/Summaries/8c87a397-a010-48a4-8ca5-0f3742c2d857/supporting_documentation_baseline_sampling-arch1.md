# A brief description/overview of the data being described

- Soil data collected from eight agricultural sites across the UK in September–October 2022 to establish baseline soil properties before biomass crop establishment.
- Measured parameters include pH (in H2O and CaCl2), soil moisture, stone content, bulk density, organic matter (LOI), soil texture, and total carbon and nitrogen.
- Processing conducted at UKCEH Lancaster; archived samples from one site (Auchincruive) analysed by Thermogravimetric Analysis (TGA) at UKCEH Bangor to address elevated carbon values.
- Experimental design geared toward site- and plot-level baseline characterization to support future comparisons after biomass cropping.
- Funded by the Department for Energy Security & Net Zero (formerly BEIS) under Client reference CEH-303.

## Experimental design and sampling regime

- Samples taken at pre-determined locations within field blocks that would receive biomass crops; replication scaled to plot size.
- Large demonstration blocks: six soil samples per block; eight sites each with three blocks (six samples per block across three large blocks: SRC Willow, Miscanthus Athena, Miscanthus giganteus).
- Smaller demonstration plots: three samples per plot; multiple plots per site.
- Reference samples: six samples from unplanted field areas or adjacent fields.
- Location data generated with GIS (QGIS 3.22.4, WGS 84) and GPS; sample locations mapped (Appendix B).

## Field collection and processing

- Depths sampled: 0–15 cm and 15–30 cm where possible; adjustments made for very stony soils (BGI) and plot shapes.
- Sampling instruments: Split-tube sampler; samples transported at 4°C to UKCEH Lancaster and processed within ~2 weeks.
- Reference and plot-specific sampling grids adjusted to field boundaries; location flags placed prior to sampling.

## Laboratory methods and calculations

- pH: measured in water (pH_H2O) and then in CaCl2 (pH_CaCl2) after a 30-minute stand and 10-minute equilibration.
- Moisture and LOI: fresh soil weighed, air-dried at 25°C for ~2 weeks, sieved to 2 mm, and LOI determined after 105°C drying and 375°C ignition.
- Bulk density: estimated for fine earth (FE) and whole core using mass and volume, adjusting for stone volume.
- Organic matter: LOI percentage from 375°C step.
- Total carbon and nitrogen: analyzed by LECO CN instrument with standard calibration; QA included blanks, standards, and repeat Runs; site-specific calibration checked.
- Texture: archival 0–15 cm samples analyzed by hydrometer sedimentation (with Na-hexametaphosphate dispersant) to estimate sand, silt, and clay fractions; results plotted on a texture triangle and classified (SSEW or descriptive).
- TGA (Auchincruive): used on archived 0–15 cm and 15–30 cm samples to partition moisture, organic matter, and inorganic components; CaCO3 loss calculated by mass loss multiplied by 2.27; analyses at Bangor per SOP-3010.
- Data handling and QA: conditional formatting flagged anomalies (e.g., airdried vs. fresh weights); problematic values back-calculated when possible; some data left blank if back-calculation was unreasonable.

## Datasets and file structure

- WP2_Baseline_sample_data.csv
  - 29 columns, 694 rows
  - Key fields: idn, id, site, plot_type (e.g., RA, DB, DP, VT, REF), crop_type (G, PG, SRC, SRF, A, etc.), species, sample_no, coordinates (wgs_lat, wgs_long), sample_date, section_start, pH_H2O, pH_CaCl2, total_ovendried_soil_wt, perc_moisture_airdried, perc_moisture_ovendried, perc_total_moisture, stone_wt, stone_perc, bulk_density_FE, bulk_density_whole, perc_LOI, perc_nitrogen, perc_carbon, carbon_density, Cstock_sample_g, QC_code, etc.
- WP2_Soil_Texture_Data.csv
  - 8 columns, 208 rows
  - Fields: unique_id, sample_id, site, method (2-hour or 6-hour), clay (%), silt (%), sand (%), classification_SSEW
- WP2_TGA_Auchincruive.csv
  - 11 columns, 79 rows
  - Fields: id, section, W_Initial, W_105, W_375, W_650, W_1000, Loss_Moisture, Loss_105to375, Loss_375to650, Loss_650to1000
- Metadata
  - Sampling window: Sep 2022–Aug 2023; field lab processing at Lancaster; AUC TGA analysis at Bangor
  - Project website: https://www.biomassconnect.org/
  - Site codes: ABR, AUC, BGI, BHF, CPF, HHL, HLS, NWK
  - Crop codes: Willow, Miscanthus giganteus (MISg), Miscanthus athena (MISt), etc.

## Context and applicability for analysis

- Data are designed to support correlations, baseline-condition modeling, and future impact assessments of biomass cropping on soil properties at multiple scales (plot to site).
- Provides both direct measurements (pH, moisture, bulk density, LOI, CN) and derived metrics (texture fractions, C stock) across eight sites, with explicit sampling design and QA notes.
- Limitations noted: some site-specific data anomalies (e.g., coal-derived carbon at AUC resolved with TGA) and the potential mismatch between methods when comparing texture and carbon measurements.
- Data are accompanied by detailed documentation of sampling schemes, lab methods, and QA procedures to support reproducibility and data reuse.