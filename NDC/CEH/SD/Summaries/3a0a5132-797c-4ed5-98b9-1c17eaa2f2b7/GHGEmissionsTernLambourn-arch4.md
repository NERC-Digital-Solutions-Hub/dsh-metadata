# Experimental Design and Laboratory Incubation Method

## Overview
- Studies microbial metabolic activity in sediment from two river geologies (Chalk and Sandstone) across six substrate types (Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse) plus controls.
- Experimental setup: five incubation temperatures (5, 9, 15, 21, 26°C), 300 ml sediment with 500 ml ultrapure water per jar, sealed jars, incubated for five hours with sampling at zero and five hours.
- Data collected per jar include substrate type, geology, temperature, organic matter content, and production rates of CO2, CH4, resorufin, plus final dissolved oxygen.

## Experimental Design and Substrates
- Substrates: Chalk and Sandstone geologies, each with fine (under vegetation), medium (unvegetated sand-dominated), and coarse (unvegetated gravel-dominated) classifications.
- Treatments: 7 per temperature (6 substrate types + 1 control), in triplicate, yielding 21 observations per temperature and 105 observations total.
- Jar labeling: Jars 1-3 = Chalk fine triplicates, 4-6 = Chalk medium triplicates, etc.

## Incubation Conditions and Procedure
- Incubation vessels: 1 L amber jars with 300 ml sediment and 500 ml ultrapure water; controls receive 500 ml water only.
- Sampling: initial (0 hours) and after 5 hours; headspace gas sampled; jars dried for sediment property analysis afterward.
- Key measurements during incubation: resazurin-resorufin tracer system to track microbial activity; CO2, CH4, resorufin, and DO are recorded.

## Measurements and Instrumentation
- CO2 and CH4: Gas chromatograph–flame ionisation detector (GC-FID). Methane detected directly; carbon dioxide methanised prior to detection.
- Resorufin: On-line fluorometer (GGUN-FL30) with excitation at 525 nm for resorufin and 570 nm for resazurin.
- Dissolved Oxygen: Pyro-science Firesting fixed-needle oxygen sensor.
- Organic matter: Loss on ignition (LOI) determined from sediment combusted at 550°C after drying at 105°C.

## Calibration and Data Quality
- GC-FID: Daily four-point CO2/CH4 calibration (zero, 1051, 525.5, 262.8 ppm CO2 and zero, 9.8, 4.9, 2.5 ppm CH4); drift checks with external standards; accuracy and detection limits reported.
- Fluorometer: Weekly three-point calibration (zero, 100 ppb resorufin, 50/50 mix of resorufin/resazurin); standard used to verify performance; LOD ~1 ppb resorufin.
- Oxygen sensor: Daily one-point calibration at 100% air saturation.
- Data used for downstream analyses include calibration-derived concentrations, with explicit instrument performance metrics provided.

## Data Recorded and Units
- Temperature: degrees Celsius (incubation temperature)
- Jar: jar identifier (1–21, with mapping to substrate type)
- Substrate_Type: Chalk or Sandstone classification and fine/medium/coarse
- Geology: Chalk or Sandstone origin; NA for controls
- Organic_Matter: percent
- CO2: milligrams of carbon per square metre per hour
- CH4: milligrams of carbon per square metre per hour
- Resorufin: nanograms of resorufin per microgram of resazurin per hour
- Dissolved_Oxygen: milligrams per litre

## Structure and Data Access
- Data file: IncubationCO2_CH4_Resorufin_DO.csv
- Columns: Temperature, Jar, Substrate_Type, Geology, Organic_Matter, CO2, CH4, Resorufin, Dissolved_Oxygen
- Notes: Control samples indicated by NA in Geology; substrate-type mapping aligned with jar numbering.

## Provenance and References
- References for methods:
  - On-line fluorometry of tracers in streams (Lemke et al., 2013)
  - Estimating soil organic carbon through LOI (Hoogsteen et al., 2015)

## Implications for Data Strategy
- Rich, multi-factor design across geology, substrate, and temperature suitable for modeling microbial respiration and greenhouse gas production under varied sediment conditions.
- Clear, well-documented calibration, measurement, and data-recording protocols support reproducibility and comparability.
- Metadata: explicit treatment mapping, units, and NA handling for controls facilitate data discoverability and integration with broader data ecosystems.