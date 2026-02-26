# Earthworm diversity and the integration of physical, biochemical and microbiological functions.

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biodiversity, soil processes, and microbial–earthworm interactions at Sourhope, Scotland.
- Investigates earthworm–soil microbial processes, organic matter transformations, and soil physical structure.
- Sweethope mesocosm experiment: 100 soil boxes moved from Sourhope plots to an animal-proof enclosure 100 m away; designed to inoculate specific earthworm functional groups while maintaining separate main plots.
- Final sampling occurred in October 2001, providing end-point data on earthworm abundance/biomass and plant botanical composition.

## Datasets (structure and contents)
- Dataset 1009: Sweethope Endpoint Botanical Composition Data (2129_BOTANICAL_COMPOSITION.csv)
  - Contains end-point botanical composition for each experimental treatment.
  - Key fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), SPECIES, BOTANICAL_COMPOSITION (Braun-Blanquet scale 0–6).
  - Purpose: capture plant community responses to treatments and plot-level replication.
- Dataset 1010: Sweethope Endpoint Earthworm Survey Data (P2129_EARTHWORM_SURVEY.csv)
  - Contains end-point earthworm census data (abundance and biomass) by species.
  - Key fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C/L), SPECIES, ABUNDANCE (per m2), BIOMASS (per m2).
  - Purpose: quantify earthworm community structure under different inoculation and lime treatments.

## Site, design, and methods (data provenance)
- Site layout: Sourhope main plots with an off-site Sweethope enclosure to prevent contamination; 5 replicated rows with randomized treatments within each row.
- Soil and environment: upland grassland on Brown Forest Soils (Sourhope series) on a north-facing slope; base-poor, damp mineral soils with typical upland vegetation; grazing terminated in 1998.
- Experimental treatments:
  - No earthworm inoculation; inoculation with epigeic (Lumbricus rubellus), endogeic (Allolobophora chlorotica), anecic (Lumbricus terrestris); combinations (ABC).
  - Lime treatment applied to mimic main Sourhope plots.
- Inoculation details: April 2000; doses per box:
  - Epigeic: 20 L. rubellus
  - Endogeic: 15 A. chlorotica
  - Anecic: 4 L. terrestris
- Box and enclosure design: plastic containers with fine mesh lids and base drainage; 50 reburied intact soil boxes (undisturbed) and 50 hand-sorted boxes.
- Sampling and processing:
  - Earthworms hand-sorted; identified to species with Sims & Gerard (1985) key; preserved in 40% ethanol for identification; abundance and biomass per m2.
  - Botanical composition recorded at end using Braun-Blanquet scale.
  - Grass clippings collected to assess biomass; regular box maintenance (roughly every two weeks) to prevent mesh displacement.

## Data content and metadata (data governance implications)
- Data are delivered as two CSV files with explicit column definitions, units, and data types.
- Metadata includes sampling dates, block structure, plot design, treatments, and grid coordinates (CELL_X, CELL_Y) to enable spatial analyses.
- Data provenance links to primary publications and project references for traceability (e.g., Scott et al. 2003; Sims & Gerard 1985).
- Data quality: numeric range checks, format conformity, and logical integrity checks performed; however, NERC disclaims warranty of accuracy or fitness for a particular use.

## Governance, access, and reuse considerations
- Data originate from the NERC Soil Biodiversity Programme; documentation includes references and Further Reading to contextualize data interpretation.
- Documentation provides clear definitions and data types, facilitating interoperability with other soil biodiversity datasets.
- Important caveat for users: while quality assurance steps exist, there is no guarantee of accuracy; data should be used with consideration of potential limitations and uncertainties.
- Potential reuse: longitudinal and cross-site analyses of earthworm effects on soil processes and plant communities; integration with other datasets from the Sourhope/Sweethope program.

## Practical notes for data stewards
- Ensure alignment of dataset 1009 and 1010 fields with existing data dictionaries (e.g., site handbooks) to maintain consistent metadata across related datasets.
- Maintain clear linkage between SAMPLE_IDs and their corresponding sampling dates, plot identifiers, and treatment codes to support reproducibility.
- Preserve provenance references (publications and supporting information) to aid users in contextualizing data.
- Provide guidance on unit interpretation (abundance and biomass per m2) and treatment coding (C vs. L) for downstream analyses.
- Plan for dataset updates or corrections by maintaining versioned records and change-log notes.