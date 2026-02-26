# Glastir Monitoring and Evaluation Programme: Topsoil Mesofauna 2013-14

- Purpose: Evaluate the effectiveness of Glastir management interventions on soil quality and ecosystem outcomes (climate, biodiversity, soil and water quality, woodland expansion), and quantify general soil quality trends independent of Glastir.

## Survey design and scope

- Programme: Glastir Monitoring and Evaluation Programme (GMEP) with a 4-year rolling survey cycle (2013–2016) to capture spatial variation and temporal trends cost-effectively. Soil mesofauna data were collected in 2013–2014 (years 1–2).
- Components: Wider Wales component for baseline estimates and national trends; Targeted component focused on Glastir priority areas.
- Spatial unit: Common 1 km square grid to enable integration with other surveys (e.g., Countryside Survey). 300 1 km squares sampled over the cycle.
- Sampling frame: Half of squares from stratified random sampling across Land Classification of Great Britain (LCGB) strata; half targeted at Glastir priority areas.
- Exclusions: Squares with >75% urban land or >90% sea excluded.
- Output scale: Aims for national and sub-national indicators; data intended to be integrated with future analyses across surveys.

## Field sampling and laboratory methods

- Within each square: 5 pre-determined, randomly dispersed soil sampling locations where possible.
- Sample collection: Soil core (F-core), 8 cm long, coincident with vegetation surveys; cores mailed to Centre for Ecology & Hydrology (CEH) Lancaster for faunal extraction.
- Sample preparation: Fresh soil cores; optional 4°C storage for up to 2 days; extraction begins on arrival.
- Faunal extraction: Dry extraction using six or more Tullgren funnels; 40 W heat source drives fauna into 70% ethanol collection bottles over ~5 days.
- Metadata capture: Recording sheets (SQXN) include core depth, start/stop times, and other sample details; data subsequently transferred to Excel.
- Quality control: Rigorous labeling and tracking (SQXN, square numbers, plot numbers); standard operating procedures maintained for consistency.

## Invertebrate identification and data recording

- Target groups: Broad groups of soil mesofauna (mites, oribatid mites, Collembola subgroups, enchytraeids, etc.) identified and tallied into predefined categories.
- Sorting protocol: Specimens separated from soil debris under a stereomicroscope; grouped into specified broad groups; counts entered into data templates.
- Sample verification: 1 in 20 samples undergo cross-check by a second staff member to ensure consistency; ongoing quality control for identifications.
- Data entry: Counts entered into Excel templates and later integrated into the CEH Bangor database.
- Training: Staff receive at least one week of identification training with voucher specimens before routine processing.

## Data management, QA, and outputs

- Data management: Data management and sample tracking assigned to designated roles; integration into the CEH Bangor database.
- QA framework: Followed DEFRA Joint Code of Practice for Research (JCoPR); independent checks for a subset of samples to ensure methodological robustness.
- Primary data product: GMEP_TOPSOIL_MESOFAUNA_2013_14.csv containing counts by sample across 1 km squares, including detailed metadata.
- Dataset schema (examples of columns in the CSV):
  - YEAR, SQ_ID, PLOT_TYPE, PLOTNUM, EASTING_10KM, NORTHING_10KM, LC (Land Classification)
  - CORE_TAKEN, MITE_ORIB_BOX, MITE_ORIB_OTHER, MITE_MESO, MITE_OTHER
  - COL_POD, COL_ENTO, COL_SYMP, ENCHY, OTHERS
  - MITE_ORIB_TOTAL, TOTAL_MITES, TOTAL_COLL, TOTAL_MESO, TOTAL_INVERT
- Data integration: Datasets structured for compatibility with existing national surveys and future cross-survey analyses; intended to be discoverable with metadata on data portals.

## Relevance and considerations for analysis

- Enables analysis of correlations between soil mesofauna communities and drivers such as land use, climate, and pollution, within the Glastir context and at national/sub-national scales.
- Provides a baseline and trend data to assess the impact of Glastir interventions on soil biodiversity and overall soil health.
- Facilitates integration with Countryside Survey methodologies to support broader ecosystem assessments.
- Scale and accessibility challenges highlighted by the project design (1 km square resolution, multi-source data), along with the need for consistent data standards and robust QA to support reliable analyses.

## References, terminology, and Appendix

- Key references include Bunce et al. 2007 (Land Classification), various CEH and Defra sources, and methodologies for Collembola and soil mite identification.
- Appendix 1 lists roles, responsibilities, and field teams involved in soil mesofauna work, highlighting collaboration across field and data management roles.