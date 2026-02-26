# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

## Overview
- Dataset collected by the UK Centre of Ecology & Hydrology (UKCEH) in 2018 to evaluate impacts of pasture-fed livestock on grassland parameters, focusing on sward composition and soil quality.
- Context: Grasslands are vital in the UK for farming and public benefit; study engages with Pasture Fed Livestock Association (PFLA) and aligns with Countryside Survey (CS) methodologies for comparability.
- Deliverables include vegetation and soil measurements from farms, plus field management data, enabling assessment of biodiversity, soil health, and carbon-related metrics under pasture-based systems.

## Aims and scope
- Provide environmental health measures to scrutinise and inform policy decisions and future monitoring around pasture-based livestock systems.
- Compare with long-running vegetation and soil monitoring frameworks (e.g., CS) to place pasture-fed practices within national baselines.
- Use data to inform stakeholders, support transparency, and identify gaps in knowledge and data governance for monitoring.

## Study design and scope
- Participants: 56 farms across Great Britain, all member(s) of PFLA; inclusion includes certified, provisionally certified, and member-only farms intending certification.
- Sampling period: May–September 2018.
- Design: Field surveys of a single 200 m² plot per farm, with a second subplot approach for vegetation within each plot; field visits conducted by trained surveyors.
- Comparability: Methods mirror the CS approach to enable cross-dataset analyses and trend assessment.

## Data collection and measurements
- Vegetation data:
  - Species presence and percent cover within nested plots; vegetation height categories; plot-level attributes.
  - Post-field data captured via electronic recording device.
  - On-site collection of current and historic management practices (grazing, sward longevity, inputs) via a dedicated questionnaire.
- Soils data:
  - One soil core per plot (15 cm depth, 7 cm diameter) for a range of properties, aligned with CS soil protocols (with some exclusions).
  - Measured properties include: bulk density, carbon (SOC) and nitrogen, phosphorus (Total P and Olsen P), pH (in water and CaCl2), electrical conductivity (EC), moisture, and additional CS-compatible measurements.
  - Advanced analyses: Loss-on-Ignition (LOI) for organic matter estimation; SOC via elemental analysis; calcium carbonate content via thermogravimetry; particle size distribution via laser diffraction and hydrometer methods; aggregate stability via wet sieving and NaOH treatment.
  - Soil physical and chemical properties used to infer carbon stocks, nutrient status, and soil structure integrity.
- Field management data:
  - Management history, pasture type, grazing regime (length of graze, livestock presence, cutting history), fertilization (mineral and organic), lime application, herbicide use, and other inputs.
  - Detailed management indicators captured to link field practices with soil/vegetation outcomes.

## Quality control and data processing
- LOI quality controls used internal soil standards; batches checked against historical norms with replication when deviations exceeded 2 standard deviations.
- Total C and N analyses performed with calibrated instruments; reference materials embedded within batches for QA.
- Phosphorus measurements included multiple quality controls: duplicates and matrix-matched blanks.
- pH and EC measurements accompanied by internal standards for QC; LD measurements cross-validated with sand and standard soils; attention to organic matter interference in LD accuracy.
- Data processing followed standardized protocols to ensure compatibility with CS datasets and long-term monitoring frameworks.

## Data structure and accessibility
- Four CSV data sheets, anonymized at the farm level:
  - SEEGSLIP_PLOTS_2018.csv: Basic plot attributes and vegetation plot data (site code, plot type, habitat classifications, canopy/shrub/ground heights, soil sampling status, grid references, and plot timing).
  - SEEGSLIP_SPECIES_2018.csv: Species-level vegetation data per plot (species name, code, nest level, cover estimates, presence/absence indicators).
  - SEEGSLIP_SOIL_2018.csv: Soil properties per plot (carbon, LOI, nitrogen, phosphorus forms, pH values, conductivity, bulk density, particle size fractions, aggregate stability, CaCO3 content, and related measurements).
  - SEEGSLIP_FIELD_MGT.csv: Field management data per site (PFLA membership duration, certification status, pasture type, grazing/infrastructure details, fertilizer and lime usage, herbicide data, and livestock information).
- Farms anonymized with IDs; location referenced via Ordnance Survey 5 km grid references to protect landowner confidentiality.
- Data designed for interoperability with Countryside Survey datasets, enabling cross-study comparisons and integration into monitoring frameworks.

## Relevance for monitoring frameworks
- Demonstrates a rigorous, governance-minded approach to environmental health monitoring at farm scale:
  - Uses standardized, CS-aligned methods to ensure data compatibility and comparability for policy evaluation and trend analysis.
  - Combines vegetation, soil, and management data to link policy-relevant practices (pasture-based systems) with ecological outcomes (soil quality, carbon indicators, biodiversity proxies).
  - Includes metadata on data provenance, QA procedures, and dataset structure to support data governance and responsible data sharing.
- Addresses common monitoring challenges identified for monitoring framework authors:
  - Data quality and standardization: robust QA/QC, documented protocols, methodological transparency.
  - Data accessibility and governance: anonymization, clear data structure, and explicit data management practices to facilitate reuse while protecting confidentiality.
  - Data completeness and relevance: comprehensive suite of soil/vegetation metrics and management context to fill knowledge gaps and enable policy-relevant analyses.
  - Data interoperability: explicit alignment with Countryside Survey methods to reduce duplication and enable integrated analysis across programs.

## Limitations and considerations
- Sampling is focused on PFLA member farms, which may introduce selection bias relative to national representativeness.
- Some CS soil measurements were excluded, which could affect direct comparability for certain soil properties.
- LD accuracy can be impacted by high organic matter content, requiring careful interpretation of sand fractions in very organic soils.
- Data sharing and openness depend on governance decisions; while data are structured for reuse, explicit public access may require additional permissions or licensing.

## References
- Emmett et al. CS-related soil manuals and methodologies; Oakley and CS technical reports; foundational soil analysis methods (Avery & Bascomb, Gee & Or, etc.); biodiversity habitat classifications and related methodological references cited in the dataset documentation.