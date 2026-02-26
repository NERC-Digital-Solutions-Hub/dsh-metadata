# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

- Purpose and scope
  - Presents substrate utilisation profiles of saprotrophic fungi and soil moisture data from soils at Sourhope, collected to understand how fungal diversity and their functional roles influence organic matter decomposition within a grassland ecosystem.
  - Part of the NERC Soil Biodiversity Thematic Programme (1999–2006), focusing on biodiversity and functional processes in soil biota.

- Study site and experimental design
  - Location: Sourhope Field Experiment, Macaulay Land Use Research Institute (James Hutton Institute), Sourhope, Scottish Borders (grid reference NT8545019630).
  - Site characteristics: upland grassland, 309 m above sea level; mean annual temp ~7.8°C; rainfall ~952 mm; brown forest-type soil; pH ~4.54–4.81; dominant grasses include Agrostis capillaris, Festuca rubra, Nardus stricta, Anthoxanthum odoratum, Poa pratensis.
  - Experimental setup: plots with treatments—Control, Lime (CaCO3), Nitrogen (NH4NO3), and Lime+Nitrogen; pits (12×20 m) across five replicates per treatment.
  - Sampling context: data linked to aboveground biomass, species composition, and diversity assessments.

- Data collection and methods
  - Isolation of fungi: cultures from soil, standing-dead plant material, and basidiomata; identification via ITS sequencing or BOLD/CABI-confirmed identifications.
  - Substrate utilisation testing (BIOLOG-based): 
    - 48 fungal isolates tested initially (abundant and occasional taxa) for utilisation of substrates (cellulose, lignin, pectin, starch, chitin) on semi-defined media; standardised inoculum; incubation up to 28 days at 15°C.
    - 12 isolates (6 abundant, 6 occasional) selected for fine-scale carbon-source profiling using BIOLOG SF-N2 microplates (95 carbon sources) to derive detailed functional patterns.
    - Inoculation and measurement: standardized inoculum in carageenan matrix; plates incubated 15°C; absorbance at 590 nm read over up to 25 days; total activity used as a proxy for carbon utilisation breadth and intensity.
  - Data handling: quality assurance procedures described; patterns used to infer functional diversity and potential roles in decomposition.

- Datasets and data structure
  - Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv)
    - Key fields: ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON (LF/H/H or A), WEIGHT_BOAT, WEIGHT_SOIL, TOTAL_DRYWEIGHT1, TOTAL_DRYWEIGHT2, DRYWEIGHT_SOIL, PERCENTAGE_MOISTURE.
    - Purpose: moisture content derived from oven-dried soil samples (105°C, 24 h).
  - Dataset 1130: Substrate utilisation assay (P2111_BIOLOG_RESULTS.csv)
    - Key fields: SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
    - Purpose: absorbance readings (590 nm) from BIOLOG assays across incubation period (up to ~25 days) for each isolate.
  - Dataset 1131: Details of BIOLOG SF-N2 microplates (P2111_BIOLOG_INFORMATION.csv)
    - Key fields: BIOLOGCELLID, SUBSTRATE, SUBSTRATE_TYPE.
    - Purpose: substrate information for each BIOLOG plate cell.
  - Dataset 1132: Species examined (P2111_BIOLOG_SPECIES.csv)
    - Key fields: SPECIESID, SPECIES_NAME.
    - Purpose: taxonomic identities corresponding to BIOLOG isolates.
  - Overall data relationship: isolates characterized for function and linked to substrates via BIOLOG INFORMATION; moisture data linked to sampling units and plots.

- Key findings and interpretation
  - Functional redundancy: abundant and infrequent fungi largely utilised similar substrates.
  - Notable roles for infrequent taxa: some infrequent fungi showed higher overall activity and broader substrate utilisation, contributing to decomposition.
  - Interactions across taxa: mixed inoculations suggested slight positive indirect effects on cellulose degradation but potential negative effects on lignin degradation due to competition.
  - Implications for ecosystem resilience: occasional taxa may bolster temporal resilience of decomposition processes; uncultured taxa may add additional functional diversity.

- Usage notes and references
  - Data quality: subject to QA procedures; NERC cannot warrant accuracy or fitness for a specific use; no liability for data use.
  - Related references and resources:
    - Deacon et al. 2006. Diversity and function of decomposer fungi from a grassland soil. Soil Biology and Biochemistry.
    - Scott et al. 2003. Sourhope Field Data Handbook (Supporting Information).
    - Usher et al. 2006. Understanding biological diversity in soil: UK Soil Biodiversity Research Programme.
  - Context and broader links: data contribute to understanding soil biodiversity and functional roles in carbon and nitrogen cycling within grassland ecosystems.

- Relevance for GIS and data integration
  - Spatially contextualizable: data are associated with sampling units (SUID), blocks, main plots, horizons, and treatments, enabling spatial mapping across the Sourhope experiment.
  - Potential GIS applications: map moisture distribution, overlay fungal functional profiles with soil properties, incorporate substrate utilisation patterns into spatial models of decomposition and carbon cycling.
  - Considerations for use: cross-dataset joins rely on SUID, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, and SAMPLE_DATE; ensure alignment of formats and units when integrating with other GIS layers.