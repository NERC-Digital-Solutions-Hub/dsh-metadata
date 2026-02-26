# Overview of data

## What this dataset is
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in seaward flux of C, N, and P.
- Field data collected by L. Rovelli, K. M. Attard, and Assoc. Prof. H. Stahl under the leadership of Prof. R. N. Glud.
- Includes 39 CSV data files accompanying the overview.

## Data files and coverage
- 39 data files with names such as Flow_<SiteCode>_<Season>_<Location>.CSV, covering multiple river sites and seasons.
- Four field campaigns measuring in situ flow velocity transects in rivers with varying land–river connectivity in the Hampshire Avon catchment.
- Flow meters: Model 801 electromagnetic flow meter by Valeport; instrument serviced throughout the project.
- Site/measurement details:
  - SiteCode mappings: CE1 (River Ebble), GA2 (River Avon), GN1 (River Nadder), CW2 (River Wylye), AS1 (AP) and AS (Sem) for tributaries.
  - Campaign seasons: Spring 2013, Summer 2013, Autumn 2013, Winter 2014.
  - Some campaigns excluded at specific sites due to conditions (AP not in summer; CE1 and GA2 in winter due to flooding).

## Field collection protocol
- For each transect, the stream is gridded:
  - 0.25 m segments if stream width < 3 m; 0.5 m segments if width > 3 m.
  - Flow measured for each segment in 0.1 m depth steps from the riverbed; where near-surface measurements cannot be done in 0.1 m steps, 0.05 m steps used.
- NaN values indicate data not collected (e.g., between grid lines or too close to banks or water surface for accurate readings).

## File naming and site locations
- File naming convention: Flow_'SiteCode'_'Season'_'Location'.CSV identifies the riverine site and whether the transect is upstream or downstream.
- SiteCode details with coordinates:
  - CE1: River Ebble (51.027499 N, -1.9217089 E)
  - GA2: River Avon (51.318289 N, -1.8600020 E)
  - GN1: River Nadder (51.043849 N, -2.1118158 E)
  - CW2: River Wylye (51.142475 N, -2.2033140 E)
  - AS1 (AP): tributary of River Sem (51.055413 N, -2.1568407 E)
  - AS (AS2): River Sem (51.045826 N, -2.1104425 E)
- Location field indicates upstream or downstream end of the studied reach.

## Campaign timing and data gaps
- Spring 2013: 23/04 – 09/05/2013
- Summer 2013: 31/07 – 16/08/2013
- Autumn 2013: 29/10 – 11/11/2013
- Winter 2014: 28/01 – 09/02/2014
- Data collection gaps:
  - AP not surveyed in summer due to insufficient flow.
  - CE1 and GA2 not surveyed in winter due to flooding.

## Data structure and content
- Column headers:
  - Distance: meters from the stream bank.
  - Water depth: measured depth in meters at each distance from the bank.
  - Notes: information on vegetation, streambed features, proximity to aquatic eddy co-variance (AEC) at each distance.
  - Date line: the date of measurements in MM/DD/YYYY format.
  - Depth [m]: variable number of columns depending on site and campaign, indicating measurement depth at which flow was recorded.
- Data rows:
  - Each row after the depth header contains the average flow in meters per second (m/s) measured over 15 seconds (n = 15) for the specified depth.
- The dataset includes a star/separator block and a detailed notes description for context.

## Metadata and notes for interpretation
- The Notes column provides contextual information such as vegetation and bed features and proximity to AEC at each distance.
- The depth values and the number of depth columns vary by site and campaign, reflecting site-specific measurement schemes.
- Date information is embedded within each transect’s data block.

## Data governance and monitoring framework considerations
- Data standardization:
  - Consistent file naming, site coding, and transect location labeling facilitate cross-site comparability.
  - Variable grid spacing and depth-step differences require clear documentation for harmonization.
- Metadata completeness:
  - Rich metadata embedded in notes (vegetation, bed features, AEC proximity) aids interpretation but may require structured metadata fields for easier automated use.
  - Depth column variability necessitates explicit documentation to ensure correct data parsing and analysis.
- Data quality and gaps:
  - Presence of NaN entries highlights data gaps due to grid alignment or boundary constraints; frameworks should account for and document such gaps.
  - Flooding and flow conditions caused partial data loss; monitoring frameworks should include contingency planning for environmental disruptions.
- Data provenance and reuse:
  - Instrument details and servicing history are documented, supporting data lineage and reproducibility.
  - Public sharing constraints are not explicitly stated; institutions may need to review sharing policies when integrating these data into broader monitoring frameworks.
- Implications for monitoring design:
  - Standardized protocols (grid spacing, depth steps, measurement duration) support comparability over time and across sites.
  - Comprehensive site metadata (locations, site codes, upstream/downstream designation) enhances interpretability for policy evaluation and decision-making.