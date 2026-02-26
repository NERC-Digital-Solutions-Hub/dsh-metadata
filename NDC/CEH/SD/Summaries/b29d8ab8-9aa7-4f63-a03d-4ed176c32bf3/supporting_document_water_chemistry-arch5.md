# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

## Overview
- Study of water chemistry in seven lakes near the Chernobyl Nuclear Power Plant, spanning Belarus and Ukraine, collected during 2014–2016.
- Lakes categorized by contamination level: Glubokoye, Yanovsky, Cooling Pond (high); Svyatoye (medium); Stoyacheye, Dvoriche, Gorova (low).
- Data cover major alkali/alkali-earth elements, trace elements, nutrients, and physico-chemical parameters in surface water.

## Datasets included
- water_chem1.csv
  - Variables describing lake identity and physico-chemical context: lake name, region, dissolved oxygen, pH, temperature, conductivity, max depth, surface area, distance from CNPP, and Cs-137 deposition.
- water_chem2.csv
  - Major and trace element concentrations (e.g., B, Na, Mg, P, S, K, Ca and many trace elements) with units (mg/L or μg/L) and metadata descriptions per column.
- water_chem3.csv
  - Nutrients and related species in millimolar units: NO3/NO2, NO2, NO3, PO4, Dsi, with sample dates and sample labels.
- Overall, data describe both elemental concentrations (major and trace) and inorganic nutrients, plus site and environmental context.

## Methodology and QA/QC
- Sample preparation and chemical analysis
  - Filtration through 0.2 μm (for ICP-MS) and acidification with 2% v/v HNO3 (65% trace metal grade).
  - ICP-MS analysis (iCAPQ; Thermo Scientific) with collision cell mode (7% H2 in He) and kinetic energy discrimination to reduce interferences.
  - Autosampler and nebuliser for sample introduction; internal standards (Ge, Rh, Ir) in 2% HNO3.
  - External multi-element calibration standards for major elements (0–30 mg/L) and trace elements (0–100 μg/L).
  - Additional filtration through 0.45 μm filtration for inorganic macronutrients measured by QuAAtro segmented flow analyser.
  - Preservation of nutrients with 1% ZnCl2 solution (50% w/v).
- Documentation and QA/QC
  - Detailed methodological notes accompany the data, including units, measurement technique, and data structure for each dataset.

## Data structure and metadata
- water_chem1.csv
  - Columns include lake identity, region, DO (%), pH, temperature (°C), conductivity (μS/cm), max depth (m), surface area (km2), distance from CNPP (km), and 137Cs deposition (kBq/m2).
- water_chem2.csv
  - Contains concentrations of numerous elements (e.g., B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl) with units mg/L or μg/L and accompanying explanations for each column.
- water_chem3.csv
  - Includes date, sample label, and concentrations of nutrients and dissolved silicate in millimolar units (NO3/NO2, NO2, NO3, PO4, Dsi).

## Data governance, availability, and reuse
- The documentation supports discoverability and reuse by providing clear metadata, measurement methods, and units, aiding interoperability and data integration.
- Data are time-bounded (2014–2016) and region-specific (Belarus and Ukraine near CNPP); users should consider context of sample timing and hydrological status when comparing sites or across time.
- As per data stewardship best practices, ensure proper data provenance, versioning, and any sharing restrictions are respected; dataset structure is designed to facilitate uploading to data portals and catalogue systems.

## Potential data quality and access considerations
- Complex, heterogeneous data formats and large, multi-file sets may pose integration challenges across systems.
- Ensuring timely data availability from producers and alignment of metadata with user needs can require ongoing coordination.
- Some datasets may involve safety considerations due to their proximity to contaminated sites; appropriate handling and documentation of any access or usage restrictions is recommended.