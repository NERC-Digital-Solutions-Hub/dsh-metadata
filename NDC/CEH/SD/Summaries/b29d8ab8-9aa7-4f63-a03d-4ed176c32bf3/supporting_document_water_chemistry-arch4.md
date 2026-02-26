# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

## Overview
- Seven lakes located 1.5 to 225 km from the Chernobyl Nuclear Power Plant (CNPP).
- Contamination levels vary by lake: Glubokoye, Yanovsky lakes, and Cooling Pond are high; Svyatoye Lake is medium; Stoyacheye, Dvoriche, and Gorova lakes are low.
- Timeframe: 2014–2016.
- Data types collected include major alkali and alkali-earth elements, trace elements, inorganic nutrients, hydrological and physicochemical parameters, and 137Cs deposition.

## Data collected and variables
- Major alkali and alkali-earth elements (Mg, Na, S, K, Ca) in mg/L.
- Trace elements (As, Sr, Cd, Cs, Pb, U) in μg/L.
- Inorganic nutrients (NO3 -, NO2 -, PO4 3-) in μg/L.
- Physicochemical parameters: dissolved oxygen (DO, %), pH, temperature (°C), conductivity (μS/cm).
- Hydrological parameters: maximum depth (m), surface area (km2), distance from CNPP (km).
- 137Cs deposition (kBq/m2) on soil.
- All measurements are averages with n = 3 per lake where specified (mean ± SD).

## Data structure and files
- water_chem1.csv
  - Columns include: Lake, Lake region, DO (%), pH, T (°C), Conductivity (μS/cm), Max_depth (m), Surface (km2), Distance_from_CNPP (km), 137Cs_deposition (kBq/m2).
  - Purpose: contextual lake properties and a geospatial/contamination backdrop for each lake.
- water_chem2.csv
  - Columns list concentrations of elements in mg/L (for B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn) and μg/L for trace elements (As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl).
  - Each element has an explanation and a unit/methodology field.
  - Purpose: detailed major and trace element chemistry per lake.
- water_chem3.csv
  - Columns include: Date, Sample, NO3/NO2_Conc_mM, NO2Conc_mM, NO3Conc_mM, PO4_Conc_mM, Dsi_Conc_mM.
  - Purpose: nutrient concentrations (nitrates, nitrites, phosphates) and dissolved silicate in millimolar units.
- Data notes
  - For all three files, the dataset provides per-lake measurements with n = 3 replicates and includes mean ± SD where indicated.
  - Sample labeling and site descriptions accompany the chemistry data to support traceability and reproducibility.

## Methodology and quality assurance
- Sample processing
  - Filtration: 0.2 μm filter for ICP-MS analyses; 0.45 μm filter for nutrient analyses.
  - Acidification: 2% v/v HNO3 (65% trace metal grade) prior to ICP-MS.
  - Preservation: 1% v/v ZnCl2 (50% w/v) for nutrient samples.
- Analytical techniques
  - Major and trace elements measured by quadrupole ICP-MS (iCAPQ) using collision cell mode with 7% Hydrogen in Helium to reduce polyatomic interferences.
  - Internal standards added to samples via a separate line (Ge, Rh, Ir in 2% HNO3).
  - External multi-element calibration standards prepared for major elements (0–30 mg/L) and trace elements (0–100 μg/L).
  - Nutrients measured with a QuAAtro segmented flow nutrient analyser, following standard procedures.
- Quality control
  - Use of internal standards, calibration standards, and replicates (n = 3 per lake) to ensure data reliability.
  - Clear documentation of sample date, sample label, and site information to support traceability.

## Relevance for data leadership and data systems
- Demonstrates a well-documented, multi-source water chemistry dataset with clear metadata, enabling cross-lake comparisons and regional analyses near CNPP.
- Highlights the importance of structured data files (with explicit column explanations, units, and methods) to support discoverability and reuse.
- Illustrates end-to-end data governance touchpoints: data collection, processing methods, QA/QC, and detailed data dictionaries that improve data quality, interoperability, and capacity for future integration with broader environmental monitoring programs.
- Provides a model for ensuring data assets are well-structured, with discoverable metadata, appropriate units, and explicit methodological context to support co-ownership and collaboration across networks of partners.