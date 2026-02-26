# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

## Overview
- Seven lakes in Belarus and Ukraine, located 1.5–225 km from the Chernobyl Nuclear Power Plant (CNPP).
- Contamination levels: Glubokoye, Yanovsky, and Cooling Pond (high); Svyatoye (medium); Stoyacheye, Dvoriche, Gorova (low).
- Study period: 2014–2016.
- Measurements include major alkali/alkali-earth elements, selected trace elements, nutrients, and basic physicochemical parameters.
- Data intended for cross-lake comparisons, assessing contamination influences, and enabling data-driven decision making or public communication.

## Datasets and data structure
- water_chem1.csv
  - Variables: Lake, Geographical region, DO (%), pH, Temperature (°C), Conductivity (μS/cm), Max_depth (m), Surface (km2), Distance_from_CNPP (km), 137Cs_deposition (kBq/m2).
  - Structure: two-column headers describing each variable (explanation and units/methodology).
- water_chem2.csv
  - Variables: Major elements (B, Na, Mg, P, S, K, Ca, etc.) and a wide list of trace elements (Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl).
  - Units: mg/L; each element accompanied by explanation and units/methodology.
- water_chem3.csv
  - Variables: Date, Sample, NO3/NO2_Conc_mM, NO2Conc_mM, NO3Conc_mM, PO4_Conc_mM, Dsi_Conc_mM.
  - Units: millimolar (mM); includes sample/site labeling and date.
- Data notes: Each file includes detailed column descriptions and units/methodology to facilitate merging and consistent analyses.

## Methodology
- Sample preparation: filtration through 0.2 μm, acidification with 2% HNO3 (65% HNO3, trace metal grade).
- Analytical technique: quadrupole ICP-MS (iCAPQ) with collision cell (KED, 7% H2 in He) to reduce interferences.
- Sample introduction: autosampler (Cetac ASX-520), nebuliser, spray chamber; internal standards (Ge, Rh, Ir) in 2% HNO3.
- Calibration: two external multi-element calibration standards (major elements 0–30 mg/L; trace elements 0–100 μg/L).
- Nutrients: after 0.45 μm filtration and preservation (ZnCl2, 1%), measured with a QuAAtro segmented flow nutrient analyser.
- Quality control: standard procedures and separate QC lines for sample integrity and calibration.

## Variables and units
- Major elements: Na, Mg, S, K, Ca (mg/L).
- Trace elements: As, Sr, Cd, Cs, Pb, U (μg/L).
- Nutrients: NO3-, NO2-, PO4^3- (from water_chem1 in μg/L; water_chem3 uses mM for NO3/NO2 and PO4, and Dsi).
- Physicochemical parameters: DO (%) , pH, Temperature (°C), Conductivity (μS/cm), Depth (m), Surface area (km2), Distance from CNPP (km), 137Cs deposition (kBq/m2).

## Temporal and spatial coverage
- Timeframe: 2014–2016.
- Locations: Seven lakes in the Belarusian and Ukrainian regions near CNPP, with diverse proximity and contamination contexts.

## Data quality, preprocessing, and structure
- Data are organized in three complementary CSV files, with explicit documentation for each variable.
- ICP-MS methodology includes collision-cell mode with kinetic energy discrimination to remove interferences.
- Nutrient measurements follow established QC methods, including preservation steps.
- Clear metadata for sampling sites, dates, and sample identifiers to support reproducible analyses.

## Potential data products and analyses
- Cross-lake comparisons of major and trace element concentrations by lake and contamination level.
- Spatial analysis: relation between Cs deposition, distance to CNPP, and elemental/nutrient profiles.
- Time-based dashboards or pivot tables to explore trends across lakes and sampling dates.
- Correlation analyses between abiotic parameters (DO, pH, temperature, conductivity) and elemental/nutrient levels.
- Public-facing maps and summaries communicating contamination context and data quality.

## How to use and integrate
- Combine the three CSVs by common keys (lake, sample/date, or sample label) to create integrated datasets containing physicochemical parameters, elemental concentrations, and nutrients.
- Normalize units where necessary (mg/L vs μg/L; convert NO3-/NO2-/PO4^3- between μM/mM and mg/L as appropriate for comparison).
- Utilize the provided methodological notes to ensure consistent interpretation of measurements and detection limits.
- Develop self-serve data products (dashboards, pivot tables) enabling stakeholders to filter by lake, region, or contamination level and compare across time.

## Challenges and considerations for data support
- Heterogeneous data formats and units across datasets; careful unit reconciliation is required.
- Patchy or uneven sampling across lakes and dates may affect trend analyses.
- Clear communication of complex measurements (e.g., trace elements at μg/L) to non-expert audiences.