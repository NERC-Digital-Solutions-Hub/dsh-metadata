# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016). Beresford et al., 2021

## Overview
- Compilation of column definitions and methods for multiple data files linked to a study of soil biological activity in the Chernobyl Exclusion Zone (CEZ) during 2005 and 2016.
- Data support map‑based analyses of radionuclide concentrations, bait lamina feeding activity, and related dose assessments for soil organisms.
- Core components include site plots, geographic coordinates, soil properties, radionuclide activity, bait-lamina reader results, and modeled absorbed dose rates.

## Files and data formats (Table-driven metadata)
- Radionuclide_concentration_data_2005.csv: soil radionuclide concentrations (e.g., Cs-137, Sr-90, Cs-134, K-40, Co-60) with sample metadata (sample number, date, location, site, plot, latitude, longitude).
- Bait_lamina_2005.csv: radionuclide-like data for bait lamina? (Table 2 headings indicate Am-241, Eu isotopes, Pu isotopes), plus measurement units.
- Reader_1_bait_lamina_2016.csv and Reader_2_bait_lamina_2016.csv: two readers’ counts of “bites” (piercings) on 16 bait lamina holes per plot, with top-to-bottom hole coding and plot metadata.
- Main_data_2016.csv: integrated 2016 dataset including ambient dose rates, Cs/Sr/Am/Pu activity in soil (dry mass), Pu below LOD flag, dose-rate components for annelids, arthropods, and bacteria, bait lamina bite totals, averaged bite metrics, habitat, field notes, and soil properties (pH, moisture, temperature, bulk density, etc.), plus geographic coordinates.
- Concentration_ratios.csv: concentration ratios for annelids and detritivorous arthropods across nuclides (Cs, Sr, Am, Pu) and related figure references.
- Each table includes detailed column explanations (units, methodology) (Tables 1–5).

## Study design and sites
- 2005 study:
  - Four CEZ sites: Red Forest (High and Dead), Izumrudnoe (Low), Novoshepel Forestry (Medium).
  - Sites categorized by expected soil activity concentrations; soil pH and moisture recorded.
- 2016 study:
  - Eighteen CEZ sites, including eight in the Red Forest; sites span mature mixed deciduous and coniferous woodlands with varied ambient dose rates.
  - Sites described by simplified habitat groupings: Coniferous, Deciduous, Red Forest.
  - Geographic locations captured with GPS coordinates; ambient dose rates measured at plots.

## Bait lamina method
- 16 bait lamina sticks deployed per plot (4x4 grid) within each of three 1x1 m plots per site.
- Strips: approximately 155x6x1 mm PVC with sixteen 5 mm interval apertures; filled with bait ( cellulose, bran, charcoal ).
- Deployment and retrieval:
  - Insertion period: 17–19 April 2016; retrieval: ~18 days later (5–7 May 2016).
  - An additional strip inserted and withdrawn to check for abrasion effects.
  - Soil temperature recorded at insertion and removal.
- Reading and scoring:
  - Strips read blind by two readers; scoring: pierced (1) or unpierced (0) per hole (1 top hole to 16 bottom hole).
  - Both readers’ results averaged; results summed per plot (across 16 strips) for analyses.
  - Variables captured include top/bottom hole piercing, hole-by-hole piercing, and overall bite metrics.
- Hole distribution data (per hole) are included in Reader_1/Reader_2 files; per-plot totals and derived metrics (e.g., average bites, percent utilization) are in Main_data_2016.csv.

## Soil sampling and analyses
- Post-laminate, five 10 cm-deep soil cores per plot were collected (corners plus center), bulked, dried, and used for:
  - pH (method of Allen, 1974) and soil moisture (oven-dried sub-sample).
  - Dry mass (DM) for dose calculations.
- Radionuclide analysis:
  - Cs-137: measured by gamma spectrometry (HPGe detector) with calibration standards; MDAs around 0.18 Bq per sample.
  - Sr-90: measured by β-spectrometry without radiochemical pretreatment.
  - Am-241 and Pu isotopes (Pu-238, Pu-239, Pu-240): measured with HPGe detector; radiometric standards used for input into models.
- Data produced include activity concentrations in Bq/kg dry mass for Cs, Sr, Am, and Pu isotopes; soil DM and related properties also recorded.

## Dose rate estimation and modeling
- Purpose: estimate absorbed dose rates for soil organisms using established wildlife radiological assessment tools.
- Modeling approaches:
  - Annelid (earthworm) and detritivorous arthropod dose rates estimated with ERICA Tool (Brown et al. 2008, 2016).
  - Soil bacteria dose rates estimated with the R&D128 model (due to ERICA size limitations).
- Inputs and assumptions:
  - Concentration ratios: derived for Lumbricidae (annelids) from 2014 Red Forest data; detritivorous arthropod ratios from ERICA defaults; bacteria assumed external exposure due to small size.
  - Pu isotopes: isotopic ratios from Red Forest 2014 data used to split total Pu into Pu-238/239/240 for ERICA inputs.
  - Occupancy: assumed 100% occupancy within the soil column.
  - Measured soil DM percentages used to scale dose outputs (e.g., 10% DM yields 10% of the 100% DM value).
- Outputs:
  - Annelid_Total_Dose_uGyh, Arthropod_Total_Dose_uGyh, Bacteria_total_Dose_uGyh (and by component).
  - Dose-related fields are designed for GIS-enabled spatial visualization across plots.

## GIS-ready data and integration considerations
- Spatial identifiers:
  - Location (site), Plot, Latitude, Longitude, and specific site identifiers (Low/Medium/High/Dead for 2005; Red Forest vs. other habitat types for 2016).
- Data granularity and resolutions:
  - Plot-level measurements across 18 sites (2016) and 4 sites (2005); 1x1 m plots per site; 16 bait lamina sticks per plot.
- Data relationships:
  - 2005 and 2016 radionuclide concentrations linked to corresponding bait lamina and dose data via site, plot, and coordinate fields.
  - Concentration_ratios and dose-model inputs provide a bridge between measured activity and modeled exposure.
- Quality and provenance notes:
  - Two independent readers for bait lamina data; results averaged for robustness.
  - Field notes and habitat classifications support contextual GIS analyses.
  - Documented methodological references and ISO standard basis (ISO 18311:2016) for bait-lamina protocols.

## Key insights for GIS applications
- Enables mapping of spatial patterns in soil radionuclide activity (Cs-137, Sr-90, Am-241, Pu isotopes) across CEZ sites and plots.
- Supports visualization of feeding activity and biodegradation proxies from bait lamina results (pierced/unpierced by readers).
- Allows linkage of radionuclide data with modeled dose rates for soil organisms (annelids, detritivorous arthropods, bacteria) to assess ecological risk landscapes.
- Provides a framework for integrating soil properties (pH, moisture, bulk density, temperature) with biological and radiological measurements for spatial analyses.

## References and methodological context
- ISO 18311:2016. Soil quality – Method for testing effects of soil contaminants on the feeding activity of soil-dwelling organisms – Bait-lamina test.
- ERICA Tool (Brown et al. 2008, 2016) for dose-rate assessments to wildlife.
- R&D 128 (Copplestone et al. 2001) for dose assessments in soil bacteria.
- Beresford et al. (2021) dataset publication and Beresford et al. 2008; Gaschak et al. 2018 for related CEZ data.
- Measurement and calibration references for Cs-137, Sr-90, Am-241, Pu isotopes (Bondarkov et al.; Bondarkov et al. 2011; Bondarkov et al. various).