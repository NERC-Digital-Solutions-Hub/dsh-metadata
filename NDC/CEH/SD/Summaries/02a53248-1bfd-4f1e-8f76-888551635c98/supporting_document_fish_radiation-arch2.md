# Impact of Environmental Radiation on the Health and Reproductive Status of Fish from Chernobyl

## Aim and Scope
- Assess health and reproductive status of perch (Perca fluviatilis) and roach (Rutilus rutilus) in relation to environmental radiation from the Chernobyl area.
- Use standardized methods and data outputs to enable monitoring of environmental health and policy performance over time.
- Collect and prepare datasets suitable for storage in portals and for broad data reuse.

## Sampling and Study Sites
- Temporal coverage:
  - September 2014: 124 perch and 82 roach from seven lakes in Belarus and Ukraine.
  - September 2015: four lakes in Ukraine.
  - March 2015: 38 perch and 60 roach collected just before spawning.
- Species and age determination:
  - Focus on mature fish; scales sampled for age assessment.
- Lake selection and radiation gradient:
  - Lakes chosen for hydrological properties and long-term exposure to a radiation dose gradient.
  - Proximity to Chernobyl NPP ranged from 1.5 to 225 km.
  - Contamination categories: High (Glubokoye, Yanovsky, Cooling Pond), Medium (Svyatoye), Low (Stoyacheye, Dvoriche, Gorova).
- Abundance assessment:
  - Relative species abundance recorded in a June 2015 session.

## Biological Measurements and Health Indicators
- Morphometrics and condition:
  - Body weight, total length; Fulton condition index (K); hepatosomatic index (HSI); gonadosomatic index (GSI).
- External and histological health indicators:
  - External signs of disease; macroscopic tumors noted.
  - Histology of gonads to assess oocyte development; oocyte surface measurements; germ cell stage frequencies.
- Age, tissue sampling, and analysis workflow:
  - Standard ICES methodologies for measurements.
  - Blood cell micronucleus test to assess genetic material loss (1000 cells scored per fish).

## Radiological Measurements and Dose Assessment
- Radionuclide activity measurements:
  - 137Cs: whole-body activity in five fish per lake (September 2014) via gamma spectrometry (HPGe detector); detection limit ~0.6 Bq.
  - 90Sr: whole-body activity in five fish from selected high-contamination lakes using radiochemical separation and β-detection; ~0.01 Bq limit.
  - 238Pu, 239,240Pu, 241Am: measured in liver and muscle (3–5 fish per high-contamination lakes) via radiochemical separation and alpha spectrometry; 241Am also via gamma spectrometry.
  - Uncertainties: ~20% for 137Cs, ~15% for 90Sr, ~25% for transuranics (0.95 confidence).
- Dose calculations:
  - External doses from 137Cs gamma radiation (dominant external source); sediment-based activity and ERICA-based dose coefficients used.
  - Sediment assumptions: majority of 137Cs in the top 15 cm, density ~1300 kg/m3.
  - External dose rate: 1.45 × 10^-4 μGy/h per Bq/kg wet weight with occupancy factor 0.5 at sediment surface.
  - Internal doses: calculated for 137Cs in all lakes; internal doses for 90Sr, 241Am, 238Pu, 239,240Pu focused on near-field lakes; dose conversion coefficients applied per radionuclide.
- Laboratory methods:
  - 137Cs: gamma spectroscopy.
  - 90Sr: radiochemical separation with 90Y daughter measurement.
  - Pu/Am isotopes: alpha spectroscopy after resin-based separation; 241Am measured by gamma spectroscopy.

## Liver Chemistry and Micronucleus/Histology
- Liver chemistry:
  - Acidic nitric mineralization of liver tissue; major and trace elements measured by ICP-MS (iCAPQ, collision cell mode) after digestion.
  - External calibration standards for major (0–30 mg/L) and trace (0–100 μg/L) elements; internal standards used.
- Micronucleus test:
  - Erythrocyte micronuclei assessed in blood; 1000 cells per fish scored blindly; micronuclei identified by morphologic criteria.
- Histological analysis of oocytes:
  - Gonad cross-sections fixed, processed, paraffin-embedded; H&E stained.
  - For females: counts of immature (perinuclear, cortical alveolar) oocytes within defined surface area; calculation of relative germ cell stage frequencies; surface area measurements via imaging software.

## Data Structure and Management
- Data collected and organized into standardized datasets:
  - fish_biometry.csv: fish identity, site, date, gender, species, weight, length, gonad/liver weights, Fulton index, GSI, HSI.
  - fish_composition.csv: per-lake presence/absence of species with site location data.
  - fish_whole.csv: radionuclide levels (e.g., 137Cs, 90Sr) in whole fish by site and species.
  - fish_tissue.csv: radionuclide levels in liver/muscle tissue by tissue type, date, site, species.
  - fish_liverchem.csv: liver mass (wet/dry), major and trace elements (B, Na, Mg, P, S, K, Ca) and trace metals (Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U).
  - fish_micronucleus.csv: site, species, sex, number of micronuclei per 1000 erythrocytes, cell-level data.
  - fish_oocyte.csv: date, site, species, oocyte counts (cortical alveolar, perinuclear), defined area measurements.
- Purpose:
  - Ensure consistent data capture for cross-lake comparisons and time-series monitoring.
  - Facilitate data storage and upload to appropriate environmental data portals.

## Uncertainties and Quality Assurance
- Measurement uncertainties explicitly stated for radionuclide analyses.
- Use of validated, standardized procedures (ICES, ERICA) to ensure data quality and comparability.
- Cross-cutting quality checks through multiple analyses (biometry, histology, micronucleus tests) to support integrated environmental health interpretation.

## Relevance for Environment Monitoring and Data Access
- The study demonstrates a comprehensive, standardized data framework linking radionuclide exposure to fish health and reproductive status across a gradient of environmental contamination.
- Data structures are designed to maximise interoperability and reuse, aligning with goals to increase dataset value and enable broad data access for researchers and policymakers.