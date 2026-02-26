# Glastir Monitoring & Evaluation Programme Vegetation Dataset 2013-2016

- Welsh Government AES-funded monitoring aims to measure biodiversity progress and support evidence for policy obligations under biodiversity conventions.
- The GMEP vegetation data contribute to baseline estimation, national trends, and Glastir-related reporting.

## Study design and sampling framework

- A 4-year rolling survey cycle (2013–2016 used for the first cycle) to maximise site visitation across Wales while monitoring year-on-year changes.
- Two components:
  - Wider Wales: baseline estimation and national trends.
  - Targeted: links to Glastir priority areas.
- Common spatial unit: 1 km x 1 km squares; total of 300 squares sampled over the cycle.
- Sampling approach:
  - Stratified random selection within Land Classification strata to ensure environmental heterogeneity is managed.
  - Half of squares randomly sampled (Wider Wales); half targeted for Glastir options.
  - Exclusions: squares with >75% urban land or >90% sea are removed.
- Spatial anonymity: distribution shown at 10 km resolution to protect confidentiality.
- Future integration: designed to align with the Countryside Survey of Great Britain to enable joint analyses.

## Data collection and vegetation survey methods

- Ecosystem-wide coverage with multiple measures captured in a single visit, maximizing cross-metric integration.
- Plot types and configurations (examples):
  - X plots: random main plots (4 m² or 200 m²; up to 5 per square).
  - Y plots: Small targeted/enclosed habitats (4 m²; up to 5 per square, more if >5 priority habitats).
  - U plots: Unenclosed broad habitats (4 m²; up to 10 per square).
  - B plots: Boundary plots (10 x 1 m; up to 5 per square).
  - A plots: Arable edges (100 x 1 m; up to 5 per square; paired with X plots if outside Glastir).
  - M plots: Field margins (2 x 2 m; up to 15 per square).
  - H plots: Hedgerow along hedgerows (10 x 1 m; 2 per square).
  - D plots: Hedgerow diversity plots (30 x 1 m; up to 10 per square).
  - S/W plots: Streamside plots (10 x 1 m; up to 5 per square).
  - P plots: Perpendicular streamside nests (10 x 1 m; new plot type; nests up to 6 total length 10 m).
  - R/V plots: Roadside verge plots (10 x 1 m; up to 5 per square; recorded only in 2016).
- Vegetation data collected:
  - Vascular plants identified with bryophytes/lichens where possible; full species lists recorded in plots; use of aggregates where field identification is difficult.
  - Cover estimates to the nearest 5% for species with at least 5% cover; presence if <5%.
  - Canopy height data and plot habitat context (glades, dead wood) recorded.
- Field procedures:
  - Pre-season training; ongoing supervision by managers; expert verification for difficult specimens.
  - Field handbook details methods; quality control measures integrated into field practice.

## Data files and data schema

- Three primary CSV files (data and metadata for analyses):
  - GMEP_VEGETATION_PLOTS_2013_16.csv: plot-level data including square ID (SQ_ID), plot type (PLOT_TYPE), plot number (PLOT_NUM), coordinates (EASTING_10km, NORTHING_10km), year (PLOTYEAR), plot characteristics (SLOPE, ASPECT, SHADE, CANOPY_HEIGHT, TREES_PRESENT, etc.), and additional plot-specific fields.
  - GMEP_VEGETATION_PLOTS_SPECIES_2013_16.csv: species occurrences per plot with Bioregional Codes (BRC_NUMBER), scientific name (BRC_NAMES), common name, nest level, cover metrics, year, coordinates, Land Classification, etc.
  - GMEP_VEGETATION_PLOTS_PNESTS_2013_16.csv: details for P plots nests, including nest level, maximum nest length, year, and related fields.
- Key metadata considerations:
  - Data follow Stace nomenclature (for plant names) and GB Countryside Survey protocols, with a note that some plots deviated slightly to reflect Glastir option representation.
  - Location data anonymized in maps (plotted at 10 km resolution).
- Quality control data:
  - Standardized QA process showing consistency across surveyors; subset (~10%) of squares re-surveyed by experts to assess reliability.
  - Data capture consistency across years reported as 85.5%–90.9% of species detected by field assessors.
- Documentation and standards:
  - Field Handbook (Smart et al., 2016) provides detailed procedures.
  - UKCEH maintains ISO 9001:2015 certified Quality Management System and QA policies.

## Quality control, assurance, and governance

- Intensive pre-field training and field supervision; challenging identifications reviewed by experts.
- QA exercise conducted on a representative subset to quantify data reliability and minimize bias.
- QA results indicate strong alignment between field surveyors and expert assessments.
- UKCEH Quality Policy and associated procedures applied to ensure high data quality and reproducibility.

## Usage, references, and publications

- Relevant publications and references accompany the dataset, including:
  - Glastir Monitoring & Evaluation Programme annual reports and website (gmep.wales).
  - Field Handbook for vegetation and soil (Smart et al., 2016).
  - Land Classification framework (Bunce et al., 2007) and related data centre references.
- Data centre and project governance:
  - UKCEH data centre hosts the datasets; field teams and roles are outlined in Appendix 1.

## Roles, responsibilities, and field teams (Appendix 1)

- Core roles include: database management, GMEP lead scientist, field team managers, sampling design experts, vegetation specialists, training leads, QA coordinators, and project management.
- Field teams comprise a broad list of surveyors and support staff who conducted the 2013–2016 vegetation surveys.
- Clear assignment of tasks and institutional responsibilities supports data integrity and reproducibility.

## Limitations and considerations for data use

- The survey mirrors GB Countryside Survey protocols but includes Glastir-focused targeting, which may introduce deviations in sampling emphasis.
- Some plots have deviations in sampling protocol to accommodate Glastir option representation.
- Spatial confidentiality is maintained via 10 km resolution for map outputs; users should account for this in spatial analyses.
- Data are limited to 2013–2016, with ongoing or future cycles potentially expanding coverage and comparability.