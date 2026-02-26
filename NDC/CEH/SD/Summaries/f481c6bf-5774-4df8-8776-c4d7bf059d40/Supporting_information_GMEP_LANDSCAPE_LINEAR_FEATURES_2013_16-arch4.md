# Glastir Monitoring & Evaluation Programme (GMEP): Landscape Linear Features 2013-2016 – Survey Design, Data Collection and QA

## Overview
- Wales’s agri-environment scheme (AES) monitoring, including Glastir, to assess landscape features and biodiversity.
- GMEP aims to track progress toward reversing native biodiversity decline and meet Convention on Biological Diversity obligations (2020).
- 4-year rolling survey cycle (2013–2016) to maximise site visits and detect spatial/temporal trends cost-effectively.
- Two components: Wider Wales (baseline estimation and national trends) and Targeted Component (Glastir priority areas).
- All data integrated on a common 1km square spatial unit to enable cross-analysis and potential GB-wide integration.

## Sampling design and scope
- Total of 300 x 1km squares sampled over the 4-year cycle.
- Randomly sampled squares within strata defined by the Land Classification of Great Britain (ITE framework) to capture environmental heterogeneity.
- Half of squares chosen randomly (Wider Wales); other half targeted at Glastir priority areas.
- Exclusion criteria: squares with >75% urban land or >90% sea area (per LCM2007 and high-tide data).
- Sampling framework aligned with the Countryside Survey of Great Britain for robust national/sub-national indicators.

## Data collection methods
- Within each 1km square, linear, areal, and point features mapped on base maps using pre-determined codes.
- Electronic data capture with CS Surveyor software and Esri GIS integration.
- Linear features (<5 m wide) include boundaries, hedges, walls, fences, streams, and other lines; recorded with attention to length, condition, and context.
- Woody linear features (hedges, lines of trees) classified via a standardized key and Habitats Steering Group guidance.
- Minimum recording: linear features must be at least 20 m long (allowing up to 20 m gaps); exceptions apply for curtilage or canopy areas.
- Primary datasets:
  - LANDSCAPE_LINEAR_FEATURES_2013_16.csv: feature-level data with IDs, spatial references, lengths, themes, habitat names, management signs, DBH, species composition, verge widths, etc.
  - LANDSCAPE_LINEAR_FEATURE_SP_2013_16.csv: species-level data linked to linear features (VEGETATION_TYPE, SPECIES, PROPORTION, etc.).
- Data quality ensured through mandatory fields, prompts, and prompts to visit all mapped components; data captured digitally to minimize transcription errors.

## Data structure and metadata
- Data organized around up to 300 1km squares with standardized attributes (e.g., SQ_ID, LC, Easting/Northing, event IDs, feature IDs).
- Key variables cover geographic location, feature geometry (start/end points, length), feature type (theme), habitat details, historic management, management indicators (staked trees, tree protectors), structural attributes (verge widths, margins), and quality indicators (condition, height).
- Species data follow standardized nomenclature (e.g., species listed with proportions; reference to Stace 1997 for nomenclature).

## Quality assurance and governance
- Field teams comprised of experienced botanical surveyors; all surveys preceded by intensive training to ensure consistency with field handbooks (Maskell et al., 2016).
- Real-time data capture reduces post-survey digitising errors; mandatory fields and prompts support data completeness.
- Data transferred to offices promptly for rapid quality checks; a Quality Control (QC) team re-surveys part or all of a square to identify and rectify issues.
- QA and methodology documented in field handbooks and linked to broader GMEP documentation and publications.

## Data use, integration and outputs
- Emphasizes integration of multiple measures into an ecosystem-based assessment.
- 1km square unit facilitates aggregation for national and sub-national reporting and potential cross-survey integration with GB datasets.
- Outputs support baseline establishment, national trends, and targeted monitoring aligned with Glastir priorities.
- References and publications (e.g., final reports, methodological handbooks) support transparency, traceability, and reuse.

## Access, publications and references
- Methodology and results referenced to multiple publications and project reports (e.g., ITE Land Classification, GMEP annual/final reports, mapping handbooks).
- Tools and project information available via the Glastir Monitoring & Evaluation Programme website (gmep.wales) and CEH/UK partners.
- Data structure and definitions documented in the associated CSV files and field mapping handbooks.

## Roles, governance and teams
- Appendix 1 lists roles (e.g., database management, sampling design/statistics, vegetation expertise, project management) and field survey teams.
- Clear division between project leadership, field teams, and data management to support consistent data collection, processing, and analysis.

## Key considerations for data leaders
- Holistic view of the data system: multiple metrics integrated at 1km scale for broad and targeted insights.
- User needs and co-ownership: data collection aligns with policy and monitoring requirements, enabling feedback-driven improvements.
- Data availability, gaps, and standards: structured sampling and metadata aim to reduce fragmentation and improve discoverability across datasets.
- Data quality and metadata: rigorous QA processes, standardized field handbooks, and electronic capture to enhance accuracy and reproducibility.
- Data discoverability and reuse: standardized formats and cross-survey compatibility to facilitate integration with national datasets and future analyses.