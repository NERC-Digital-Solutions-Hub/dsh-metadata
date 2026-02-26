# Soil Baseline Data Across Eight UK Sites

- This data resource documents soil measurements from eight UK agricultural sites collected in September–October 2022, with laboratory processing from September 2022 to August 2023. It provides baseline soil characteristics prior to planting biomass crops, funded by the Department for Energy Security & Net Zero.

## GIS and Location Information

- Sample locations were generated and planned using a Geographic Information System (GIS), specifically QGIS Version 3.22.4.
- All sampling coordinates are provided in the World Geodetic System 84 (WGS 84, EPSG:4326) projection.
- Planned soil sample locations were exported as GPS Exchange Format (GPX) files and imported into handheld GPS devices for field collection.
- Maps of sample locations are available in Appendix B.
- The data include precise geospatial fields such as wgs_lat and wgs_long for each sample.

## Experimental Design and Sampling Regime

- Predetermined locations across eight sites were selected to cover plots where biomass crops would be planted.
- Replicate samples were taken within the perimeter of each field block/plot to capture both broad site variation and plot-specific variation.
- Large demonstration blocks (SRC Willow, Miscanthus Athena, Miscanthus giganteus) had six samples per site; five smaller demonstration plots had three samples per site. Regular-grid sampling was used where feasible, with adaptations for plot shapes.
- Six reference samples were taken from non-planted field areas or adjacent fields.

## Data Collected and Laboratory Methods

- Soil characteristics measured:
  - pH (in water and CaCl2)
  - Soil moisture (air-dried, oven-dried), total moisture
  - Stone content and stone percentage
  - Fine earth bulk density and bulk density of the whole sample
  - Organic matter content via Loss-On-Ignition (LOI)
  - Total Carbon and Nitrogen (CN) by LECO TruSpec CN instrument
  - Texture (sand, silt, clay) via hydrometer sedimentation method and temperature-corrected readings
  - Optional: Texture data for archived 0–15 cm samples
  - Thermo-Gravimetric Analyses (TGA) for Auchincruive site to account for anomalous carbon values due to coal waste
- Depths sampled per location: 0–15 cm and 15–30 cm, with subsoil where applicable.
- Sample collection: Split-tube sampler to ~30 cm depth; samples split into depth increments; sterile handling and cold storage at 4°C prior to processing.

## Data Files and Schemas

- WP2_Baseline_sample_data.csv
  - 29 columns, 694 rows
  - Key fields: idn, id, site, plot_type, crop_type, species, sample_no, wgs_lat, wgs_long, sample_date, section_start, pH_H2O, pH_CaCl2, total_ovendried_soil_wt, perc_moisture_airdried, perc_moisture_ovendried, perc_total_moisture, stone_wt, stone_perc, bulk_density_FE, bulk_density_whole, perc_LOI, perc_nitrogen, perc_carbon, carbon_density, Cstock_sample_g, QC_code
- WP2_Soil_Texture_Data.csv
  - 8 columns, 208 rows
  - Fields include: unique_id, sample_id, site, method, clay, silt, sand, classification_SSEW
- WP2_TGA_Auchincruive.csv
  - 11 columns, 79 rows
  - Fields include: id, section, W_Initial, W_105, W_375, W_650, W_1000, Loss_Moisture, Loss_105to375, Loss_375to650, Loss_650to1000
- Data dictionaries and column descriptions are provided inline with the filenames.

## Quality Control and Data Handling

- Data quality checks used conditional formatting to flag anomalies (e.g., airdried weight greater than fresh weight).
- Flagged entries were cross-checked against lab notebooks; in some cases, values were back-calculated or left blank if not resolvable.
- Missing weights such as 'fresh soil+tray' or 'air-dried sample+tray' were back-calculated using alternative recorded data and typical mass loss.
- The Auchincruive site required TGA analysis due to coal-related carbon contamination, affecting carbon estimates.

## Site Codes and Crop Types

- Site codes include: ABR (Aberystwyth), AUC (Auchincruive), BGI (Bio Global Industries), BHF (Boghall Farm), CPF (Cockle Park Farm), HHL (Headley Hall), HLS (Hillsborough), NWK (North Wyke).
- Crop types reflect biomass-focused trials (Willow, Miscanthus giganteus, Miscanthus Athena) and reference areas; various plots include diverse biomass crops and trial configurations.

## Appendices and References

- Appendix B lists partner institutes and site-related acronyms (e.g., IBERS, SRUC, NIAB, AFBI).
- References and related methods include the OSU Soil Fertility Laboratory 2-Hour Hydrometer method and Moorberg & Crouse soil texture procedures.
- Project website: https://www.biomassconnect.org/

## Practical Implications for GIS

- The dataset provides richly geolocated soil baseline information suitable for map-based visualization and spatial analyses, including:
  - Per-plot and per-depth soil properties that can be joined to GIS layers (plots, soils, land cover).
  - Textural class predictions derived from hydrometer measurements plotted against texture triangles.
  - Temporal sequence: sampling coordinates with exact depths enable 3D soil mapping concepts.
- Data formats are CSVs with explicit coordinate columns, enabling straightforward integration with standard GIS workflows.