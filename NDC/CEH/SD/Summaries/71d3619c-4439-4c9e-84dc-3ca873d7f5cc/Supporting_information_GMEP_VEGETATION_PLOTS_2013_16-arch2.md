# Glastir Monitoring & Evaluation Programme Vegetation

- A Wales-wide monitoring program (GMEP) established to track the effects of the Glastir AES scheme on vegetation and biodiversity, contributing to progress toward reversing native biodiversity decline and meeting CBD 2020 obligations.
- Focus: vegetation biodiversity data to support evidence for environmental health and policy performance.

## Survey design and scope

- 4-year rolling survey cycle (2013–2016) to maximize site coverage while monitoring year-on-year changes.
- Two components:
  - Wider Wales Component: baseline estimation, national trends, national reporting for Glastir.
  - Targeted Component: links to Glastir priority areas and scheme aims.
- Integration across metrics with a common spatial unit: 1 km square.
- Sampling frame: 300 × 1 km squares over the cycle.
  - Half randomly sampled within strata defined by the ITE Land Classification (GB-wide stratification by landscape type).
  - Other half targeted at Glastir priority areas.
- Exclusions: any square with >75% urban land or >90% sea (per LCM2007 and census data) excluded.
- Spatial distribution and confidentiality: maps plotted at 10 km resolution to protect data.

## Data collection and vegetation sampling

- Field method: record plant species presence and abundance across multiple plot types and nested sub-plots (nests) within plots.
- Species recorded:
  - Complete vascular plant list for each plot.
  - Selected bryophytes and macro-lichens; D plots record only woody species.
  - Some species may be aggregated in field to reflect identification difficulties.
- Abundance recording: cover estimates to nearest 5% for species with ≥5% cover; presence noted if cover <5%.
- Additional habitat info: canopy cover, overhanging vegetation, glades, dead wood, general plot descriptors.
- Plot recording procedures and difficulty adaptations detailed in the Field Handbook (Smart et al., 2016).

## Plot types and sampling design

- Plot types and sampling scales (examples):
  - X (Random/Main): 4 m² or 200 m², up to 5 plots per 1 km square.
  - Y (Small: Targeted/Enclosed Habitat): 4 m², up to 5 per square (more if >5 priority habitats).
  - U (Unenclosed): 4 m², up to 10 per square.
  - B (Boundary): 10 × 1 m, up to 5 per square.
  - A (Arable): 100 × 1 m, up to 5 per square (paired with X plots if outside option).
  - M (Margin): 2 × 2 m, up to 15 per square.
  - H (Hedgerow): 10 × 1 m, up to 2 per square.
  - D (Hedgerow Diversity): 30 × 1 m, up to 10 per square.
  - S/W (Streamside): 10 × 1 m, up to 5 per square (along watercourses).
  - P (Perpendicular streamside): 10 × 1 m, up to 5 per square (new P plot type; nests up to 10 m).
  - R/V (Roadside verge): 10 × 1 m, up to 5 per square (recorded in 2016 only for squares replicated from CS 2007).
- Plot nesting and layout: nests within plots subdivided to capture habitat variation; some plots align with stream proximity or boundaries to reflect landscape features.
- Data files describe plot-level attributes (location, plot type, year, habitat context) and nest-specific measurements.

## Data files and metadata

- Three core CSV data files are provided:
  - GMEP_VEGETATION_PLOTS_2013_16.csv: plot-level metadata per nest, including square ID, plot type, values for slope/aspect/shade, canopy/ground heights, presence of trees, invasive species indicators, and habitat context fields.
  - GMEP_VEGETATION_PLOTS_SPECIES_2013_16.csv: species-level records per plot, including BRC species codes, scientific and common names, nest level, cover percentages (zero/first/total), plot year, and location coordinates.
  - GMEP_VEGETATION_PLOTS_PNESTS_2013_16.csv: per-nest extent measurements for P plots (perpendicular to watercourses), with nest length details and year.
- Data standards and nomenclature:
  - Species nomenclature follows Stace (1997).
  - Location based on random stratified design using ITE Land Classification (2007).
  - Metadata columns include square identifiers, plot numbers, coordinates, survey year, plot dimensions, slope/aspect/shade, heights, tree presence, and various habitat/disease/invasive-species indicators.
- Field handbook and data documentation referenced for detailed methods and column definitions (Smart et al., 2016).

## Quality control, assurance and data governance

- Rigorous field training and standardized methodologies to maintain consistency among surveyors.
- Quality Assurance (QA) exercise to quantify consistency and identify potential biases.
  - QA targeted just over 10% of total sample squares; selected to represent Land Classification strata and both Wider Wales and Targeted components.
  - QA surveys conducted the week after field surveys; re-recorded vegetation plots, using photographs and sketches to verify plots and plot-type placements.
  - Across years, field surveyors recorded between 85.5% and 90.9% of the species recorded by the assessor during QA.
- UKCEH operates a Quality Management System (ISO 9001:2015 certified) with a formal QA policy and procedures to ensure high standards.

## Publications, references and related resources

- Key methodological references and data descriptions linked, including:
  - ITE Land Classification of Great Britain (2007) as the sampling framework.
  - Glastir Monitoring & Evaluation Programme (GMEP) annual and methodological reports.
  - Field Handbook for vegetation and soils (Smart et al., 2016).
  - GMEP website and data centre resources for methodologies and results.
- Appendix 1 (Roles, tasks, responsibilities) lists:
  - Core project roles (e.g., GMEP Lead Scientist, field team managers, sampling design/statistical experts, data management, species work package lead, project management, QA).
  - Field survey teams and individuals contributing to data collection and management.

## Appendix 1: Roles, tasks and responsibilities (highlights)

- Core team includes:
  - GMEP Lead Scientist, Field Team Managers, Sampling Design/Statistics experts, Vegetation experts, Data managers, Project manager, and QA lead.
- Field survey teams list numerous named personnel responsible for field data collection.
- Emphasizes collaboration between field teams and data management to maintain data integrity and traceability.

- Overall, the document describes a structured, multi-component vegetation monitoring program (GMEP) with a robust, standardized design, extensive field protocols, quality assurance, and dataset architecture designed to support national biodiversity evidence and policy evaluation in Wales.