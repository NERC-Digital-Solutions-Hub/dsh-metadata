# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

- Seven lakes near the Chernobyl Nuclear Power Plant (CNPP) studied from 2014–2016, spanning distances of 1.5 to 225 km from CNPP.
- Lakes and contamination levels:
  - High contamination: Glubokoye, Yanovsky lakes, Cooling Pond.
  - Medium contamination: Svyatoye Lake.
  - Low contamination: Stoyacheye, Dvoriche, Gorova lakes.
- Analytes and measurements:
  - Major alkali and alkali-earth elements: Na, Mg, S, K, Ca (mg/L; mean ± SD; n = 3 per lake).
  - Trace elements: As, Sr, Cd, Cs, Pb, U (μg/L; mean ± SD; n = 3 per lake).
  - Nutrients and physicochemical parameters: NO3^−, NO2^−, PO4^3− (μg/L; NO3/NO2 and PO4), dissolved oxygen (DO, %), pH, temperature (°C), conductivity (μS/cm).
  - Caesium-137 deposition (137Cs) in soil (kBq/m^2) surrounding the lakes.
- Surface-water sampling and time frame:
  - Sampling across 2014–2016, with surface water analyses and initial Cs deposition context.

- Methodology and measurement approach:
  - Sample processing: filtration through 0.2 μm (for major and trace elements) and 0.45 μm (for nutrients); acidification with 2% v/v HNO3 (65% HNO3, trace metal grade) prior to ICP-MS.
  - Instrumentation for major/trace elements: quadrupole ICP-MS (iCAPQ, Thermo Scientific) with collision cell mode (7% hydrogen in helium) and kinetic energy discrimination to reduce interferences.
  - Internal standards: Ge, Rh, Ir in 2% HNO3.
  - Sample introduction: autosampler (Cetac ASX-520), nebuliser (1 mL/min), spray chamber.
  - Calibration: two external multi-element calibration standards (major: 0–30 mg/L; trace: 0–100 μg/L).
  - Quality control: dedicated QA/QC procedures including internal standards and calibration validation.
  - Post-filtration nutrients: 0.45 μm filtration followed by preservation with 1% ZnCl2 (50% w/v) and analysis via QuAAtro segmented flow nutrient analyser.
  - Data structure notes: measurements reported as mean ± SD with n = 3 per lake where applicable.

- Data files and structures:
  - water_chem1.csv
    - Contents: Lake, geographic region, dissolved oxygen (DO %), pH, temperature (T °C), conductivity (μS/cm), maximum depth (m), surface area (km^2), distance from CNPP (km), 137Cs deposition (kBq/m^2), and related metadata.
    - Data structure: columns described with explanations and units; link to sampling sites (Figure 1 map context).
  - water_chem2.csv
    - Contents: Concentrations of major and trace elements (B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl) in mg/L, with explanations and units for each column.
  - water_chem3.csv
    - Contents: Date, Sample, NO3/NO2_Conc_mM (combined nitrate/nitrite), NO2Conc_mM, NO3Conc_mM, PO4_Conc_mM, Dsi_Conc_mM (dissolved silicate), with explanations and units.
    - Data structure: time-stamped nutrient and dissolved silicate concentrations by sample.

- Analytical context and potential uses:
  - Enables examination of correlations between Cs deposition and Cs concentrations in lake waters, as well as broader trace-element patterns across lakes with different contamination levels.
  - Supports analyses of nutrient status (nitrates, nitrites, phosphates) in relation to lake contamination category and hydrological parameters.
  - Allows spatial comparisons (distance from CNPP) and temporal assessments across 2014–2016 (via water_chem3) to identify trends or anomalies.
  - Facilitates unification of datasets from different formats (mg/L, μg/L, mM) into a coherent, multi-parameter water chemistry profile for each lake.

- Data considerations for analysts:
  - Replication: measurements often reported as mean ± SD with n = 3 per lake; consider implications for statistical power at local scales.
  - Unit harmonization: major elements (mg/L), trace elements (μg/L), nutrients (mM); ensure consistent unit conversion when integrating across datasets.
  - Spatial scale: data encompass multiple lakes at varying distances from CNPP, enabling local-to-regional inferences but requiring careful interpretation for extrapolation.
  - Data provenance and metadata: structured data descriptions accompany each file, including sampling dates and site descriptions; facilitates reproducibility and metadata-driven discovery.