# Experimental Design and Laboratory Incubation Method

## Overview
- Study design to assess microbial metabolic activity in river sediments using a resazurin-resorufin tracer system.
- Incubations across two geologies (Chalk, Sandstone), three substrate types (fine, medium, coarse), plus controls.
- Five incubation temperatures (5, 9, 15, 21, 26°C) with triplicate samples, yielding 105 observations and 21 observations per temperature.

## Experimental Design

- Sample sources and substrates
  - Sediment collected from upper 10 cm of two rivers: River Lambourn (Chalk) and River Tern (Sandstone) in Sept 2015.
  - Three substrate areas per river: silt under vegetation (fine), sand in unvegetated zones (medium), gravel in unvegetated zones (coarse).
  - Approximately 5 L per sample; six substrate treatments plus controls: Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse.
- Sample handling
  - Samples homogenised, sieved (0.8 cm for fine; 1.6 cm for medium and coarse), stored airtight, cold, dark until incubation.
- Incubation setup
  - 300 mL sediment + 500 mL ultrapure water per jar; controls received 500 mL ultrapure water only.
  - Jars incubated in sealed 1 L amber jars; incubated for five hours with sampling at zero and five hours.
  - Jars labeled 1–21: mapping corresponds to substrate treatments (1–3 Chalk fine, 4–6 Chalk medium, etc.).

## Measurements and Instrumentation

- Metabolic activity proxy
  - Resazurin-resorufin tracer system; resorufin production indicates microbial activity.
  - Initial addition: 5 mL of ~14.5–15.4 ppb resazurin to each jar.
  - Measurements: initial and after five hours for resorufin and related metrics.
- Instrumentation
  - CO2 and CH4: GC-FID (Agilent 7890A) with separation and calibration details.
  - Resorufin: GGUN-FL30 fluorometer with LED excitation (525 nm for resorufin, 570 nm for resazurin).
  - Dissolved oxygen: Pyro-science Firesting O2 sensor.
- Calibration and quality control
  - GC-FID: daily four-point calibration for CO2 and CH4; drift checks with external standards; blanks included.
  - Fluorometer: weekly three-point calibration (zero, 100 ng/L resorufin, mix of resorufin/resazurin); standard used to assess performance; detection limit ~1 ng/L.
  - Oxygen sensor: daily one-point calibration at 100% air saturation.
- Organic matter determination
  - Loss on ignition (LOI) methodology: 105°C drying, 550°C combustion for 6 hours, percentage mass loss to estimate organic matter.

## Data Structure and Metadata

- Data file
  - One CSV file: IncubationCO2_CH4_Resorufin_DO.
- Columns (nine)
  - Temperature (°C)
  - Jar (1–21)
  - Substrate_Type (Chalk fine/ Chalk medium/ Chalk coarse / Sandstone fine / Sandstone medium / Sandstone coarse; NA for controls)
  - Geology (Chalk or Sandstone; NA for controls)
  - Organic_Matter (%)
  - CO2 (mg C m^-2 h^-1)
  - CH4 (mg C m^-2 h^-1)
  - Resorufin (ng resorufin per µg resazurin per hour)
  - Dissolved_Oxygen (mg L^-1)
- Substrate classification
  - Chalk or Sandstone geology; Substrate_Type indicates particle size and vegetated vs unvegetated origin.
- Units and scale
  - Temperature: degrees Celsius
  - Organic matter: percent
  - Gas production: mg C m^-2 h^-1
  - Resorufin: ng per µg per hour
  - Dissolved oxygen: mg/L
- Provenance and references
  - Calibration and measurement references provided for traceability to methods cited (Lemke et al. on online fluorometry; Hoogsteen et al. for LOI).

## Provenance, Reproducibility, and References

- Detailed methodological context and calibration references
  - On-line fluorometry of reactive tracers in streams (Lemke et al., 2013)
  - Estimating soil organic carbon through LOI and ignition conditions (Hoogsteen et al., 2015)
- Documented labeling scheme links jars to substrate treatments, enabling traceability from raw measurements to treatment conditions.

## Data Stewardship Considerations

- Metadata completeness
  - Ensure metadata includes sampling coordinates, river/site identifiers, collection dates, and exact substrate preparation details.
  - Include instrument models, calibration curves, and QA/QC procedures to support auditability.
- Data quality and interoperability
  - Maintain explicit data dictionary with units, detection limits, and any data transformations.
  - Preserve raw measurements and processed values; note any corrections for drift or blanks.
- Dataset discoverability and governance
  - Store under a clear dataset title with authors, affiliations, and versioning.
  - Include licensing, data use restrictions, and citation guidance for downstream users.
- Practical guidance for reuse
  - Provide mapping of jar numbers to substrate_type and corresponding treatment conditions to enable re-analysis.
  - Document potential limitations (e.g., controlled lab incubation may not reflect in-situ conditions).