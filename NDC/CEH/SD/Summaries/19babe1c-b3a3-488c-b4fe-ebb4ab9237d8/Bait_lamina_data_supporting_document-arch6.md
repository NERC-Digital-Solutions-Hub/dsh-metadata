# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016)

## Overview
- A data companion to the study of soil biological activity in the Chernobyl Exclusion Zone (CEZ), comprising dataset materials and methods, and column explanations for multiple data files.
- Supports analysis of radionuclide concentrations, bait lamina feeding activity, and associated environmental variables across sampling campaigns in 2005 and 2016.
- Data underpin a 2021 publication by Beresford et al. and are tied to established radiological assessment methods (ERICA Tool, R&D128).

## Data files and their content
- Radionuclide_concentration_data_2005.csv
  - Metadata: Sample_number (CEH sample identifier), Date_of_sampling, Location, Site (Low/Medium/High/Dead), Latitude, Longitude, Plot.
  - Measured soil activities (dry mass): Cs-137, Sr-90, Cs-134, K-40, Co-60 (kBq/kg dry mass); includes < for minimum detectable activity where applicable.
- Bait_lamina_2005.csv
  - Activity measurements for bait-lamina related nuclides detected in soil: Am-241, Eu-154, Eu-155, Pu-238+239+240 (kBq/kg dry mass).
- Reader_1_bait_lamina_2016.csv and Reader_2_bait_lamina_2016.csv
  - Reading results for 16 bait-lamina strips per plot across 18 sites: site, plot, replicate, bait-lamina identifiers, and a 0/1 score per hole indicating pierced (1) or unpierced (0).
  - Extra field to track bottom/top hole status and overall bite counts per strip; results read blind by two readers and averaged.
- Main_data_2016.csv
  - Site-level and plot-level data for 2016, including: Location (RF/other CEZ zones), Plot, Latitude, Longitude, Ambient_dose_rate (µSv/h), radionuclide activities (Cs_Bqkg_DW, Sr_Bqkg_DW, Am_Bqkg_DW, Pu isotopes), Pu_isotopes_below_LOD flag, Pu-238/239/240 activities, and dose-related metrics for different organisms (Annelid_Total_Dose_uGyh, Arthropod_Total_Dose_uGyh, Bacteria_total_Dose_uGyh).
  - Additional fields: Reader total bites (Reader_1_total_bites, Reader_2_total_bites, Average_total_bites), Average_total_bites, Percent_utilisation, Bite_holes_1_4 through Bite_holes_9_16, Soil_pH, Soil_percent_moisture, Soil_bulk_density_gcm3, Soil_temp_oC_Apr_2016, Soil_temp_oC_May_2016, Simple_habitat, Field_notes.
- Concentration_ratios.csv
  - Concentration ratios for exposure models, detailing nuclide-specific ratios by organism (Annelid, Detritivorous_arthropod) and nuclides (Cs, Sr, Am, Pu) to contextualize dose estimates (e.g., Cs, Sr, Am, Pu; for Annelid and Detritivorous_arthropod; with Nuclide labels).

## Study design and sampling timeline
- 2005 (four CEZ sites)
  - Sites: Red Forest (High, Dead), Izumrudnoe (Low), Novoshepel Forestry (Medium).
  - Bait lamina deployed; soil samples collected on 27 September 2005; pH and soil moisture recorded.
- 2016 (eighteen CEZ sites)
  - Within CEZ; includes Red Forest (eight sites with a wide range of ambient dose rates) and various deciduous/coniferous woodlands.
  - Sites categorized into habitat groups: Coniferous, Deciduous, Red Forest.
  - Experimental setup: three 1x1 m plots per site; sixteen bait-lamina strips deployed per plot in a 4x4 grid; retrieval after ~18 days (5–7 May 2016).
  - Environmental measurements: ambient dose rate at plot level; soil temperature at insertion and removal; post-retrieval soil pH, moisture, bulk density.

## Measurements and analytical methods
- Radionuclide analyses (soil)
  - Cs-137: gamma spectrometry with HPGe detector; calibration with 152Eu source; detection limits around 0.18 Bq/sample; uncertainties ~10–15%.
  - Sr-90: beta-spectrometry without radiochemical pretreatment; daily calibrations; uncertainties ~20%.
  - Am-241 and Pu isotopes (238Pu, 239Pu, 240Pu): HPGe detector; method validated against radiochemical standards; typical uncertainties ~10–15% at higher activity levels.
  - Data organization includes detection limits and whether activities are reported as minimum detectable values.
- Bait lamina feeding activity
  - ISO 18311: 16 bait-lamina strips per plot, with 16 holes per strip at 5 mm intervals; bait composition (cellulose, wheat bran, charcoal).
  - Feeding activity scored as pierced vs unpierced per hole; reads performed blind by two readers; results averaged per plot.
  - Outputs include top/bottom hole statuses and aggregated bite counts per strip, plus-derived metrics (total bites, average bites, percent utilization, bite holes by segment ranges).
- Soil and environmental measurements
  - pH (soil), soil moisture (%), soil bulk density (g/cm3), and soil temperatures (April and May 2016) collected per plot.
  - Ambient dose rate measured with a dose-rate meter at plot level.
- Dose-rate estimation for soil organisms
  - Annelid (worms) and detritivorous arthropod doses estimated using ERICA Tool (Brown et al. 2008, 2016).
  - Soil bacteria doses estimated using the R&D128 model (due to ERICA size limitations); both approaches yield comparable results.
  - Internal concentrations for annelids derived using 2014 Lumbricidae concentration ratios; detritivorous arthropod using ERICA default ratios; Pu isotopes treated using Red Forest 2014 isotopic ratios for input into ERICA.
  - Assumption: 100% occupancy within the soil column; measured soil dry matter (DM) used to scale external dose rates.

## Data quality, handling, and notes
- Detection limits and censored data indicated with “<” in relevant tables.
- Two readers conducted bait-lamina scoring; no significant differences observed; results averaged for analyses.
- Field notes may contain contextual information (age, vegetation cover, soil type, site history) to aid interpretation.
- Data linked to the Beresford et al. (2021) publication and related methodological references (ISO 2016, ERICA Tool updates, R&D128).

## Data usage and ecosystem context
- Dataset enables cross-year comparison of soil radionuclide contamination, soil properties, and soil organism activity across CEZ habitats.
- Provides structured, self-describing data to support downstream analyses, dashboards, or self-serve exploration of feeding activity and radiological risk to soil-dwelling organisms.
- Useful for reproducible dose assessments and for studies requiring integration of physical measurements, biological activity proxies, and radionuclide concentration data.

## References and related resources
- Beresford et al. (2021) Dataset underpinning the assessment of soil biological activity in the CEZ.
- ERICA Tool (Brown et al. 2008, 2016).
- R&D128 (Copplestone et al. 2001).
- ISO 18311:2016 (bait-lamina test method).
- Field and laboratory methodologies for radionuclide measurements and dose estimation cited within the materials and methods.