# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016)

## Overview
- A data collection and metadata package accompanying a dataset from the Chernobyl Exclusion Zone (CEZ), linked to Beresford et al., 2021.
- Contains column heading explanations (Tables 1–5) and materials/methods for multiple data files spanning 2005 and 2016:
  - Radionuclide_concentration_data_2005.csv
  - Bait_lamina_2005.csv
  - Reader_1_bait_lamina_2016.csv
  - Reader_2_bait_lamina_2016.csv
  - Main_data_2016.csv
  - Concentration_ratios.csv
- Data cover radionuclide concentrations in soils, bait-lamina feeding activity, readers’ bite assessments, and modeled absorbed dose rates for soil biota.
- Fields include site metadata, geographic coordinates, sampling dates, environmental measurements, radionuclide activities, and dose-rate outputs for selected organisms (annelids, detritivorous arthropods, bacteria).
- Methods reflect standard field sampling, laboratory analysis, and dose estimation using recognized tools (ERICA Tool and R&D128), with explicit notes on detection limits and uncertainties.

## Data files and schema (high-level)
- Radionuclide_concentration_data_2005.csv
  - Core fields: Sample_number, Date_of_sampling, Location, Site (Low/Med/High/Dead), Latitude, Longitude, Plot
  - Radionuclide concentrations in soil (dry mass): Cs-137, Sr-90, Cs-134, K-40, Co-60
  - Units: kBq/kg dry mass; some < symbols indicate minimum detectable activity
- Bait_lamina_2005.csv
  - Radionuclides detected in bait-lamina context including Am-241, Eu-154, Eu-155, Pu-238/239/240
  - Units: kBq/kg dry mass; includes < for minimum detectable activity
- Reader_1_bait_lamina_2016.csv and Reader_2_bait_lamina_2016.csv
  - Field structure: Site, Plot, Replicate, Bait_lamina identifiers, 16 holes per stick (top holes 1–16, bottom 16), pierced/unpierced per hole
  - Aggregated fields: total bites per reader, average bites across readers, percent utilization, bite holes by hole ranges (1–4, 5–8, 9–12, 13–16, and 1–8, 9–16)
  - Additional plot-level fields: soil_pH, soil_moisture
- Main_data_2016.csv
  - Location (including RF Red Forest), Plot, Latitude, Longitude
  - Ambient_dose_rate (µSv/h)
  - Radionuclide activities in soil (dry mass): Cs, Sr, Am, Pu isotopes (Pu_238, Pu_239, Pu_240)
  - Pu_isotopes_below_LOD flag
  - Dose-rate outputs for: Annelid, Arthropod (detritivorous), Bacteria (uGy/h)
  - Biological exposure metrics: Reader_1_total_bites, Reader_2_total_bites, Average_total_bites, Percent_utilisation, Bite_holes_1_4, 1_8, 9_16, 1_8/9_16
  - Soil properties: Soil_pH, Soil_percent_moisture, Soil_bulk_density_gcm3
  - Soil temperatures (Apr 2016, May 2016)
  - Simple_habitat and Field_notes
- Concentration_ratios.csv
  - Concentration ratios for annelid and detritivorous arthropod across nuclides (Cs, Sr, Am, Pu); includes Nuclide identifiers
  - Table-style headings describe the relationships and units/methodology

## Data collection and processing methods (highlights)
- Study sites
  - 2005: four CEZ sites (Red Forest: High and Dead; Izumrudnoe: Low; Novoshepel Forestry: Medium)
  - 2016: eighteen CEZ sites within the CEZ, including Red Forest and peripheral woodland types; ambient dose rates measured per plot
  - Sites categorized by simplified habitat groups: Coniferous, Deciduous, Red Forest
