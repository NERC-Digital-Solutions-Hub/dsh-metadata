# Plant_microbe_microcosm_design.csv

- Purpose: describes the experimental design of a plant-microbe microcosm study to understand drought adaptation interactions between plants and root-associated bacteria across moisture environments.
- Experimental setup:
  - Materials: surface-sterilised Festuca ovina plant clones and sterilised rendzina soil; inocula from two Buxton climate treatments (drought-adapted and control-adapted).
  - Inocula: pooled Pseudomonas koreensis isolates or field-derived soil wash; both derived from Buxton drought or control treatments.
  - Design: factorial combination of two climate adaptations (drought, control) with two moisture environments (drought, well-watered), totaling eight main combinations; 176 microcosms + 32 no-plant controls; plus 16 spare microcosms and 3 sterilised-soil pots.
  - Duration: 19 weeks under an automatically ventilated polytunnel.
  - Measurements: weekly soil respiration and volumetric soil water content; additional datasets (enzyme activity, nutrient availability, plant size/morphology) collected from designated microcosms.
- Data structure elements (Metadata Table 1):
  - pot_no, potID, Clone full_ID, Festuca ancestry, Inoculation type, Microbial ancestry, Treatment, and spatial design fields (table, row, column).
  - Notes on design categories: Full, No plant control, Spare, probes.
- Key cross-links: designed to be merged with other dataset files via pot_no.
- Quality and governance considerations:
  - Randomisation applied to the experimental design.
  - Documentation supports traceability from design to measurements.

---

## Related datasets (descriptions and governance implications)

- Plant_microbe_microcosm_soil_respiration.csv
  - What it measures: CO2 efflux from soil and soil water content across 15 observation weeks (within 19 weeks total); includes soil temperature data for subset measurements.
  - Data structure: weekly observations with temporal blocks; metadata Table 2 defines week, date, temporal block, pot_no, swc, soil_temp, file_name, label, timestamp, efflux, and notes.
  - Instrumentation: Li-Cor Li-8100 IRGA and Li-Cor 8150 Multiplexer; ThetaProbe ML2x for soil moisture.
  - QC: temperature probe stabilization and sterilization procedures prior to measurement.
  - Cross-linking: pot_no used to join with design file and other datasets.

- Plant_microbe_microcosm_enzymes.csv
  - What it measures: extracellular enzyme activities (GLU, NAG, PHO) from control-treatment soils collected Feb 2021; analysis performed Aug 2021.
  - Methods: enzyme extraction (CaCl2, PVP, Tween 80), dialysis, concentration, and fluorescence-based activity assays; live vs boiled controls with 4 analytical replicates per enzyme per sample.
  - Calibration: fluorescence converted to activities (nMol g-1 h-1) using a standard curve and a defined equation.
  - Metadata Table 3 includes pot_no, sampling details, plate layout, and calculated enzyme activities.

- Plant_microbe_microcosm_sup_substrate.csv
  - What it measures: effects of substrate additions on soil CO2 efflux using MicroResp; substrates include glucose, ABA, malic acid, L-leucine, and water control.
  - Design: 3 analytical replicates per substrate per soil sample; pre-incubation and incubation steps with 570 nm absorbance readings to derive respiration rates.
  - Data handling: normalization (T6/T0) and calibration to CO2 percent using a laboratory calibration curve; subsequent efflux calculations incorporate soil weight, temperature, and other constants.
  - Metadata Table 4 documents plate, well, pot_no, substrate type, analytical_rep, and derived metrics (CO2_percent, efflux, mean_efflux, se_efflux).

- Plant_microbe_microcosm_sup_drought.csv
  - What it measures: drought and rewet dynamics on soil CO2 efflux using MicroResp across multiple days (day 1 drought, days 2–5 rewet).
  - Design: lab-imposed drought (15% WHC) followed by rewet; three analytical replicates per sample-substrate combination; days capture rewet trajectory.
  - Alignment: follows the MicroResp protocol in Ness_poly_lab_substrate.csv with noted modifications.
  - Metadata Table 5 captures MR_Treatment (control vs drought), day, plate/well details, and calculated efflux metrics (CO2_percent, calc, efflux, mean_efflux, se_efflux).

- Plant_microbe_microcosm_nutrient_supply.csv
  - What it measures: nutrient supply rates using PRS probes installed in each watered control microcosm; probes analyzed by Western Ag.
  - Data: sampleID, pot_no, burial/retrieval dates, anion/cation probe counts, and concentrations for N (total, NO3-N, NH4-N) and a suite of elements (Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd) with detection limits notes.
  - Metadata Table 6 lists all nutrient variables and notes on detection limits included in values.

- Plant_microbe_microcosm_plant_size_traits.csv
  - What it measures: non-invasive plant size traits over time (canopy area, maximum height, maximum width) via image analysis.
  - Data collection: two images per timepoint per microcosm; analysis performed with ImageJ; canopy area via convex hull.
  - Metadata Table 7 includes date, replicate, researcher, pot_no, and image-derived metrics (area, height, max_width) with corresponding file_area, file_height, file_width references.

- Plant_microbe_microcosm_plant_morphology_traits.csv
  - What it measures: six plant morphological traits measured once (June 2020 and March 2021) including leaf lengths, SLA, leaf area, biomass, inflorescences.
  - Methods: direct measurements (ruler, microscopy) and dry mass for SLA/biomass.
  - Metadata Table 8 provides pot_no and trait values (leaf lengths, regrowth, SLA, biomass, inflorescences).

---

## Metadata, interoperability, and governance notes

- Central linking key: pot_no is the primary identifier to merge all datasets with the design file and across measurements.
- Metadata coverage: each dataset includes a dedicated metadata table detailing fields, units, and intended data types; descriptions of design, measurement, and analysis steps are provided.
- Measurements and units: explicit units and calculation methods are described (e.g., enzyme activities in nMol g-1 h-1, CO2 efflux in μmol CO2 m-2 s-1 or μg CO2 g-1 h-1, SLA units, etc.).
- QC and instrumentation: each file documents quality control steps and instrumentation used, enabling reproducibility and auditability.
- Potential governance considerations for data stewards:
  - Ensure harmonized data dictionary across all files; map to a common ontology where possible (e.g., soil respiration, enzyme activity, PRS nutrient metrics).
  - Maintain robust versioning and clear data provenance, given multiple data collection phases, instruments, and calibration steps.
  - Track potential risk fields (e.g., pot-label_mismatch in respiration metadata) and implement data cleaning steps.
  - Plan for data sharing and portal ingestion by consolidating design and dataset metadata; ensure consistent field names and merge keys (pot_no, date, plate/well) across datasets.
  - Document licensing, data use agreements, and any embargo periods for sensitive datasets or ongoing experiments.

---

## Practical takeaways for data stewardship

- The collection comprises multi-modal, time-series data tied together by a single pot-based design, enabling integrated analyses of plant-microbe interactions under drought and moisture treatments.
- The data are well-documented at the file level with explicit metadata tables, instrumentation, and processing details, supporting discoverability and reproducibility.
- To maximize reusability, maintain strict adherence to the pot_no key across all datasets, enforce consistent unit usage, and publish a master data dictionary that aligns variable names and units across files.