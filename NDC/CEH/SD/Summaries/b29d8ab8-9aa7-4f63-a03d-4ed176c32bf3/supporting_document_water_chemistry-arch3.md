# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

- Seven lakes near the Chernobyl Nuclear Power Plant (CNPP) were sampled between 2014 and 2016, located 1.5 to 225 km from CNPP.
- Lakes categorized by contamination level: Glubokoye, Yanovsky lakes, and Cooling Pond as high (H); Svyatoye Lake as medium (M); Stoyacheye, Dvoriche, and Gorova as low (L).
- The study records a spatial gradient of contamination and provides a dataset suitable for monitoring environmental health in relation to radiological risk.

## Study design and scope

- Time period: 2014–2016.
- Sampling locations span the Mogilev (Svyatoye Lake) and Gomel (Stoyacheye and Dvoriche) regions of Belarus and the eastern region of Kiev in Ukraine.
- Data compiled to support assessment of environmental health indicators and to inform policy decisions on monitoring approaches.

## Measured parameters

- Major alkali and alkali-earth elements in surface water:
  - Na, Mg, S, K, Ca (mg/L; mean ± SD; n = 3 per lake).
- Trace elements in surface water:
  - As, Sr, Cd, Cs, Pb, U (μg/L; mean ± SD; n = 3 per lake).
- Nutrients and hydro-chemistry:
  - Nitrate (NO3−), Nitrite (NO2−), Phosphate (PO4 3−) in μg/L (mean ± SD; n = 3 per lake).
  - Dissolved Oxygen (DO) in %, pH, Temperature (T in °C), Conductivity (μS/cm).
- Additional elements and indicators:
  - A broader set of elements measured (see data structure for water_chem2.csv), reflecting a comprehensive water-quality profile.
- Cs-137 soil deposition data:
  - 137Cs deposition (kBq/m²) included as a deposition-related parameter.

## Analytical methods and QA/QC

- Major ions and trace elements:
  - Filtration: 0.2 μm, acidification to 2% v/v HNO3 (65% trace metal grade).
  - Instrumentation: Quadrupole ICP-MS (iCAPQ) with collision cell mode (KED) using 7% H2 in He to minimize interferences.
  - Sample introduction: Autosampler (Cetac ASX-520) with nebulizer (1 mL/min) and spray chamber.
  - Internal standards: Ge, Rh, Ir in 2% HNO3.
  - Calibration: Two multi-element calibration standards sets for major elements (0–30 mg/L) and trace elements (0–100 μg/L).
- Nutrients:
  - Filtration: 0.45 μm, preservation with 1% ZnCl2 (50% w/v).
  - Instrumentation: QuAAtro segmented flow nutrient analyser with autosampler.
  - Analysis performed according to standard procedures.
- Replication and data quality:
  - Reported mean ± SD with n = 3 per lake for major and trace elements, indicating triplicate sampling/measurement.
- Data structure documentation:
  - Detailed column descriptions and units/methodologies provided for each dataset to support data reuse and interoperability.

## Data structure and accessibility

- water_chem1.csv:
  - Contains lake-level metadata and physicochemical context (e.g., DO, pH, temperature, conductivity, maximum depth, surface area, distance from CNPP, 137Cs deposition).
  - Includes Lake and Geographical Region descriptors and location-specific attributes such as distance from CNPP and Cs deposition.
- water_chem2.csv:
  - Concentrations of major and trace elements (e.g., B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl).
  - Each row includes Date, SampleLabel/Quality Control, and concentration values in appropriate units (mg/L for many major elements; μg/L for trace elements).
- water_chem3.csv:
  - Nutrients and dissolved species concentrations (NO3/NO2, NO2, NO3, NO3/NO2 in mM, PO4 in mM, Dsi (dissolved silicate) in mM).
  - Includes Date and Sample identifiers/locations for traceability.

- Data structure documentation includes explicit column explanations and units to enable cross-study comparison and integration into monitoring frameworks.

## Implications for monitoring frameworks

- Demonstrates a comprehensive, QA-focused workflow for environmental health monitoring near a contamination gradient.
- Provides a rich, multi-parameter dataset (major/trace elements, nutrients, dissolved properties, deposition context) suitable for trend analysis and policy evaluation.
- Highlights the importance of:
  - Clear metadata and dataset structure to support data sharing and reuse.
  - Use of standardized, auditable analytical methods (ICP-MS with collision cell, QA steps, internal standards).
  - Replication (n = 3 per lake) to assess variability and improve confidence in inferences.
- The approach supports informing future monitoring decisions by illustrating how to capture spatial gradients, contamination context, and nutrient/chemical status in a coherent data package.

## Notes on data governance and practical considerations

- Detailed metadata and structured data files ease data discovery, interpretation, and integration into monitoring dashboards and reports.
- The documentation emphasizes transparency in methodology (filtration, preservation, calibration, QA) to ensure data reliability and comparability over time.
- Potential considerations for broader monitoring use include ensuring consistent data standards, timely access to data, and maintaining up-to-date metadata to support ongoing governance and policy evaluation.