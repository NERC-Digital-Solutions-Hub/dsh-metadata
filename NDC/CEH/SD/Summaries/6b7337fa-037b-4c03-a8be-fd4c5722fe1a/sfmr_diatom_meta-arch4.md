# Diatom data

## Overview
- Dataset documenting diatom response to wildfire in restored and unrestored sites of the South Fork McKenzie River, Oregon, USA, following the Holiday Farm Fire (Sept 2020).
- Collected at two time points: February 2022 and September 2021.
- Includes 23 sites (10 in Feb 2022: 5 restored, 5 unrestored; 13 in Sep 2021: 7 restored, 6 unrestored).
- Data support assessment of periphyton community structure, autotrophic index, and restoration effects.

## Data Content and Structure
- Primary data file: SFMR_Diatom_Data.csv
- Auxiliary file: A description of key column names for the main data file; and a separate file with genus-level counts and site characteristics.
- Columns (examples): Status (restored/unrestored), date.coll, year, habitat (e.g., pool, riffle), Season, transect, site.id, AI (autotrophic index), mean.depth (cm), mean.velocity (m/s), rock1.area.cm2, rock2.area.cm2, rock3.area.cm2, genus-level diatom counts (e.g., Tabellaria, Epithemia, Fragilaria, Navicula, Amphora, etc.), leftLon/leftLat/rightLon/rightLat (transect coordinates).
- Sample unit and grouping: Sample units are transects; three rocks sampled per transect (rock1/2/3.area.cm2) and combined for analysis.
- Data coverage: AI and periphyton metrics derived from counts of at least 500 diatom valves per sample; genus-level identifications.
- Autotrophic index (AI): ratio of organic mass per cm2 in periphyton to chlorophyll a per cm2 in periphyton.

## Collection Methodology
- Periphyton sampled from riffles and pools in both restored and unrestored reaches using standard methods.
- Procedure: scrub periphyton from five randomly selected cobbles with a toothbrush, rinse, and composite into a single sample; split into three subsamples.
  - One subsample preserved in formalin for diatom analysis.
  - Two subsamples unpreserved for chlorophyll a (Chl a) and ash-free dry mass (AFDM) analyses.
- Diatoms counted and identified to genus level using standard techniques.
- Chl a and AFDM used to estimate Chl a per unit organic biomass; AI calculated from these metrics.
- Quality control follows established protocols (minimum 500 diatom valves per sample).

## Data Standards and References
- Uses standard methods for diatom analysis:
  - Baird, Eaton & Rice (2017) Standard Methods for the Examination of Water and Wastewater (23rd ed.).
  - Kelly et al. (1998) Recommendations for routine sampling of diatoms for water quality assessments in Europe.
- Dataset explicitly notes that diatoms were sampled and counted per standard laboratory procedures.

## Dataset Details and Access
- Dataset structure: SFMR_Diatom_Data includes multiple columns for sample metadata, site characteristics, and genus-level diatom counts.
- Spatial and temporal context: lat/long provided (e.g., 44.17, -122.30); sampling dates: February 2022 and September 2021; all sites post-fire affected.
- Status descriptor: indicates whether a site is in the restored or unrestored condition for comparison purposes.
- Sample distribution by date and restoration status as described above, enabling cross-site restoration effect analyses.

## Data Management and Usage
- Data are organized for analysis of diatom community composition across restoration states, seasons, habitats, and transects.
- Suitable for assessing restoration outcomes, correlations between AI and diatom assemblages, and habitat-dependent diatom distribution.
- Provides a structured foundation for cross-site comparisons and informing restoration management decisions.

## Limitations and Considerations
- Data reflect post-fire conditions; may not capture pre-fire baselines.
- Genus-level identifications limit species-level resolution but are appropriate for broad ecological assessments.
- Access and use should respect the provided metadata fields, including sampling dates, transect details, and site statuses.