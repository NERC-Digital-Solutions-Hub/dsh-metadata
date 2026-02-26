# Plant_microbe_microcosm_design.csv

- Purpose: describe the experimental design of a plant-microbe microcosm study aimed at understanding how drought adaptation in plants and their root-associated bacteria interact under different moisture environments.
- Experimental system:
  - Plant: Festuca ovina clones (surface-sterilised).
  - Microbes: pooled population of Pseudomonas koreensis isolates or field-derived soil wash (intact microbial community).
  - Soil: sterilised Rendzina soil.
  - Origins: materials from Buxton Climate Change Impacts Lab (Buxton) drought treatment (drought-adapted) or control treatment (control-adapted).
- Experimental design:
  - Two climate treatments (drought-adapted vs control-adapted) combined factorially with two moisture environments (drought vs well-watered), yielding eight plant-microbe climate adaptation combinations and two moisture levels.
  - Total microcosms: 176 in the main experiment plus 32 no-plant controls; plus 16 spare microcosms and 3 soil-only pots.
  - Setting: automatically ventilated polytunnel; duration: 19 weeks.
- Measurements and data streams:
  - Weekly soil respiration (CO2 efflux) and soil volumetric water content.
  - Soil temperature recorded with CO2 measurements.
  - Selected datasets collected Feb 2021 for enzymes, substrate use, lab drought resistance, nutrient probes, and plant growth traits.
- Metadata highlights:
  - pot_no and potID identify microcosm pots; design categories include Full, No plant control, Spare, and probes.
  - Clonal and microbial ancestry, inoculation type, and treatment details captured for linking datasets.
- Quality and data flow:
  - Randomisation used to validate experimental design.
  - Data intended to be stored and uploaded to appropriate data portals; underlying datasets intended to be accessible for broader use. 

## Key variables and data categories (linked datasets)

- pot and clone identifiers, ancestry, inoculation type, and treatment details (Design metadata).
- Plant_microbe_microcosm_soil_respiration.csv: weekly CO2 efflux, soil water content, soil temperature, and related file metadata across two temporal blocks over 19 weeks.
- Plant_microbe_microcosm_enzymes.csv: extracellular enzyme activities (GLU, NAG, PHO) with extraction, assay, replicates, and calibration details.
- Plant_microbe_microcosm_sup_substrate.csv: substrate-induced respiration using MicroResp, including substrates (glucose, ABA, malic acid, L-leucine, water), triplicate measurements, and data normalization/calibration steps.
- Plant_microbe_microcosm_sup_drought.csv: drought and rewet experiments on soil CO2 efflux, detailing lab-imposed drought progression and rewetting timepoints.
- Plant_microbe_microcosm_nutrient_supply.csv: PRS probe-derived nutrient supply rates (N, NO3-N, NH4-N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd) with sample metadata and notes.
- Plant_microbe_microcosm_plant_size_traits.csv: non-invasive image-based plant size metrics (canopy area, height, width) across time with image-derived measurements and replication notes.
- Plant_microbe_microcosm_plant_morphology_traits.csv: morphometric traits measured once per pot (leaf lengths, SLA, biomass, regrowth, inflorescences) across specified dates.

## Experimental procedures and instrumentation (highlights)

- Soil respiration and moisture:
  - Instrumentation: Li-Cor Li8100 IRGA and Li-Cor 8150 Multiplexer; ThetaProbe ML2x for soil moisture; temperature measurements with CO2 readings.
  - Timeframe: weekly observations in 15 weeks across 19 weeks; temperature probes calibrated per measurement batch.
- Enzyme assays:
  - Target enzymes: GLU (β-glucosidase), NAG (N-acetylglucosaminidase), PHO (phosphatase).
  - Extraction protocol with CaCl2-based extract, dialysis, and fluorescence-based detection (96-well plates; 25°C; 3-hour incubation).
  - Readout: fluorescence; conversion to activity using a standard curve with live vs boiled controls for each enzyme.
- Substrate-induced respiration (MicroResp):
  - Substrates: glucose, ABA, malic acid, L-leucine, and water control.
  - Procedure: soil prep, pre-incubation at 20°C, substrate addition, incubation, 570 nm absorbance read to infer CO2 efflux; normalization against blanks and baseline.
  - Data processing: CO2_percent calibration and efflux calculation incorporating soil weight, headspace, and temperature factors.
- Drought and rewet experiments:
  - Lab-imposed drought on dried samples to 15% soil water content, followed by rewetting; MicroResp-based respiration measured across days 1–5 to track rewetting dynamics.
- Plant nutrient and growth traits:
  - PRS probes to measure in-situ nutrient supply rates (N species: NO3-N, NH4-N; macro- and micronutrients).
  - Image-based plant size monitoring and classical morphometrics (leaf lengths, SLA, biomass, inflorescences).

## Data quality and controls

- Randomisation implemented in design.
- Multiple analytical replicates per measurement (e.g., enzyme assays, respiration substrates, MicroResp replicates).
- Controls include boiled enzyme samples, blanks, and lab controls in drought experiments.
- Calibration and data transformation steps documented for enzyme activities and CO2 efflux calculations.

## References

- Campbell et al. (2003). Microtiter plate method for measuring CO2 evolved from carbon substrate amendments.
- Creamer et al. (2009). Inter-laboratory comparison of multi-enzyme and substrate-induced respiration assays.