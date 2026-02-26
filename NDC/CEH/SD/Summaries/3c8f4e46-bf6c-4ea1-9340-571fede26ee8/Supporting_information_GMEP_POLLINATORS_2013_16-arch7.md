# Glastir Monitoring & Evaluation Programme (GMEP) - Pollinator Survey Data in Wales

## Overview
- Purpose: collect biodiversity data to track Wales’ native biodiversity trends and contribute to biodiversity targets under the Well-Being of Future Generations Act.
- Focus: pollinators (butterflies, bees, hoverflies) and associated flowering plant communities; data supports landscape-scale biodiversity indicators and habitat extent estimates.
- Spatial unit: 1 km square grid across Wales; anonymised square identifiers to protect confidentiality.
- Timeframe: 4-year rolling survey cycle (first cycle 2013–2016); two components (Wider Wales baseline/trends and Glastir priority-area targeting).

## Survey Design and Spatial Sampling
- Sampling framework: 300 1 km squares sampled over the four-year cycle; half randomly selected within strata defined by the Land Classification of Great Britain, half targeted at Glastir priority areas.
- Exclusion criteria: squares with >75% urban land or >90% sea excluded and replaced.
- Data integration: same 1 km spatial unit used across components to enable integration; future analyses can align with the Countryside Survey of Great Britain.
- Data confidentiality: 10 km plotted maps to protect data confidentiality.

## Data Collection Methods
- Survey visits: each square visited twice in one year (July and August) between 2013–2016.
- Pollinator groups recorded:
  - Butterflies: species level.
  - Bees and hoverflies: grouped by broad morphological/ecological groups.
- Flowering plants: abundance recorded using the DAFOR-X scale.
- Transect method: standardized 2 km transect route (Pollard Walks) split into two 1 km legs; counts recorded in 5 m2 recording boxes across ten sections; DAFOR-X flowering plants recorded within 2.5 m of transect sections; weather data captured (temperature, sunshine, wind).
- Timed observations: 150 m2 flower-rich area surveyed for 20 minutes; recording of pollinators visiting flowers and plant groups.
- Activity window and conditions: surveys conducted between 10:00–16:00 (or up to 16:30 if unshaded), weather thresholds (e.g., 11–17°C with sunshine or >17°C with low wind) to ensure insect activity.

## Data Structure and Metadata
- Core data components: Transect data (two tables per component: VISIT and COUNT) and Timed observation data (two tables per component: VISIT and COUNT).
- Linking structure:
  - VISIT tables link to COUNT tables via VISITID.
  - Square-level linkage via SQ_ID; site anonymised (6-letter code) in all records.
  - Taxa and groups coded via GROUP_CODE and FLOWER_GROUP_CODE/INSECT_GROUP_CODE, with a central lookup: GMEP_POLLINATOR_GROUP_CODES.csv.
- File set (example):
  - GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv: transect visit metadata ( july/august visits, weather, timing, etc.).
  - GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv: transect insect/flower counts by section.
  - GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv: timed observation visit metadata.
  - GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv: timed observation counts of flowers and pollinators.
  - GMEP_POLLINATOR_GROUP_CODES.csv: taxonomy/group lookup with names, valid scientific names, and taxonomy level.
- Key fields include SQ_ID, VISITID, DATE, START_TIME/END_TIME, SUNSHINE, TEMPERATURE, WIND_SPEED, EASTING_10km, NORTHING_10km, LC (Land Classification), DAFOR-X, and counts by GROUP_CODE.

## Quality Assurance and Validation
- Training and ID verification: field surveyors trained; bee/hoverfly identification aided by experts; photographs submitted for verification.
- Quality control: annual QC visits to seven 1 km squares with repeat surveys; online assessment for surveyors after each year.
- Standards: DEFRA Joint Codes of Practice (JCoPR) followed to ensure robust scientific quality and repeatability.

## Outputs and Relevance for GIS Applications
- Spatial analyses: data designed for map-based visualization and spatial statistics at 1 km resolution; potential integration with GB Countryside Survey data.
- Data joinability: relational structure (VISIT–COUNT, SQ_ID, VISITID) supports GIS joins; taxonomy lookups enable dynamic filtering by insect/plant groups.
- Indicators: supports national and regional indicators for healthy ecosystems and biodiversity monitoring in Wales.

## Publications, References and Documentation
- Key references: Bunce et al. (ITE Land Classification), Emmett et al. (GMEP reports and methodologies), Pollard (butterfly transect method), field handbooks, and GMEP website.
- Supporting appendices and field handbooks provide survey forms and hoverfly ID guidance.

## Practical Notes for GIS Practitioners
- Data ingestion: import the five CSV tables and join on SQ_ID and VISITID; enrich with GMEP_POLLINATOR_GROUP_CODES.csv for taxonomy and groupings.
- Privacy: use 10 km coordinate data for mapping to protect square confidentiality; optionally use centroids for 1 km squares where appropriate.
- Visualization: create layers by square and year, with transect counts and timed observation counts; symbolize by insect group, plant group, and flowering cover (DAFOR-X).
- Integration opportunities: align with Countryside Survey outputs for broader national analyses; combine with habitat and land-use layers for ecosystem assessments.

## Appendix Highlights (Context)
- Appendix 2: Survey recording forms for transect walks (species/group entries, weather, plant covers, etc.).
- Appendix 3: Survey recording forms for timed observations (start/end times, flower visitation, DAFOR-X, etc.).
- Appendix 4: Hoverfly ID – key groups and atypical species for field identification guidance.