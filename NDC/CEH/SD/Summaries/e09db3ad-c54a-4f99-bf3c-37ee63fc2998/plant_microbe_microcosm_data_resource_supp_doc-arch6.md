# Plant_microbe_microcosm_design.csv

- Purpose: Describes the experimental design of a plant–microbe microcosm study to understand how drought adaptation in plants and their root-associated bacteria interact under different moisture environments.
- Scope: Full factorial design combining two climate adaptations (drought-adapted vs control-adapted) with two moisture environments (drought vs well-watered), across plant–microbe combinations.

## Experimental setup

- Materials:
  - Bacterial inocula: pooled populations of Pseudomonas koreensis or field-derived soil wash containing intact microbial communities.
  - Plants: surface-sterilised Festuca ovina clones.
  - Soil: sterilised natural rendzina soil.
  - Source of adaptation: Buxton Climate Change Impacts Lab (BCCIL) drought treatment vs control treatment.
- Structure:
  - Two climate treatments (drought vs control) for both plants and microbes, combined factorially with two moisture environments (drought vs well-watered).
  - 176 microcosms in total, across eight plant–microbe climate adaptation combinations and two moisture treatments.
  - 32 additional no-plant control microcosms (containing either pooled bacterial population or soil wash, subjected to drought or control moisture).
  - 16 spare microcosms (one of each treatment combination represented once) and 3 sterile soil pots.
- Timeframe: Experiment ran for 19 weeks in an automatically ventilated polytunnel.
- Randomization: Randomisation used to validate the experimental design.
- Data capture: Weekly soil respiration and volumetric soil water content (using LiCor Li8100/8150 and ThetaProbe ML2x); additional data collected from separate datasets.

## Data structure and linking

- Key identifiers:
  - pot_no and potID: unique microcosm identifiers for merging across datasets.
  - Clone full_ID and Festuca ancestry: plant origin and climate-adaptation lineage.
  - Inoculation and Microbial ancestry: type and climate-origin of microbial inoculum.
  - Treatment: moisture environment (D for drought, C for control).
  - Table, row, column: spatial blocking information in the polytunnel.
- Datasets designed to be cross-linked via pot_no for integrated analyses.

## Data products and datasets included

- Plant_microbe_microcosm_design.csv
  - Content: Experimental design metadata, inoculation types, plant/microbial ancestry, treatment, and spatial blocking information.
- Plant_microbe_microcosm_soil_respiration.csv
  - Content: CO2 efflux from soil and soil water content across 19 weeks, with two temporal blocks and soil temperature data.
  - Measurements: Weekly respiration data; includes time-block, pot_no, swc, soil_temp, file_name, timestamp, efflux, and notes.
- Plant_microbe_microcosm_enzymes.csv
  - Content: Extracellular enzyme activities (GLU, NAG, PHO) from control microcosm soils (Feb 2021), with extraction and assay procedures.
  - Data: Raw fluorescence, calculated activities (GLUactivity, NAGactivity, PHOactivity), and metadata (pot_no, Analytical rep, etc.).
- Plant_microbe_microcosm_sup_substrate.csv
  - Content: Substrate addition effects on soil CO2 efflux (MicroResp method) for control soils.
  - Substrates: glucose, ABA, malic acid, L-leucine, and water control; three analytical replicates per sample.
  - Data: Absorbance readings (T0, T6), normalized values, CO2 percentages, efflux calculations, and mean/SE across replicates.
- Plant_microbe_microcosm_sup_drought.csv
  - Content: Effects of a lab-drought treatment and subsequent rewetting on CO2 efflux in soils from watered controls.
  - Experimental design: Lab control vs lab drought fractions; timepoints day-based during drought and rewet.
  - Data: Similar to MicroResp substrates with MR_Treatment, day, T0/T6, CO2_percent, efflux, mean_efflux, se_efflux.
- Plant_microbe_microcosm_nutrient_supply.csv
  - Content: Nutrient supply rates measured by in-situ PRS probes (cation and anion probes) installed in microcosms (Feb–Apr 2021).
  - Nutrients: NO3-N, NH4-N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd; notes on detection limits.
  - Data: Sample IDs, pot_no, burial/retrieval dates, counts of probes, and measured concentrations (µg/10 cm2 / 2 weeks).
- Plant_microbe_microcosm_plant_size_traits.csv
  - Content: Non-invasive image-based plant size metrics over time ( canopy area, height, width ).
  - Imaging: Two images per timepoint per microcosm; analysis via ImageJ; canopy area via convex hull.
  - Data: date, rep, person, pot_no, area (cm2), height (cm), max_width (cm), file_area/file_height/file_width.
- Plant_microbe_microcosm_plant_morphology_traits.csv
  - Content: Six plant morphological traits measured once (June 2020 and March 2021).
  - Traits: leaf_length, regrowth, SLA, biomass (above-ground dry mass), inflorescences; unit details included.
- Metadata and quality control
  - Metadata Tables: Comprehensive descriptors for each dataset (e.g., pot_no, plate, column, soil fresh weight, analytical_rep, etc.).
  - Quality control notes: Randomization applied; replication schemes for enzyme and substrate assays; instrument calibration notes and handling procedures.

## Data quality and methods

- Quality control:
  - Randomization used to validate experimental design.
  - Multiple replicates for key assays (e.g., 4 analytical replicates for enzyme assays; 3 technical replicates for MicroResp substrate assays).
  - Sterilization, contamination controls, and cross-checks described for specific datasets.
- Instrumentation:
  - CO2 efflux measured with Li-Cor Li8100/8150; soil moisture with ThetaProbe ML2x; soil temperature monitored during some measurements.
  - Image-based plant metrics captured with a Canon EOS 700D camera; ImageJ used for analysis.
- Calibration and data processing:
  - Enzyme activities calculated from fluorescence using a defined standard curve and detailed formula.
  - MicroResp data processed with normalization against T0 and blank wells; CO2Percent calibration performed with a separate calibration file.

## How the data can be used (Data Support perspective)

- Integrative analyses:
  - Link pot_no across datasets to assess how drought adaptation in plants and microbes interacts with soil respiration, enzyme activity, substrate-induced respiration, nutrient supply, and plant growth traits.
- Self-serve data exploration:
  - Build dashboards or pivot-style reports to compare treatments (drought vs control) and climate adaptation combinations across time and biological responses.
- Data provenance and reuse:
  - Rich metadata tables enable traceability and reuse in meta-analyses or cross-study comparisons.
- Potential outputs:
  - Relationships between microbial community function (enzyme activities, substrate responses) and plant performance (size traits, morphology) under drought stress.
  - Influence of nutrient availability and root-zone nutrient supply on respiration dynamics under varying moisture regimes.

## References

- Campbell, C. D., et al. (2003). A rapid microtiter plate method to measure carbon dioxide evolved from carbon substrate amendments. Applied and Environmental Microbiology, 69(6), 3593-3599.
- Creamer, R. E., et al. (2009). Inter-laboratory comparison of multi-enzyme and substrate-induced respiration assays. Biology and Fertility of Soils, 45(6), 623-633.