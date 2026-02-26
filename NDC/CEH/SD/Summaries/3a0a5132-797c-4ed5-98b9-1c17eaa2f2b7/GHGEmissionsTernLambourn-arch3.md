# Experimental Design and Laboratory Incubation Method

- Purpose
  - To assess microbial metabolic activity in river sediments using a resazurin-resorufin tracer system and to quantify carbon dioxide and methane production, resorufin production, and dissolved oxygen under controlled sediment types and temperatures.
  - Data intended to inform environmental monitoring and interpretation of microbial processes across substrate types and thermal conditions.

- Sampling and Substrate Preparation
  - Sediment collected from the upper 10 cm of the streambed from two rivers: Chalk River Lambourn (Berkshire) and Sandstone River Tern (Shropshire) in September 2015.
  - Three samples per river from distinct sediment zones:
    - Chalk: fine (silt underneath vegetation), medium (sand-dominated unvegetated zones), coarse (gravel-dominated unvegetated zones)
    - Sandstone: fine, medium, coarse as above
  - Each sample ~5 litres; samples homogenised, sieved (0.8 cm for fine, 1.6 cm for medium and coarse), stored airtight, cold, dark until incubation.
  - Resulting seven substrate treatments: Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse, plus controls.

- Incubation Design
  - Temperature treatments: 5, 9, 15, 21, 26°C.
  - Incubation setup: 300 ml sediment with 500 ml ultrapure water in sealed 1 L amber jars; controls received 500 ml ultrapure water only.
  - Substrate treatments replicated in triplicate, yielding 21 observations per temperature, 105 observations total.
  - Sampling times: zero hours and after five hours of incubation.
  - Jars are labeled 1–21 to correspond to substrate treatments (e.g., Jars 1–3 Chalk fine, 4–6 Chalk medium, etc.); Substrate_Type column records the treatment.

- Tracer System and Measurements
  - Use of resazurin-resorufin ‘smart’ tracer to gauge microbial metabolic activity.
  - Procedure: add 5 ml of 14.5–15.4 ppb resazurin solution to each jar; initial concentrations measured; headspace gas sampled; DO measured; after five hours, samples re-collected for analysis.
  - Primary metrics: resorufin production (proxy for metabolic activity), CO2 and CH4 production, and DO.

- Instrumentation and Calibration
  - Carbon dioxide and methane: Agilent 7890A gas chromatograph with flame ionisation detector (GC-FID).
  - Resorufin: GGUN-FL30 fluorometer with LED excitation (525 nm for resorufin; 570 nm for resazurin).
  - Dissolved oxygen: Pyro-science Firesting fixed-needle oxygen sensor.
  - Calibration details:
    - GC-FID: four-point calibration for CO2 (0, 1051, 525.5, 262.8 ppm) and CH4 (0, 9.8, 4.9, 2.5 ppm); drift correction using periodic external standard gas; occasional pure nitrogen blanks.
    - Fluorometer: three-point calibration (zero; 100 ppb resorufin; 50/50 mix of resorufin/resazurin at 50 ppb each) plus a 93.1 ppb resorufin standard for instrument performance; limit of detection ~1 ppb resorufin; measurements taken every 10 s with 2 min per sample.
    - Oxygen sensor: daily one-point calibration at 100% air saturation in air.
  - Calibration performance metrics provided (accuracy, precision, limits of detection) for both GC-FID and fluorometer.

- Recorded Variables and Units
  - Temperature: degrees Celsius
  - Jar: integer identifier
  - Substrate_Type: Chalk or Sandstone with fine, medium, or coarse designation
  - Geology: Chalk or Sandstone; NA for control experiments
  - Organic_Matter: percent
  - CO2: milligrams of carbon per square metre per hour
  - CH4: milligrams of carbon per square metre per hour
  - Resorufin: nanograms of resorufin per microgram of resazurin per hour
  - Dissolved_Oxygen: milligrams per litre

- Data Structure and Recording
  - Single CSV dataset titled IncubationCO2_CH4_Resorufin_DO with nine columns:
    - Temperature, Jar, Substrate_Type, Geology, Organic_Matter, CO2, CH4, Resorufin, Dissolved_Oxygen
  - Geology NA indicates no geology (control)
  - References for methods and calibration are provided:
    - Lemke et al. on online fluorometry for tracers in streams
    - Hoogsteen et al. on loss on ignition for soil organic carbon

- Analytical Methods Summary
  - Gas chromatography: 60°C oven, FID detection; methane elutes at ~3.5 min, CO2 at ~5.7 min; run time ~7 min; methane quantified after methanation of CO2 as needed.
  - Resorufin measurements: online fluorometer with careful chamber sealing to prevent light interference; data captured at 10 s intervals and averaged per sample.
  - Organic matter determination: loss on ignition (dry at 105°C, weigh, combust at 550°C for 6 h, weigh again) to estimate organic content.
  - Data handling: dataset structure supports traceability of temperature, substrate, geology, and all measured gas and tracer parameters.

- Data Provenance and Context for Monitoring Frameworks
  - Demonstrates comprehensive data quality controls (calibration, blanks, drift checks) and explicit metadata (substrate type, geology, organic matter).
  - Provides a reproducible, well-documented data structure suitable for monitoring frameworks seeking transparent methods, standardized instruments, and clear data governance pathways.