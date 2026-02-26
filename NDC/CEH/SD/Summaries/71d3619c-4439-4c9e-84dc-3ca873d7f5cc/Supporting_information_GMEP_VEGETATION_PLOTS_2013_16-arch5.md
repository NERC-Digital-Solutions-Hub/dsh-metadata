# Glastir Monitoring & Evaluation Programme Vegetation Data (GMEP, 2013-2016)

## Overview
- Wales-wide monitoring under the Glastir scheme aims to track biodiversity to support the reversal of native biodiversity decline and meet CBD 2020 obligations.
- GMEP uses an ecosystem-based, multi-metric design with a rolling 4-year cycle (2013–2016) to maximize site coverage and detect temporal trends.
- Two components: Wider Wales baseline/national trends and Targeted component linked to Glastir priorities; data integrated within a common 1 km square spatial framework.
- Sampling aligns with the Countryside Survey methodology to enable future data integration with GB analyses.
- Location confidentiality is maintained by plotting maps at 10 km resolution.

## Study design and sampling framework
- 300 x 1 km squares sampled over the 4-year cycle.
- Squares split into: half Wider Wales (randomly sampled within Land Classification strata) and half Targeted at Glastir priority areas.
- Exclusion criteria: squares with >75% urban land or >90% sea water excluded.
- Stratified random selection by Land Classification to minimize within-stratum heterogeneity and maximize between-stratum differences.

## Data collection methods
- Vegetation surveys record plant presence/abundance across multiple plot types within each square (e.g., X plots, Y plots, U/B/A/M/H/D/S-W/P/R-V plots), with varying sizes and nest structures.
- Plots capture a complete vascular plant list plus selected bryophytes/macro-lichens; some aggregates used for difficult taxa.
- Cover estimated to the nearest 5% for species ≥5% cover; presence recorded for lower covers.
- Canopy and habitat context (glades, dead wood) documented.
- Field teams receive rigorous training; challenging specimens referred to experts.
- Field Handbook provides detailed protocols (Smart et al., 2016).

## Data files and metadata
- Three primary CSV files (2013–2016):
  - GMEP_VEGETATION_PLOTS_2013_16.csv: plot metadata per nest, including coordinates (E/N in OSGB), plot type, year, slope, shade, height metrics, and species-related fields (e.g., invasive species indicators, hedgerow attributes).
  - GMEP_VEGETATION_PLOTS_SPECIES_2013_16.csv: species-level records with BRC codes, scientific and common names, nest level, and cover metrics (zero/first/total cover), plus plot identifiers.
  - GMEP_VEGETATION_PLOTS_PNESTS_2013_16.csv: perpendicular nest measurements for P plots.
- Coordinates use OSGB 1936; 1 km square unit as the common spatial reference; confidentiality maintained in published maps (10 km plotting).
- Taxonomy follows Stace (1997) for British flora.
- Data are linked to the Field Handbook and standard GB Countryside Survey protocols.

## Quality control and assurance
- UKCEH maintains a Quality Management System (ISO 9001:2015) for data quality and reproducibility.
- Extensive training, field handbooks, and continuous communication to ensure consistency across field surveyors.
- QA exercise conducted to quantify data consistency; ~10% of samples resurveyed by experts to assess reliability and bias.
- QA plots and nested plots re-recorded using photographs and sketches; spatial coverage strategies verified for appropriateness.
- Across years, field teams captured 85–91% of species recorded by assessors, indicating robust data capture.

## Data governance, stewardship, and metadata
- Clear roles and responsibilities: database management, field team management, lead scientists, sampling design experts, statistics, vegetation expertise, quality assurance, and project management.
- Appendix lists named personnel and field survey teams, illustrating formal governance and accountability.
- Data are documented with a Field Handbook and linked to relevant publications, ensuring traceability and methodological clarity.
- Data are designed for potential integration with GB Countryside Survey data to support cross-border analyses.

## Access, dissemination, and use
- Data are produced and curated by UKCEH as part of the Glastir Monitoring & Evaluation Programme.
- Supporting materials include field handbooks, methodology references, and annual reports; public dissemination is anchored in the GMEP website and published references.

## Key considerations for Data Stewards
- Ensure alignment with GB Countryside Survey protocols to enable future data integration across UK datasets.
- Maintain detailed metadata: plot types, nest structure, plot year, coordinates, habitat descriptions, and species coding (BRC codes; taxonomy).
- Preserve confidentiality by continuing to mask precise plot locations in public outputs.
- Uphold data quality standards via ISO 9001:2015 framework and continuous QA processes.
- Track data lineage from field collection through QA to final datasets; document any deviations from standard protocols (e.g., adjustments to plot types in certain years).
- Maintain governance continuity by sustaining the roles outlined in Appendix 1 and ensuring junior field teams have access to Field Handbook resources.
- Plan for future data integration and interoperability, particularly with Countryside Survey methodologies and potential cross-year analyses.

## Appendix highlights (roles and teams)
- Roles include database management, lead scientist, sampling design and statistics, vegetation experts, QA, and project management.
- Field Survey Teams: list of personnel across field teams, illustrating structured, hierarchical data collection operations.