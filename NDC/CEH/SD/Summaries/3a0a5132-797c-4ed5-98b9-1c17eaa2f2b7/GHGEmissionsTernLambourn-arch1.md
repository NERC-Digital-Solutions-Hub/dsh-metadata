# Experimental Design and Laboratory Incubation Method

- Objective and scope: Experimental incubation to assess microbial metabolic activity and gas production (CO2, CH4) across substrate types and temperatures using a resazurin-resorufin tracer system, with measurements of dissolved oxygen as an additional indicator.

- Sampling locations and substrates:
  - Sediment collected from the upper 10 cm of two river types in September 2015:
    - Chalk river: River Lambourn, Berkshire (Centre for Ecology and Hydrology's River Lambourn Observatory, Boxford)
    - Sandstone river: River Tern, Shropshire
  - Three substrate areas per site:
    - Fine: silt-dominated sediment under vegetation
    - Medium: sand-dominated sediment from unvegetated zones
    - Coarse: gravel-dominated sediment from unvegetated zones
  - Substrate treatments (six total): Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse
  - Controls: 500 mL ultrapure water only (no sediment)

- Incubation setup:
  - Temperature treatments: 5, 9, 15, 21, and 26°C
  - Containers: 300 mL sediment + 500 mL ultrapure water in sealed 1 L amber jars
  - Replication: Each substrate treatment at each temperature in triplicate (21 observations per temperature; 105 observations total)
  - Sampling times: Zero hours and after five hours of incubation
  - Jar labeling: Jars 1–3 Chalk fine; 4–6 Chalk medium; 7–9 Chalk coarse; 10–12 Sandstone fine; 13–15 Sandstone medium; 16–18 Sandstone coarse; 19–21 controls (as per Substrate_Type mapping)

- tracer system and measurements during incubation:
  - Resazurin-resorufin tracer used to proxy microbial metabolic activity
  - At zero hours: add 5 mL of 14.5–15.4 ppb resazurin to water column; initial resorufin and dissolved oxygen measured; headspace gas sample collected
  - After five hours: repeat resorufin measurement and headspace sampling

- Instrumentation and measurements:
  - Carbon dioxide and methane: Agilent 7890A GC-FID (methane detected after methanisation of CO2); calibration and drift correction described
  - Resorufin: GGUN-FL30 fluorometer (customized; excitation at 525 nm for resorufin, 570 nm for resazurin)
  - Dissolved oxygen: Pyro-Science Firesting fixed needle-type sensor

- Calibration and validation details:
  - GC-FID calibration: daily four-point standards for CO2 (0, 1051, 525.5, 262.8 ppm) and CH4 (0, 9.8, 4.9, 2.5 ppm); drift correction using periodic standard analyses; accuracy and LOD specified
  - Fluorometer calibration: weekly three-point calibration (zero, 100 ppb resorufin, 50/50 mix of resorufin/resazurin); additional standard 93.1 ppb resorufin for performance; LOD ~1 ppb resorufin
  - Oxygen sensor: daily one-point calibration at 100% air saturation

- Data and variables recorded:
  - Temperature: incubation temperature (°C)
  - Jar: jar identifier (1–21)
  - Substrate_Type: Chalk or Sandstone, with subcategories fine, medium, coarse
  - Geology: origin geology (Chalk or Sandstone); NA for controls
  - Organic_Matter: sediment organic matter content (%)
  - CO2: carbon dioxide production (mg C m^-2 h^-1)
  - CH4: methane production (mg C m^-2 h^-1)
  - Resorufin: resorufin production (ng resorufin per μg resazurin per hour)
  - Dissolved_Oxygen: dissolved oxygen in water column at end of incubation (mg L^-1)

- Dataset structure and file details:
  - One CSV file: IncubationCO2_CH4_Resorufin_DO
  - Nine columns: Temperature, Jar, Substrate_Type, Geology, Organic_Matter, CO2, CH4, Resorufin, Dissolved_Oxygen
  - Substrate_Type coding aligns with Chalk or Sandstone and particle-size class (fine/medium/coarse)
  - Substrate labeling and triplicate organization described for traceability
  - References supporting methods for LOI and online fluorometry included

- Notes on data interpretation and context:
  - The dataset enables analysis of how microbial metabolic activity (via resorufin proxy) and gas production (CO2/CH4) respond to temperature, substrate type, and geologic origin
  - Includes both vegetated and unvegetated sediment contexts through substrate differentiation
  - Data quality considerations include calibration accuracy, detection limits, and drift corrections as documented
  - Organic matter content obtained via loss on ignition (reference methods provided) for potential covariate analyses