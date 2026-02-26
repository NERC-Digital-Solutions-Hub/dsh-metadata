# Plant_microbe_microcosm_design.csv

- Overview
  - Describes the experimental design for a plant-microbe microcosm study investigating how drought adaptation in Festuca ovina and root-associated bacteria interact under different moisture environments.
  - Factorial design combining drought/control-adapted plants and microbes with drought and well-watered moisture treatments.
  - 176 main microcosms across two climate adaptations, plus 32 no-plant controls, 16 spare microcosms, and 3 soil-only pots.
  - Conducted in an automatically ventilated polytunnel over 19 weeks; weekly soil respiration monitoring and soil moisture data collection; additional targeted sampling in February 2021.

- Datasets and data types (associated files)
  - Plant_microbe_microcosm_design.csv
    - Metadata table describing pots and experimental design fields (pot_no, Clone full_ID, Festuca ancestry, Inoculation type, Microbial ancestry, Treatment, spatial arrangement).
  - Plant_microbe_microcosm_soil_respiration.csv
    - CO2 efflux and soil water content measured weekly across 15 observation weeks (19-week period).
    - Instrumentation: Li-Cor Li8100 IRGA and Li-Cor 8150 Multiplexer; soil temperature recorded with a probe.
    - Metadata include week, date, temporal block, pot_no, swc, soil_temp, file_name, and notes.
  - Plant_microbe_microcosm_enzymes.csv
    - Extracellular enzyme activities (GLU, NAG, PHO) from February 2021 soil samples.
    - Extraction, dialysis, and fluorescence-based assays; data converted to enzyme activities (nmol g-1 h-1) with technical replicates.
    - Metadata includes pot_no, assay details, and activity calculations.
  - Plant_microbe_microcosm_sup_substrate.csv
    - Substrate addition effects on soil respiration using the MicroResp method (glucose, ABA, malic acid, L-leucine, H2O).
    - 3 analytical replicates per sample; pre-incubation and readouts at 0 and 6 hours; plate reader measurements at 570 nm.
    - Outputs include CO2_percent, total efflux, and mean/se for replicates; metadata covers plate, well, pot_no, day, and substrate.
  - Plant_microbe_microcosm_sup_drought.csv
    - Lab drought and rewet experiment effects on soil CO2 efflux (drought and rewet days).
    - Lab treatments with drought reached 15% soil water content, followed by rewetting; MicroResp assays adapted from substrate dataset.
    - Metadata includes MR_Treatment, day, pot_no, and analytical reps.
  - Plant_microbe_microcosm_nutrient_supply.csv
    - Nutrient supply rates measured by PRS probes (anion and cation probes) installed in each watered control microcosm pot.
    - Analysis by Western Ag; nutrient metrics include NO3-N, NH4-N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd, and notes.
    - Probes installed 04-02-2021 and retrieved 18-02-2021; probes cleaned and sent for analysis.
  - Plant_microbe_microcosm_plant_size_traits.csv
    - Non-invasive image-based plant size traits (canopy area, maximum height, maximum width) collected April–May 2020.
    - Two images per timepoint per pot; analysis in ImageJ; spatial layout captured via pot_no mapping.
    - Quality control includes replicate observations by multiple researchers.
  - Plant_microbe_microcosm_plant_morphology_traits.csv
    - Six plant morphological traits measured once (June 2020 and March 2021): leaf length, leaf width, SLA, regrowth, above-ground biomass, inflorescences.
    - Measurements using ruler, microscopy, and balance; data linked to pot_no.
  - Metadata Tables (Tables 1–7)
    - Provide detailed field definitions, units, and descriptions for pot_no, design, ancestry, treatment, plate/well mappings, sample IDs, and measurement-specific columns.

- Spatial design and GIS-relevant features
  - Spatial identifiers
    - pot_no serves as a core join key across datasets.
    - Spatial layout information captured in Plant_microbe_microcosm_design.csv via table, row, and column (indicating microcosm position within the polytunnel tables).
    - Four tables in the polytunnel with grid-like arrangement; includes blocking and replication information.
  - Temporal sequencing
    - Week numbers, observation days, and dates enabling time-series mapping of respiration, enzyme activity, and substrate responses.
  - Plot-level context for mapping
    - Climate adaptation status (drought vs. control) and microbial/plant ancestries (Buxton drought-adapted vs. control-adapted) provide categorical layers for thematic GIS maps.
  - Data integration readiness
    - Consistent pot_id linkage across respiration, enzymes, substrates, drought, nutrient, and plant trait datasets supports multi-layer GIS analyses and temporal visualization.

- Data quality, calibration, and instrumentation notes (GIS implications)
  - Randomisation used in experimental design to support valid spatial analyses.
  - Instrumentation details provided for respiration measurements (Li-Cor LI-8100/LI-8150) and microplate readers for enzyme and substrate assays.
  - Calibration/analytical methods specified for enzyme activity conversion and substrate-based respiration calculations.
  - Quality control highlights include multiple analytical replicates, sterilization steps, controlled pre-incubations, and notes on data labels and potential pot-label mismatches.

- Data integration and GIS-ready considerations
  - Primary join keys: pot_no (across all datasets) and spatial coordinates (table/row/column) from design metadata.
  - Time-series alignment: weekly respiration data linked to dates/weeks; substrate and drought experiments include day-based observations.
  - Attribute enrichment: potential GIS layers include treatment (Drought vs. Control), climate adaptation, inoculation type, microbial/plant ancestry, nutrient status (PRS data), and plant morphology/size metrics.
  - Data gaps and granularity
    - Some datasets are time-point specific (e.g., enzyme activity from February 2021; plant traits from June 2020 and March 2021), requiring careful temporal alignment for dynamic GIS analyses.

- Practical GIS outcomes and use cases
  - Create a spatially explicit microcosm map of the polytunnel, with pot_no as the core attribute and table/row/column as spatial anchors.
  - Develop time-enabled GIS products showing how soil respiration, enzyme activity, and substrate responses change over the 19-week experiment.
  - Combine nutrient status (PRS-derived) with plant traits to explore spatial correlations between nutrient availability and plant growth metrics.
  - Overlay treatment regimes (drought vs. control) with microbial/plant ancestry to study spatial patterns in interactions.
  - Support data packaging or dashboards that allow policy colleagues, clients, or the public to explore spatial and temporal patterns in plant-microbe drought responses.

- References
  - Campbell, C. D., et al. (2003). A rapid microtiter plate method to measure carbon dioxide evolved from carbon substrate amendments.
  - Creamer, R. E., et al. (2009). Inter-laboratory comparison of multi-enzyme and substrate-induced respiration assays.