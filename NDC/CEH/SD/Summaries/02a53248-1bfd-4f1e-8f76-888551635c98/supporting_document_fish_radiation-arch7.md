# Impact of Environmental Radiation on the Health and Reproductive Status of Fish from Chernobyl

## Overview
- A study assessing health and reproductive status of perch and roach across lakes in Belarus and Ukraine with a gradient of radiation exposure from the Chernobyl NPP.
- Sampling occurred in September 2014 (seven lakes), September 2015 (Ukraine, four lakes), and March 2015 (before spawning for a subset).
- Data collected span fish biometry, chemical and radiological analyses, and histological assessments to relate health indices to environmental radiation.

## Study Area and Sampling Design
- Seven lakes in Belarus and Ukraine selected to represent a radiation dose gradient:
  - High contamination: Glubokoye, Yanovsky lakes, Cooling Pond
  - Medium contamination: Svyatoye Lake
  - Low contamination: Stoyacheye, Dvoriche, Gorova lakes
- Lakes located 1.5 to 225 km from the Chernobyl NPP.
- Species focus: Perch (Perca fluviatilis) and Roach (Rutilus rutilus); additional overall fish abundance recorded in June 2015.
- Sampling gear: three gill nets (20 m length, 21 mm mesh) to target mature fish; separate sessions for age/disease assessments and radionuclide measurements.
- Ethical considerations: fish euthanized following UK Home Office procedures to minimise suffering.

## Measurements and Health Indices
- Fish metrics collected for each individual:
  - Body weight, total length, presence of external disease signs, and macroscopic tumors.
  - Health indices: Fulton’s condition index (K), hepatosomatic index (HSI), gonadosomatic index (GSI).
  - Age determined from scales.
- Micronucleus test: 1000 erythrocytes scored per fish to assess genetic material loss.
- Histology: gonad and liver tissues fixed, sectioned, and stained for assessment. Oocyte development staged by counts of immature/mature oocytes and cortical alveolar forms; germ cell stage frequencies calculated as percentages.
- Data structures prepared for multiple analyses (see Data Structures).

## Radiological Analysis and Dose Calculations
- Radionuclides measured:
  - 137Cs (whole-body measurements; gamma spectrometry)
  - 90Sr (whole-body for select lakes; radiochemical procedures)
  - 238Pu, 239,240Pu, 241Am (liver and muscle tissues; radiochemical separation and alpha spectrometry)
- Uncertainties: 137Cs (≤20%), 90Sr (≤15%), transuranics (≤25%) at 95% confidence.
- Dose calculations:
  - External doses from 137Cs gamma radiation; external exposure to 90Sr and 137Cs beta radiation considered minor due to water shielding.
  - Sediment-based activity concentrations used to estimate external doses; water and sediment densities assumed (sediment 1300 kg/m3; surface layer ~15 cm).
  - Dose coefficients and factors applied for internal doses:
    - 137Cs internal dose coefficient: 4.32×10^-6 mGy/d per Bq/kg
    - 90Sr internal dose coefficient: 1.51×10^-5 mGy/d per Bq/kg
    - 241Am, 238Pu, 239,240Pu internal dose coefficients: ~7.6×10^-5 to 7.2×10^-5 mGy/d per Bq/kg
- Internal dose calculations focused on lakes near the NPP where radionuclides concentrate; broader lakes had lower significance for these isotopes.

## Liver Chemistry and Elemental Analysis
- Liver tissue analyzed after nitric acid digestion; samples filtered and acidified for ICP-MS analysis.
- Major elements measured: Na, Mg, S, K, Ca (mg/L).
- Trace elements measured: As, Sr, Cd, Cs, Pb, U and a broad suite of metals (Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, etc.) in µg/L or µg/L units.
- Rigorous calibration and internal standards used to ensure accuracy in multi-element measurements.

## Data Structures and Datasets
- Detailed schemas prepared for integration into GIS workflows:
  - fish_biometry.csv: site, date, gender, species, weight, total length, gonad weight, liver weight, Fulton index (K), GSI, HSI.
  - fish_composition.csv: date and per-lake presence/abundance by location (Dvorishche, Stoyacheye, Svyatoye, Glybokoye, Yanovsky, Cooling Pond, Gorova).
  - fish_whole.csv: site, species (Perch, Roach), 137Cs (Bq/kg), 90Sr (Bq/kg).
  - fish_tissue.csv: tissue type (muscle or liver), date, site, species, tissue weight, activity concentrations for Cs-137, Sr-90, Am, Pu-239, Pu-238.
  - fish_liverchem.csv: liver mass (wet and dry), and concentrations of multiple elements (B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U) with appropriate units.
  - fish_micronucleus.csv: site, species, sex, number of micronuclei per 1000 erythrocytes, total cell counts, and percentage metrics.
  - fish_oocyte.csv: date, site, species, oocyte metrics (Oocyte_micro_m2, cortical alveolar/oocyte counts, perinuclear oocytes, etc.).
- These datasets enable GIS-based analyses of spatial patterns in health indices and radiological burden across lakes and regions.

## GIS and Data Integration Implications
- The study provides spatially referenced health and radiological datasets across multiple lakes with known contamination gradients, suitable for map-based visualizations and spatial analyses.
- Enables exploration of correlations between radiation dose (external/internal) and biological responses (health indices, micronuclei frequency, oocyte development, liver chemistry).
- Data standardization across lakes and years supports cross-site comparisons and trend analyses in a GIS environment.
- The inclusion of standardized data structures facilitates integration with additional geospatial layers (lake boundaries, distance to NPP, hydrography, land use) for policy and public communication purposes.