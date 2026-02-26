# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Provides soil moisture data and substrate utilisation profiles for saprotrophic fungi collected from Sourhope upland grassland (2001) as part of the NERC Soil Biodiversity Programme.
- Data support understanding of how fungal diversity and function influence organic matter decomposition in grassland soils.
- Includes four comma-separated data files linked to fungal isolates and BIOLOG-based substrate utilisation testing.

## Data provenance and scope
- Site: Sourhope Field Experiment, upland grassland, Sourhope, Roxburghshire, Scotland; 309 m a.s.l., mean temp 7.8°C, rain 952 mm.
- Soil: brown forest type, pH 4.54–4.81; dominant grasses listed (e.g., Agrostis capillaris, Festuca rubra, Nardus stricta).
- Programme aims: link soil biota diversity with functional roles in key ecological processes (carbon and nitrogen cycles) across multiple organism groups.
- Datasets relate to substrate utilisation by saprotrophic fungi and corresponding soil moisture measurements collected in July 2001.

## Methods and data collection
- Isolation of cultures:
  - Samples from soil horizons (litter fermentation LF, humus H, mineral A) and standing-dead plant material.
  - Culture methods (Warcup soil plating) to estimate fungal frequency of occurrence; identifications confirmed by sequencing or external strain identification.
  - Treatments in field plots included control, lime, nitrogen, and lime+nitrogen.
- Substrate utilisation experiments:
  - Phase 1: selection of fungal taxa from abundant and occasional groups; basidiomata collected where necessary.
  - Phase 2: testing of 48 isolates (26 frequent, 22 occasional) across substrates ( cellulose, lignin, pectin, starch, chitin ) and related indicators on semi-defined media.
  - Phase 3: BIOLOG SF-N2 microplates to profile 12 selected isolates on 95 low-molecular-weight carbon sources (carbohydrates, acids, amino acids, amines, amides).
  - Inoculum standardisation: spores/mycelial fragments in 0.2% carageenan; inoculum adjusted to 0.22 absorbance at 590 nm; three replicates per taxon.
  - Incubation: 15°C, up to 28 days; plates read at 590 nm, twice weekly, up to 600 hours (25 days).
- Data interpretation:
  - Total activity from BIOLOG plates treated as a proxy for carbon-source utilisation breadth; used to assess functional diversity and potential guild-level differences.
  - Cross-comparisons of abundant vs occasional isolates to explore functional redundancy and potential resilience in decomposition.

## Datasets and file structures
- Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv)
  - Key fields: ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, WEIGHT_BOAT, WEIGHT_SOIL, TOTAL_DRYWEIGHT1, TOTAL_DRYWEIGHT2, DRYWEIGHT_SOIL, PERCENTAGE_MOISTURE.
  - Measurement: oven-dried soil moisture determination (105°C, 24 h) from July 2001 samples.
- Dataset 1130: Substrate utilisation assay, using BIOLOG SF-N2 microplates (P2111_BIOLOG_RESULTS.csv)
  - Fields: SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
  - Data: absorbance readings (590 nm) per well across time (up to ~25 days) to quantify substrate utilisation.
- Dataset 1131: Details of the BIOLOG SF-N2 microplates (P2111_BIOLOG_INFORMATION.csv)
  - Fields: BIOLOGCELLID, SUBSTRATE, SUBSTRATE_TYPE.
  - Description: substrates loaded per BIOLOG cell in the SF-N2 plate.
- Dataset 1132: Details of Species examined using the BIOLOG SF-N2 microplates (P2111_BIOLOG_SPECIES.csv)
  - Fields: SPECIESID, SPECIES_NAME.
  - Description: taxonomy/name mapping for species used on BIOLOG plates.
- Additional context:
  - Final published dataset is described in Deacon et al., 2006 (Soil Biology and Biochemistry).
  - Useful references include Sourhope Field Data Handbook (Scott et al., 2003) and Usher et al. (2006).

## Data quality and access notes
- Data are subject to quality assurance procedures; however, NERC cannot warrant the accuracy or fitness for a particular use.
- No liability accepted by NERC Soil Biodiversity Programme for damages or losses arising from use of these data.
- Data references and related publications provide guidance for interpretation and context.
- Access and reuse guidance:
  - Data linked to published studies (Deacon et al., 2006) and project handbooks; associated materials available through EIDC catalogue records.
  - Encouraged citation: Deacon et al. 2006; Sourhope data handbook; related UK soil biodiversity literature.

## Usage and citations
- Primary interpretation goals: assess functional diversity and decomposition roles of soil saprotrophic fungi, including potential redundancy and resilience across abundant vs occasional taxa.
- Key findings (as reported): high functional redundancy among culturable decomposer fungi, with occasional taxa showing notable activity and broader substrate utilisation; possible positive indirect effects on cellulose degradation when abundant and occasional taxa are co-inoculated; occasional taxa may enhance temporal resilience in decomposition dynamics.
- Suggested references for users:
  - Deacon, L.J. et al., 2006. Diversity and function of decomposer fungi from a grassland soil. Soil Biology and Biochemistry.
  - Sourhope Field Data Handbook (Scott et al., 2003).
  - Usher, M.B. et al., 2006. Understanding biological diversity in soil: UK Soil Biodiversity Research Programme.

## Data governance considerations for Data Stewards
- Metadata and provenance:
  - Clear linking of soil moisture data (Dataset 1105) with BIOLOG-based substrate utilisation data (Datasets 1130–1132) and species identifications (Dataset 1132).
  - Document sampling context: site characteristics, soil horizons, treatments, and sampling dates.
- Data interoperability:
  - Alignment with common soil biodiversity data schemas by preserving identifiers (ROWNO, SUID, BIOLOGCELLID, SPECIESID) and consistent field definitions.
  - Cross-reference to published literature and data handbooks for reuse guidance.
- Update and versioning:
  - Datasets represent July 2001 sampling; ensure traceability to the corresponding project outputs (Deacon et al. 2006) and data publisher records.
- Access and reuse:
  - Acknowledge the liability disclaimer; provide clear citations and links to related datasets and manuals (EIDC catalogue entries, project records).
- Potential data quality actions:
  - Verify sample dates and plot identifiers against field notebooks.
  - Maintain linkage between moisture data and BIOLOG results via shared sampling units (SUID, MAIN_PLOT, BLOCK, TREATMENT, HORIZON).
  - Ensure consistent taxonomic naming and documentation of isolate provenance (soil vs litter, abundant vs occasional).