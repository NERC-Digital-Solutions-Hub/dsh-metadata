# WP2 Baseline sample data

- Overview
  - Soil data from eight agricultural sites across the UK, collected Sept–Oct 2022.
  - Measured: pH (in water and CaCl2), soil moisture, stone content, bulk density, organic matter (LOI), soil texture, total carbon and nitrogen.
  - Samples processed at UKCEH Lancaster (Sept 2022–Aug 2023); archived Auchincruive samples analysed by Thermo-Gravimetric Analyses (TGA) at UKCEH Bangor.
  - Aimed to provide baseline soil data before planting biomass crops.
  - Funded by the Department for Energy Security & Net Zero (Client CEH-303).

- Experimental Design and Sampling Regime
  - Pre-determined sampling locations across plots to reflect planned biomass crop blocks.
  - Replicates: six samples for large blocks; three samples for smaller plots; six reference samples from unplanted areas or nearby fields.
  - GPS/ GIS: Locations generated in QGIS (v3.22.4) using WGS84; exported to handheld GPS (Garmin GPSMap 66s).
  - Depths: 0–15 cm and 15–30 cm (adjusted at some sites, e.g., BGI); six samples per large block, three per small plot.
  - In-field variation considered to contextualize future measurements.

- Sample Collection and Handling
  - Locations flagged; soil sampled to 30 cm depth, split into 0–15 cm and 15–30 cm (adjusted where necessary).
  - Collected with Split tube sampler (approx. 40 cm long, 48 mm diameter).
  - Samples stored in insulated cool box, transported to UKCEH Lancaster, stored at 4°C until processing within two weeks.

- Laboratory Methods and Processing
  - pH: 10 g fresh subsample with 25 ml water (1:2.5); measure after 30 min and 30 s; then measure again after adding 2 ml 0.125 M CaCl2.
  - Moisture and LOI: air-dry at 25°C for ≥2 weeks; sieve to 2 mm; measure moisture by drying at 105°C; LOI by heating to 375°C.
  - Bulk density: calculated for fine earth (FE) and whole sample using core weight, sample volume, and stone volume.
  - Organic matter: LOI on 2 mm sieved, oven-dried subsamples.
  - Total Carbon and Nitrogen: measured with LECO TruSpec CN instrument; calibration runs with blanks and standards (LECO CRM) prior to sample runs.
  - Texture (subset analysis): 12–14 samples per site using hydrometer sedimentation after dispersal with 5% Na-HMP; temperature-corrected readings; texture fractions used to plot SSEW texture class.
  - TGA (Auchincruive AUC): used to investigate anomalously high carbon values; analyses at Bangor following SOP; presents moisture, organic/inorganic fractions, and CaCO3 (via CO2 loss × 2.27).
  - Data capture: sample identifiers, depths, method details, and instrument readings systematically recorded.

- Calculations and Transformations
  - Moisture content: gravimetric calculation from fresh and oven-dried weights.
  - Fine earth bulk density and whole-sample bulk density calculations.
  - LOI: percentage weight loss during LOI step.
  - Carbon and nitrogen: derived from LECO CN instrument readings with calibration standards; quality checks included.
  - Texture: fractions of sand, silt, and clay derived from hydrometer readings; classification via SSEW protocol.
  - TGA outputs: moisture and organic/inorganic content; CaCO3 inferred from CO2 loss where applicable.

- Quality Control and Data Integrity
  - Conditional formatting flagged potential data errors (e.g., airdried weight > fresh weight).
  - Flagged data were back-checked against lab notebooks; if unreliable, data left blank.
  - Missing weights for fresh soil+tray or air-dried subsamples back-calculated where possible (QC_code indicators used).
  - Calibration and instrument performance tracked; Truspec carbon calibration summaries include multiple standard runs and performance metrics.

- Data Files and Structure
  - WP2_Baseline_sample_data.csv
    - 29 columns, 694 rows.
    - Key fields include idn, id, section (0–15, 15–30, subsoil), site codes, plot_type, crop_type, species, sample_no, GPS coordinates, sample_date, section_start, and multiple measured parameters (pH H2O, pH CaCl2, total_ovendried_soil_wt, perc_moisture_airdried, perc_moisture_ovendried, bulk_density_FE, bulk_density_whole, LOI, perc_nitrogen, perc_carbon, carbon_density, Cstock_sample_g, QC_code).
  - WP2_Soil_Texture_Data.csv
    - 8 columns, 208 rows.
    - Fields: unique_id, sample_id, site, method (2-hour or 6-hour sedimentation), clay, silt, sand percentages, classification_SSEW, and description.
  - WP2_TGA_Auchincruive.csv
    - 11 columns, 79 rows.
    - Fields: id, section, W_Initial, W_105, W_375, W_650, W_1000, Loss_Moisture, Loss_105to375, Loss_375to650, Loss_650to1000.
  - Quality Control code (QC_code) fields indicate back-calculation status or flagged data.
  - Project website: https://www.biomassconnect.org/

- Site and Crop Context
  - Site codes: ABR, AUC, BGI, BHF, CPF, HHL, HLS, NWK (e.g., Auchincruive, Aberystwyth, Hillsborough, etc.).
  - Crop codes reflect study plots: Willow, Miscanthus giganteus (MISg), Miscanthus Athena (MISt), etc.
  - Appendix lists partner institutes (IBERS, SRUC, NIAB, AFBI, etc.).

- Data Provenance and References
  - OSU Soil Fertility Laboratory (2020) texture method; Moorberg & Crouse (2017) soils manual referenced for texture use.
  - Project context and resources tied to the biomass crop baseline assessment.

- Additional Notes
  - A Truspec carbon calibration summary is included, detailing calibration curves, standards, drift, and error metrics for carbon measurements.