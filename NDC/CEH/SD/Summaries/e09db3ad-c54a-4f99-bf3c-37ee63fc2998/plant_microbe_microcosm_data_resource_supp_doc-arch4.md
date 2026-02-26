# Plant_microbe_microcosm_design.csv

- Purpose: Describes the experimental design of a plant–microbe microcosm study to understand how drought adaptation in plants and their root-associated bacteria interact under different moisture environments.

- Experimental setup
  - Pools of bacterial isolates (Pseudomonas koreensis) or field-derived soil wash inoculated into microcosms containing surface-sterilised Festuca ovina clones and sterilised rendzina soil.
  - Inocula derived from drought-adapted Buxton Climate Change Impacts Lab (BCCIL) or control-adapted Buxton material.
  - A single pooled bacterial population and a single soil wash from each climate treatment used per Buxton cohort; 11 drought- and 11 control-ancestry plant clones (total 22 clones).
  - Full factorial design: drought vs well-watered (two moisture environments) × drought- vs control-adapted plant-microbe combinations (eight main combinations).
  - Additional 32 microcosms without plants (no-plant controls) and 16 spare microcosms; three pots contained sterilised soil only.
  - Experiment duration: 19 weeks in an automatically ventilated polytunnel.

- Data collection context
  - Weekly soil respiration and volumetric soil water content monitoring.
  - Plant and microbial physiology, growth traits, and nutrient data collected through various timepoints and methods (see associated files).

- Metadata and data linkage
  - Metadata table fields include pot number, clone identity, Festuca ancestry, inoculation type, microbial ancestry, treatment, and spatial/blocking information.

- Key data relationships
  - Pot-level IDs (pot_no) link to multiple datasets describing soil respiration, enzyme activity, substrate responses, plant traits, and nutrient measures.
  - Distinct treatment combinations across climate adaptation, moisture environment, and plant-microbe pairings are traceable through the metadata.

- Associated datasets (overview of what they contain)
  - Plant_microbe_microcosm_soil_respiration.csv: CO2 efflux and soil moisture/temperature measurements across microcosms and time.
  - Plant_microbe_microcosm_enzymes.csv: extracellular enzyme activities (GLU, NAG, PHO) with extraction, measurement, and calibration details.
  - Plant_microbe_microcosm_sup_substrate.csv: effects of substrate additions on soil CO2 efflux using MicroResp; multiple substrates and 3 analytical replicates.
  - Plant_microbe_microcosm_sup_drought.csv: drought and rewetging experiment on soil CO2 efflux measured via MicroResp with multiple days.
  - Plant_microbe_microcosm_nutrient_supply.csv: PRS probe-based nutrient supply rates, including N species and macro/micronutrients with detection limits noted.
  - Plant_microbe_microcosm_plant_size_traits.csv: non-invasive image-based plant size traits (canopy area, height, width) over time; image analysis workflow.
  - Plant_microbe_microcosm_plant_morphology_traits.csv: six plant morphological traits measured once or later (leaf lengths, SLA, biomass, inflorescences) across dates.

- Data quality and documentation
  - Randomisation used in experimental design; replication at multiple levels (analytical replicates, technical replicates where applicable).
  - Instrumentation referenced for each dataset (e.g., Li-Cor CO2 flux system, ThetaProbe soil moisture, imaging with Canon camera).
  - Metadata tables define variables, units, and data relationships to enable discovery and integration with other datasets.

- References for methodology
  - Campbell et al. (2003) microtiter plate method for measuring CO2 evolution to profile microbial communities.
  - Creamer et al. (2009) inter-laboratory comparison of respiration assays for methodological consistency.