- Bait lamina method
  - Strips (approximately 155x6x1 mm PVC) with sixteen 5 mm interval apertures, filled with bait (70% cellulose, 25% finely ground wheat bran, 5% active charcoal)
  - Deployed at three 1x1 m plots per site (4x4 grid per plot), top aperture just below soil surface; retrieval after ~18 days
  - Feeding activity assessed as “pierced” (evidence of bait removal) or “unpierced”; two readers read blind; results averaged
  - An additional strip was inserted and withdrawn to check for abrasion damage
- Soil sampling and analyses
  - At bait lamina removal, five 10 cm-deep soil cores per plot collected; bulked and homogenized
  - Measurements: soil pH, moisture; soil dried at 60°C for dry-mass-based analyses; bulk density estimated
- Radionuclide analyses (2005 and 2016)
  - Cs-137: gamma spectrometry (HPGe detector)
  - Sr-90: beta spectrometry without radiochemical pretreatment
  - Am-241 and Pu isotopes: HPGe detector; standard references and calibration used
  - Uncertainties: typically 10–15% (p=0.95) for Cs/Sr/Am/Pu depending on sample type; LOQ/LOD considerations noted
- Dose-rate estimation
  - Annelid and detritivorous arthropod: ERICA Tool (Brown et al. 2008, 2016)
  - Bacteria: R&D128 model (environment Agency, Copplestone et al. 2001)
  - Concentration ratios for annelids sourced from Lumbricidae data (2014; western Red Forest)
  - Pu isotopes: input into ERICA with Red Forest 2014 isotopic ratios
  - Assumptions: 100% occupancy within the soil column; measured dry matter used to adjust dose estimates
- Quality and units
  - Detection limits and uncertainties clearly stated (e.g., minimal detectable activity for Cs-134; 90Sr measurement uncertainties)
  - Some columns indicate measurements below detection limit (e.g., Pu isotopes below LOD)
  - Metadata include field notes on age, vegetation, soil type, and site history

## Data quality, limitations, and governance considerations
- Detection limits and measurement uncertainties vary by nuclide and method (e.g., Cs-137 ~0.18 Bq per sample; Sr-90 ~20% uncertainty)
- Assumptions in dose modeling (e.g., 100% soil-column occupancy, reliance on DM for dose calculations) influence external vs. internal dose estimates
- Data from 2005 and 2016 are cross-referenced with multiple sources and standard methods, but still require careful harmonization when integrated
- Data are accompanied by detailed metadata (Tables 1–5) to support discoverability and interpretability, aiding data governance and reuse

## Access, reuse, and data governance implications for Data Leaders
- The dataset provides comprehensive metadata and explicit documentation of methods, enabling reproducibility and transparent data governance
- Clear data lineage: multiple CSV files with table-level explanations align with ISO/standardized reporting expectations
- Reuse potential: cross-year analysis of soil radionuclide activity, soil biota feeding activity (bait lamina), and modeled dose rates; cross-reference with ecological and radiological risk assessments
- Linkages to broader data ecosystems: references to ERICA Tool, R&D128, ISO 18311, and related CEZ data initiatives (e.g., NERC Environmental Information Data Centre)
- Considerations for data platform design:
  - Ensure consistent metadata schemas across years and datasets
  - Preserve detection limits, uncertainties, and occupancy assumptions as data provenance
  - Provide clear lineage from raw measurements to modeled dose-rate outputs
  - Facilitate crosswalks between radionuclide concentrations, feeding activity metrics, and dose-rate estimates for policy-relevant analyses

## References (selected)
- ISO 2016. Soil quality - Method for testing effects of soil contaminants on the feeding activity of soil dwelling organisms - Bait-lamina test. ISO 18311:2016
- ERICA Tool updates and related dose modeling literature (Brown et al. 2008, 2016)
- R&D 128 dose assessment methodology (Copplestone et al. 2001)
- Beresford et al. series and related CEZ studies documenting ecological radiological assessments
- Field and analytical methodology references (e.g., Allen 1974 for soil pH, Bondarkov et al. for radionuclide analyses)