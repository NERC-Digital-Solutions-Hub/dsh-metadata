# Water chemistry of seven Belarus and Ukraine lakes (2014-2016)

- Study area and context:
  - Seven lakes in Belarus and Ukraine located 1.5–225 km from the Chernobyl Nuclear Power Plant (CNPP).
  - Contamination levels by lake: Glubokoye, Yanovsky, Cooling Pond are high (H); Svyatoye is medium (M); Stoyacheye, Dvoriche, Gorova are low (L).
  - Map of sampling sites referenced (Fig. 1).

- Lakes and spatial/physical characteristics:
  - Lakes: Glubokoye, Yanovsky, Cooling Pond (H); Svyatoye (M); Stoyacheye, Dvoriche, Gorova (L).
  - Recorded properties per lake include distance from CNPP, surface area, maximum depth, and 137Cs soil deposition (Cs deposition).

- Measured chemical constituents and time frame:
  - Major alkali and alkali-earth elements: Na, Mg, S, K, Ca (mg/L; mean ± SD, n = 3 per lake).
  - Trace elements: As, Sr, Cd, Cs, Pb, U (μg/L; mean ± SD, n = 3 per lake).
  - Nutrients and other physicochemical parameters: NO3-, NO2-, PO4 3- (μg/L; mean ± SD, n = 3 per lake); dissolved oxygen (DO, %), pH, temperature (T in °C), conductivity (μS/cm).
  - Sampling period: 2014–2016; surface water samples collected and analyzed.

- Methods and data integrity:
  - Sample preparation: filtration (0.2 μm for metals; 0.45 μm for nutrients) and acidification with 2% HNO3 for ICP-MS analyses; preservation with 1% ZnCl2 for nutrients.
  - Instruments and protocols: quadrupole ICP-MS (Model iCAPQ) with collision cell mode (CCTED) using 7% H2 in He; autosampler with nebuliser; internal standards Ge, Rh, Ir.
  - Calibration: two external multi-element calibration standards (major elements 0–30 mg/L; trace elements 0–100 μg/L).
  - Nutrient analysis: QuAAtro segmented flow nutrient analyser.
  - Quality assurance: standard procedures for ICP-MS and nutrient analyses; replicates reported as n = 3 per lake for major/trace elements and nutrients.

- Data files and structure (CSV datasets):
  - water_chem1.csv:
    - Columns include Lake, Lake region, DO (%), pH, T (°C), Conductivity (μS/cm), Max_depth (m), Surface (km2), Distance_from_CNPP (km), 137Cs_deposition (kBq/m2).
  - water_chem2.csv:
    - Columns list elemental concentrations in mg/L for B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, Li, Be, Tl.
  - water_chem3.csv:
    - Columns include Date, Sample, NO3/NO2_Conc_mM (nitrates/nitrite overall), NO2Conc_mM, NO3Conc_mM, PO4_Conc_mM, Dsi_Conc_mM (dissolved silicate).
  - Notes: water_chem2 and water_chem3 include additional metadata such as SampleLabel or Sample descriptions and units/methodology details in the column definitions.

- How this data supports GIS and map-based analysis:
  - Enables spatial visualization of contaminant distributions and lake chemistry relative to CNPP distance and Cs deposition.
  - Supports comparisons across lakes with differing contamination levels (H, M, L).
  - Data can be joined with geographic coordinates to create layered maps showing major/trace element concentrations, nutrients, and physico-chemical parameters over time.
  - Provides structured metadata and explicit units, aiding data standardization and integration with other GIS datasets.