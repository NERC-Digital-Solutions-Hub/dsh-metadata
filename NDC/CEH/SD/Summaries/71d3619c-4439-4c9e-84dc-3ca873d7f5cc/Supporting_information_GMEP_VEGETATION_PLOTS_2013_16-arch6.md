# Glastir Monitoring & Evaluation Programme Vegetation Data (2013-2016)

- A Wales-wide monitoring initiative (GMEP) collecting vegetation biodiversity data to support evidence for biodiversity goals and obligations under biodiversity conventions.
- Data support focus: structure, quality, integration, and dissemination to enable reuse and policy interpretation.

## Study design and scope

- 4-year rolling survey cycle (2013–2016) to maximise site coverage and detect temporal trends cost-effectively.
- Two components:
  - Wider Wales Component: baseline estimation, national trends, national reporting of Glastir.
  - Targeted Component: links to Glastir priority areas.
- Common spatial unit: 1 km² squares; total of 300 squares sampled over the cycle.
- Sampling frame aligned with Countryside Survey of Great Britain to enable future integration.
- Exclusion criteria: delete squares with >75% urban land or >90% sea.

## Sampling framework and field locations

- 1 km² squares randomly sampled within strata defined by the ITE Land Classification (Bunce et al., 2007); proportional allocation by stratum size.
- Half of squares randomly sampled (Wider Wales); half targeted at Glastir priority areas.
- Map distribution provided at 10 km resolution to protect confidentiality.

## Data collection methods

- Vegetation survey records presence and abundance of vascular plants, selected bryophytes, and macro-lichens across multiple plot types; field methods outlined in the Field Handbook (Smart et al., 2016).
- Plot types and configurations (examples):
  - X plots: random/main, 4 m² or 200 m², up to 5 per square
  - Y plots: Small, Targeted/Habitat, 4 m²
  - U plots: Unenclosed broad habitats, 4 m²
  - B plots: Boundary, 10 × 1 m
  - A plots: Arable margins, 100 × 1 m
  - M plots: Margin, 2 × 2 m
  - H plots: Hedgerow, 10 × 1 m
  - D plots: Hedgerow diversity, 30 × 1 m
  - S/W plots: Stream/Watercourse/Perpendicular, 10 × 1 m
  - P plots: Perpendicular streamside (new nest type, up to 10 m)
  - R/V plots: Roadside verge, 10 × 1 m (specific years)
- Nest structure and sampling:
  - Nested subplots (nests) within plots; some plots have fixed nesting rules; total nest lengths and counts defined per plot type.
  - Canopy and ground features recorded; height measurements captured as modal values.
- Data files produced:
  - GMEP_VEGETATION_PLOTS_2013_16.csv: plot metadata and plot-level attributes (e.g., SQ_ID, PLOT_TYPE, PLOT_NUM, coordinates, year, slope, aspect, shade, vegetation heights, species presence, etc.).
  - GMEP_VEGETATION_PLOTS_SPECIES_2013_16.csv: species-level data per plot/nest (BRC code, scientific name, common name, nesting level, cover metrics, year, grid references, land classification, etc.).
  - GMEP_VEGETATION_PLOTS_PNESTS_2013_16.csv: perpendicular nest measurements (NEST_LEVEL, MAX_LENGTH, year, etc.).

## Data quality, assurance, and standards

- Rigorous field training and detailed methodologies in the Field Handbook; ongoing supervision and expert identification for difficult taxa.
- Quality Assurance (QA) program: ~10% of the total sample undergoes QA in summer after field surveys; experts re-record vegetation plots to verify locations and species.
- QA checks focus on plot type placement and comprehensiveness of species capture; across years 85.5%–90.9% of assessor-recorded species were matched by QA.
- UKCEH maintains ISO 9001:2015-certified Quality Management System; formal QA policy, objectives, and procedures.

## Data structure and accessibility

- Three primary CSV files with extensive metadata and field definitions:
  - PLOT-level data (SQ_ID, PLOT_TYPE, PLOT_NUM, coordinates, year, slope, aspect, shade, heights, trees, disease indicators, invasive species, etc.)
  - SPECIES data (species codes, scientific and common names, nest level, cover by nest, plot year, coordinates, land classification)
  - PNESTS data (P plots nested measurements and nesting extents)
- Fields are anchored to standard GB Countryside Survey protocols where applicable, enabling cross-survey integration.
- Data validation and field recording standards detailed in the Field Handbook; nomenclature follows Stace (1997) for plant names.

## Potential data products and use cases

- Dashboards and self-serve tools enabling exploration of national and regional biodiversity indicators.
- Cross-survey integration with the GB Countryside Survey for broader trend analyses.
- Baseline estimation, national trend reporting, and monitoring of Glastir scheme outcomes.
- Support for policy decisions and reporting to Welsh Government and biodiversity objectives.

## References and related materials

- Key methodological and background references, including:
  - Bunce et al. (2007) ITE Land Classification methodology
  - Smart et al. (2016) GMEP Vegetation and Soil Field Handbook
  - Emmett et al. (2014) GMEP First Year Annual Report
  - Glastir Monitoring & Evaluation Programme project website (gmep.wales)
- Appendices with roles, tasks, and field team rosters.

## Roles, tasks, and teams

- Appendix 1 outlines responsibilities (e.g., Database management, Field team management, Lead Scientist, Statistical expertise, Vegetation experts, Project management, QA).
- Field Survey Teams lists multiple field team members across the monitoring period.

## Data governance and stewardship

- UKCEH Quality Management System guidance and QA procedures applied to ensure data reliability and traceability.
- Data offered with accompanying documentation, Field Handbook, and methodological references to support reproducibility and future analyses.