# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016). Beresford et al., 2021

## Overview
- Compiles column heading explanations for multiple CSV data files and describes materials and methods.
- DataFiles: Radionuclide_concentration_data_2005.csv, Bait_lamina_2005.csv, Reader_1_bait_lamina_2016.csv, Reader_2_bait_lamina_2016.csv, Main_data_2016.csv, Concentration_ratios.csv.
- Associated publication: Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016).
- Purpose aligned with environmental monitoring: standardised dataset descriptions to support assessment of soil biological activity and radiation exposure.

## Data Files and Key Content (Table-Driven Summaries)
- Radionuclide_concentration_data_2005.csv (Table 1)
  - Columns include sample identifier, sample type (soil), sampling date, location, site, geographic coordinates, plot, and activity concentrations for Cs-137, Sr-90, Cs-134, K-40, Co-60 (all in kBq/kg dry mass), with markers for minimum detectable activities where applicable.
- Bait_lamina_2005.csv (Table 2)
  - Contains radionuclide data for bait-lamina substrates (Am-241, Eu-154, Eu-155, Pu-238+239+240) in kBq/kg dry mass.
- Reader_1_bait_lamina.csv and Reader_2_bait_lamina.csv (Table 3)
  - Site/Plot/Replicate structure across 18 sites; 3 plots per site; 16 bait-lamina strips per plot read by each reader.
  - For each strip: top-to-bottom hole piercing status (1 = pierced, 0 = not), total readings per strip, and plot-level fields including soil pH and soil moisture.
  - Readings are blinded; two readers’ results averaged.
- Main_data_2016.csv (Table 4)
  - Spatial and environmental context: Location (including RF/CEZ designation), plot, latitude/longitude, ambient dose rate (µSv/h).
  - Radionuclide concentrations in soil (Cs, Sr, Am, Pu isotopes) in Bq/kg dry mass; Pu below LOD indicator; cumulative dose-rate metrics for target organisms (Annelid, Detritivorous Arthropod, Bacteria).
  - Bait-lamina derived metrics: total bites (Reader 1 and 2), average bites, percent utilisation, bite holes by hole-group (top 4, 5–8, 9–12, 13–16, top 8, bottom 8), soil properties (pH, moisture, bulk density, temperature), habitat classification, and field notes.
  - Additional fields include Pu isotopes below LOD flag and various field-derived descriptors.
- Concentration_ratios.csv (Table 5)
  - Concentration ratios by organism (Annelid; Detritivorous_arthropod) and nuclide (Cs, Sr, Am, Pu) used to convert soil activity to internal exposure proxies; includes column headings and units/methodology.

## Study Design and Sites
- 2005
  - Four CEZ sites: Red Forest (High and Dead), Izumrudnoe (Low), Novoshepel Forestry (Medium).
  - Bait lamina deployment in September 2005; soil pH and moisture recorded.
  - Sites categorized by anticipated soil activity; Dead site near High site with pine-tree die-off in 1986.
- 2016
  - 18 CEZ sites (within Red Forest and surrounding woodlands).
  - Site types: Red Forest (8 sites), mature mixed deciduous woodland, deciduous woodland to the west, coniferous woodland in lower deposition areas.
  - Ambient dose rate measured at each plot; habitat groups classified as Coniferous or Deciduous woodland or Red Forest.
  - Bait lamina deployment in April 2016; retrieval after ~18 days in May 2016.

## Bait Lamina Method
- Strips: 155 × 6 × 1 mm PVC with 16 bi-conical apertures at 5 mm intervals; bait composed of cellulose, wheat bran, and active charcoal.
- Deployment: 16 sticks per plot in a 4×4 grid; top aperture just below soil surface; one extra strip inserted/withdrawn to prevent abrasion damage.
- Reading: After retrieval, two readers scored “pierced” vs “unpierced” to indicate bait removal; strips read blind; results averaged per plot.
- Outcome: Feeding activity represented as hole piercing, with vertical distribution of feeding recorded.

## Field Sampling and Laboratory Analyses
- Soil sampling
  - Per plot: five 10 cm-deep soil cores (2.5 cm diameter) collected, bulked, and homogenised.
  - Sub-samples for pH and moisture; remaining sample dried to determine dry mass and soil bulk density.
- Radionuclide analyses
  - Cs-137: Gamma spectrometry (HPGe detector); calibration with 152Eu source; minimum detectable activity ~0.18 Bq per sample; ~10–15% uncertainties.
  - Sr-90: Beta spectrometry without radiochemical pretreatment; ~20% uncertainty.
  - Am-241 and Pu isotopes: HPGe detector with thin Be window; standard-based comparison for activity concentrations; typical agreement within ±10–15%.
- Dose-rate estimation
  - Annelid and Detritivorous Arthropod doses estimated with ERICA Tool (v2; Brown et al., 2008, 2016).
  - Bacteria dose estimated with R&D128 methodology (soil bacteria external exposure modeled).
  - Concentration ratios for annelids derived from Lumbricidae (Western Red Forest, 2014) and ERICA defaults for detritivorous arthropods.
  - Pu isotopes incorporated using Red Forest 2014 isotopic ratios for input into ERICA; all three organisms assumed 100% soil column occupancy.
  - Measured soil DM used to scale external dose rates (e.g., 10% DM implies 10% of 100% DM dose).

## Data Quality and Standardisation
- Standardised data collection and documentation across 2005 and 2016; use of blind readers and averaging to reduce observer bias.
- Clear unit definitions and minimum detectable activity markers included to support reproducibility.
- Data linked to established methodologies (ISO 2016 bait-lamina standard; ERICA/R&D128 dose models) to support cross-study comparability.
- Dataset designed to enable integrated environmental health assessment and monitoring over time, in line with environmental monitoring aims.

## References and Context
- ISO 18311:2016 on bait-lamina test methodology.
- ERICA Tool (Brown et al., 2008, 2016) and R&D128 dose assessment framework (Copplestone et al., 2001).
- Prior and related CEZ work: Beresford et al. (various years), Gaschak et al., Smith & Beresford, and Beresford et al. 2021 (online in press) providing context on Red Forest and CEZ radiation ecology.
- Data centre reference: Radionuclide data for vertebrates in the CEZ (Gaschak et al., 2018).

## Notes for Analysts
- The dataset provides a structured, standardised basis for comparing environmental health indicators over time in a radiologically contaminated habitat.
- By including both direct measurements (radionuclide concentrations) and biological activity proxies (bait-lamina feeding), plus modeled dose rates, the data support assessment of ecological health and policy performance.
- The materials emphasize data provenance, measurement uncertainty, and cross-method compatibility to facilitate verification and reuse in monitoring programmes.