# Determination of Suspended Particulate Matter (SPM) in Seawater

## Purpose and scope
- Protocol to quantify suspended particulate matter in water and, if desired, separate into organic and inorganic fractions.
- Outputs include particulate concentration in mg/L (and optionally mg/m³), and, for split analyses, organic and inorganic contributions (CO and CI).
- Key data elements: W1 (initial filter weight), W2 (filter with particulates), W3 (filter with inorganic after ignition), V (volume filtered), X (blank correction), derived concentrations CS P M, CI, CO.
- Emphasizes data provenance, traceability, and reproducibility through documented steps, equipment, and correction factors.

## Data collection and measurement process
- Equipment and consumables: drying oven, muffle furnace, 47 mm GF/F filters, balance (0.01 mg, 5 d.p.), desiccator, filtration manifold, vacuum pump, forceps, measuring cylinders, sample bottles, trays, bags, distilled water.
- Filter preparation
  - Harden and rinse filters; dry at 75 °C; cool in desiccator.
  - Weigh each filter and dish (W1) rapidly to 0.01 mg; store weighed filters in sealed bags until use.
- Filtration procedure
  - Collect water samples in bottles; filter as soon as possible; store at <4 °C if delayed.
  - Place weighed filter (W1) on the filter base; filter a volume until adequate particulate matter is captured (typically until clogging, aiming for ~2 mg of material; ocean 2–5 L, coast 0.5–1 L; volume is V).
  - Rinse solids and filter margins; remove and store dried filter promptly in freezer until drying.
- Determination of blanks
  - Use at least three blank filters per batch to determine mean blank correction X = mean(W2) − mean(W1); X may be ± but should not exceed 0.5 mg.
- Field duplicates
  - Collect two simultaneous samples under identical conditions to assess field/sample handling and lab procedure precision.
- Filter drying and SPM calculation
  - Dry filters (W2) at 75 °C for 1 h, then cool and weigh to 0.01 mg.
  - Compute SPM concentration: CS P M = (W2 − W1 + X) / V (mg/L). Multiply by 1000 to convert to mg/m³.
- If organic/inorganic split is required
  - Ignite filters at 500 °C for 3 h; weigh as W3 (inorganic fraction plus initial filter).
  - Atomic inorganic concentration: CI = (W3 − W1) / V.
  - Organic concentration: CO = (W2 − W3) / V.
  - Note weight units: W1, W2, W3 in mg; V in L; convert weights from g to mg as needed in calculations.

## Data quality, metadata, and governance considerations
- Data provenance and traceability
  - Record all weights (W1, W2, W3 where applicable), V (volume filtered), X (blank correction), date/time, sample ID, filter ID, and processing steps.
  - Document drying/ignition conditions (75 °C, 500 °C durations), storage conditions (freezer), and equipment used (models if possible).
- Metadata and data model suggestions
  - Core fields: sample_id, batch_id, date_collected, time_collected, location, sample_type (ocean/coastal), V, W1, W2, W3, X, CS_P_M, CI, CO, units, method_version, QA/QC flags (duplicate of field/lab, blank results).
  - Derived fields: CS_P_M_mg_per_L, CS_P_M_mg_per_m3, CI_mg_per_L, CO_mg_per_L.
  - QA indicators: field_duplicate_flag, blank_count, blank_mean, weight_precision (0.01 mg), weight-change considerations due to hygroscopicity.
- Data handling and sharing
  - Preserve raw weights (W1, W2, W3) and processed results; store raw data alongside derived results.
  - Include references to standard methods and any deviations; maintain versioning of method and calibration details.
  - Ensure data formats support units and conversions (mg, g, mL, L) and explicit V, so calculations are reproducible.
- Potential challenges to manage
  - Incomplete understanding of user needs for dataset scope (organic vs inorganic split) and reporting units.
  - Timely acquisition of data from field or labs and reconciliation across multiple systems/formats.
  - Interoperability across equipment and units; ensure consistent metadata and documentation.

## Computation details and unit handling
- Key equations
  - CS P M = (W2 − W1 + X) / V (mg/L); multiply by 1000 to obtain mg/m³.
  - CI = (W3 − W1) / V (mg/L).
  - CO = (W2 − W3) / V (mg/L).
- Unit notes
  - W1, W2, W3 are in mg; V is in L (convert as needed).
  - If initial weights were in g, multiply by 1000 to convert to mg; V in mL is converted to L by dividing by 1000.
  - Maintain explicit units in all data records to prevent conversion errors.
- Practical data considerations
  - X (blank correction) is bounded by ±0.5 mg; apply to final CS P M calculation.
  - Field duplicates provide a measure of overall precision from collection to analysis.

## References
- Strickland, J.D.H., Parsons, T.R. (1972) A Practical Handbook of Seawater Analysis, Fish Res. Board Canada, Bulletin 167.
- Radojevic, M., Bashkin, V.N. (1999) Practical Environmental Analysis, Royal Society of Chemistry.