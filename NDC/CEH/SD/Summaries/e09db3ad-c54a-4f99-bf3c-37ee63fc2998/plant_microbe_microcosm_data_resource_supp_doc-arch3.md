# Plant_microbe_microcosm_design.csv

- Overview
  - Describes an environmental microcosm experiment to study drought adaptation in plants and root-associated bacteria under varying moisture environments.
  - Fully factorial design with drought/control adaptations in both plants and microbes and two moisture environments; includes no-plant controls and spare pots.
  - Conducted in an automatically ventilated polytunnel over 19 weeks with weekly soil respiration measurements and multiple ancillary assays.

- Experimental design and data structure
  - Sources of material: drought-adapted and control-adapted plant clones (Festuca ovina), and drought/control-derived microbial inocula (Pseudomonas koreensis isolates or field soil wash).
  - Treatments: two climate adaptations (drought vs. control) × two moisture environments (drought vs. well-watered) × inoculation type (bacteria or soil wash) × plant presence (plant vs. no-plant controls) with spare pots and sterilised soil-only pots.
  - Total: 176 microcosms in the main design, plus 32 no-plant controls and 3 sterilised-soil pots; spatially organized in a polytunnel with 4 tables and a grid layout.
  - Variables in Metadata Table 1 (selected):
    - pot_no, potID, Design (Main/No Plant Control/Spare/Probes), Clone full_ID, Festuca ancestry, Inoculation type, Microbial ancestry, Treatment (Moisture), table, row, column.

- Associated experiments and measurements (linked datasets)
  - Soil respiration and moisture (see Plant_microbe_microcosm_soil_respiration.csv)
  - Soil extracellular enzyme activities (see Plant_microbe_microcosm_enzymes.csv)
  - Substrate effects on respiration (see Plant_microbe_microcosm_sup_substrate.csv)
  - Lab-drought effects on respiration (see Plant_microbe_microcosm_sup_drought.csv)
  - Nutrient supply via PRS probes (see Plant_microbe_microcosm_nutrient_supply.csv)
  - Plant size traits from image analysis (see Plant_microbe_microcosm_plant_size_traits.csv)
  - Plant morphology traits (see Plant_microbe_microcosm_plant_morphology_traits.csv)

- Data quality, metadata, and governance
  - Randomisation used to validate experimental design.
  - No instrumentation or calibration requirements stated for the design file itself; instrumentation and methods are detailed in the associated datasets.
  - Metadata tables provide linking keys to merge datasets (e.g., pot_no) and descriptive fields for traceability (ancestry, inoculation, treatment, plate/tile positions).

- Key considerations for monitoring frameworks ( relevance and reuse)
  - A comprehensive, multi-factor design linking biotic (plant/microbial) and abiotic (moisture) drivers supports policy-relevant environmental health monitoring by enabling assessment of climate-change stressor interactions.
  - Time-series data over 19 weeks (soil respiration, moisture, and growth traits) illustrate dynamic responses to stressors, valuable for policy scenarios requiring temporal monitoring.
  - Rich metadata and explicit data governance (mergable identifiers, descriptive fields, replication) support data transparency, reuse, and integration into monitoring dashboards.
  - The collection includes open-access data types (CO2 efflux, enzyme activities, nutrient fluxes, plant traits) that can inform soil health indicators, carbon cycling, and ecosystem resilience assessments.
  - Highlights common monitoring challenges relevant to policy: data gaps (some datasets may need further metadata or standardization), data sharing considerations, and the need for consistent metadata to verify data suitability for decision-making.

- Instrumentation, methods, and calculations (summary)
  - Soil respiration and moisture: Li-Cor LC-8100 IRGA and Lambda multiplexer; ThetaProbe ML2x for soil moisture; weekly measurements across 15 observation weeks within 19 weeks.
  - Enzyme activities: β-glucosidase, N-acetylglucosaminidase, and phosphatase assays using fluorescence with a defined extraction and dialysis protocol; activity calculated from live vs boiled controls.
  - Substrate-induced respiration (MicroResp): substrates including glucose, ABA, malic acid, L-leucine, and water control; colorimetric 570 nm readouts; data processing uses normalization to baseline and calibration curves.
  - Drought assays (MicroResp): pre-drought and post-drought rewetting measurements with the same substrates; includes day-by-day observations during rewetting.
  - Nutrient probes (PRS): burial and retrieval of anion and cation PRS probes; measured NO3-N, NH4-N, and multiple macro/micronutrients; values expressed per 10 cm² over 2 weeks.
  - Plant traits: non-invasive image analysis for canopy area and maximum height/width; traditional morphology measurements for leaf length, SLA, biomass, and inflorescences collected in designated time windows.
  - Data handling and structure: multiple metadata tables (pot_no, plate, well, etc.) to support data merging, replicates, and analytical tallies across datasets.

- Files and their purposes (summary)
  - Plant_microbe_microcosm_design.csv: experimental layout, treatments, and metadata to integrate all datasets.
  - Plant_microbe_microcosm_soil_respiration.csv: CO2 efflux and soil moisture/temperature across microcosms and weeks.
  - Plant_microbe_microcosm_enzymes.csv: extracellular enzyme activities with QA and calculation method.
  - Plant_microbe_microcosm_sup_substrate.csv: substrate-induced respiration data from MicroResp assays.
  - Plant_microbe_microcosm_sup_drought.csv: drought-rewet experiments to assess respiration under lab-induced drying and rewetting.
  - Plant_microbe_microcosm_nutrient_supply.csv: PRS-based nutrient supply rates for each pot.
  - Plant_microbe_microcosm_plant_size_traits.csv: non-invasive canopy area, height, and width measurements over time.
  - Plant_microbe_microcosm_plant_morphology_traits.csv: six plant morphological traits measured once in two periods (June 2020 and March 2021).

- References for methodology
  - Campbell et al. (2003) rapid microtiter plate method for microbial carbon substrate profiling.
  - Creamer et al. (2009) inter-laboratory comparison for respiration assays.