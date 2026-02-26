# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

## Overview
- Seven lakes near the Chernobyl Nuclear Power Plant (CNPP), located 1.5 to 225 km from CNPP.
- Lakes categorized by contamination: Glubokoye, Yanovsky, and Cooling Pond (high); Svyatoye (medium); Stoyacheye, Dvoriche, Gorova (low).
- Study presents major alkali and alkali-earth element concentrations and selected trace elements in surface water during 2014–2016.
- Includes hydrological parameters, nutrient levels, and Cs deposition for context of radionuclide influence.

## Sampling and Analytical Methods
- Water samples filtered through 0.2 μm, acidified with 2% v/v HNO3 (65% trace metal grade) for ICP-MS analysis.
- Major elements (Na, Mg, S, K, Ca) and trace elements (As, Sr, Cd, Cs, Pb, U) measured by quadrupole ICP-MS (iCAPQ, Thermo Scientific) with collision cell mode (7% H2 in He) and kinetic energy discrimination.
- Samples analyzed with an autosampler (Cetac ASX-520) and a nebuliser (1 mL/min); internal standards Ge, Rh, Ir in 2% HNO3 used for bias correction.
- Two external multi-element calibration standards prepared for major elements (0–30 mg/L) and trace elements (0–100 μg/L).
- Nutrients (NO3–, NO2–, PO4 3–) measured after filtration through 0.45 μm and preservation with 1% ZnCl2 (50% w/v). Analysis conducted with a QuAAtro segmented flow nutrient analyser (SEAL Analytical) following standard procedures.

## Parameters and Data Collected
- Major elements (mg/L): Na, Mg, S, K, Ca.
- Trace elements (μg/L): As, Sr, Cd, Cs, Pb, U; a broader suite listed in data structure (e.g., V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ag, Cd, Ba, Li, Be, Tl, etc. in water_chem2.csv).
- Nutrients (μg/L): NO3−, NO2−, PO4 3−; dissolved silicate (Dsi) in millimolar.
- Physicochemical parameters: Dissolved Oxygen (DO %), pH, temperature (°C), conductivity (μS/cm); maximum depth; surface area.
- Hydrological context: distance from CNPP (km) and 137Cs soil deposition (kBq/m2).
- Sample structure: Data are organized into three CSVs (water_chem1.csv, water_chem2.csv, water_chem3.csv) detailing lake-level context, sample-specific concentrations, and nutrient/ion concentrations, respectively.
  - water_chem1.csv: lake identity, region, DO, pH, temperature, conductivity, max depth, surface area, distance from CNPP, 137Cs deposition.
  - water_chem2.csv: sample-level concentrations for a broad panel of elements (B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl) with corresponding sample metadata.
  - water_chem3.csv: date, sample label, nitrate/nitrite and phosphate concentrations (NO3/NO2, NO2, NO3, PO4) in millimolar, and dissolved silicate (Dsi) in millimolar.

## Data Quality and Structure
- Replicates: n = 3 per lake for major and trace element measurements.
- Data are presented as mean ± SD where indicated.
- Data structures are explicitly defined to support standardized data ingestion and cross-lake comparisons.

## Purpose and Use
- Provides a consistent, monitor-ready dataset to assess environmental health and policy performance related to lake water chemistry and radionuclide influence in the Chernobyl region.
- Enables time-series analyses and inter-lake comparisons using standardized methodologies and outputs (concentrations of major/trace elements and nutrients, and supporting hydrological context).
- Aligns with monitoring workflows by detailing data structure and ensuring potential integration with other datasets and portals for broader accessibility.