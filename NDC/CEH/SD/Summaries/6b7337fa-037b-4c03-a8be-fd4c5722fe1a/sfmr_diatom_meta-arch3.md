# Diatom data from the South Fork McKenzie River in Oregon, USA

## Overview
- Purpose: Assess diatom response to wildfire in restored and unrestored sites of the South Fork McKenzie River to inform restoration effectiveness and future monitoring decisions.
- Location and context: South Fork McKenzie River, Oregon, USA (approx. 44.17 N, -122.30 W); post-fire sampling following the Holiday Farm Fire (Sept 2020).
- Temporal scope: Data collected from two campaigns—February 2022 and September 2021.
- Site design: 23 sites in total (10 sites in Feb 2022: 5 restored, 5 unrestored; 13 sites in Sep 2021: 7 restored, 6 unrestored). Transect details include T1, T2 in restored zones and T8, T9, T10, T11, T8.5 in unrestored zones.

## Data and Methods
- Data type and purpose: Monitoring data focused on periphyton diatoms to characterize ecological response to wildfire and restoration status.
- Collection methodology:
  - Periphyton sampled from riffles and pools using standard methods.
  - At each location, five randomly selected cobbles were scrubbed with a toothbrush, rinsed, and composited into a single sample, then split into three subsamples.
  - One subsample preserved in 37% formalin for diatom analysis; two subsamples unpreserved for chlorophyll a (Chl a) and ash-free dry mass (AFDM).
  - Diatoms counted to genus level; at least 500 diatom valves counted per sample.
  - Autotrophic Index (AI) computed as the ratio of periphyton organic mass (ug) per cm2 to periphyton Chl a per cm2.
- Measurements and variables:
  - AI, mean depth (cm), mean velocity (m/s), rock area samples (rock1/rock2/rock3 in cm2).
  - Diatom counts by genus (e.g., Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Nitzschia, etc.).
  - Sample metadata: Status (restored/unrestored), date.coll, year, habitat (pool, riffle, off-channel), Season, transect, river-left/right end coordinates.
- Data standards and references: Analyses conducted following standard methods (Baird, Eaton & Rice, 2017; Kelly et al., 1998) for diatom sampling and interpretation.

## Dataset structure and content
- File: SFMR_Diatom_Data.csv (single CSV dataset).
- Key columns:
  - Status, date.coll, year
  - habitat, Season
  - transect, leftLon, leftLat, rightLon, rightLat
  - AI, mean.depth, mean.velocity
  - rock1.area.cm2, rock2.area.cm2, rock3.area.cm2
  - Diatom genus counts (e.g., Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Nitzchia, Cocconeis, Gomphonema, Diatoma, Navicula, Achnanthes, Reimeria, Cyclotella, Cymbella, Frustulia, Synedra, Rhopalodia, Eunotia, Pinnularia, Rhicosphenia, Amphora, Caloneis, Surirella, Asterionella, etc.).
- Sampling scope:
  - February 2022: n = 10 sites (5 restored, 5 unrestored).
  - September 2021: n = 13 sites (7 restored, 6 unrestored).
- Data quality: Diatoms counted and identified according to standard laboratory procedures; minimum robust sample size targeted at 500 valves per sample.

## Quality control and data standards
- Counting protocol: At least 500 diatom valves per sample to ensure robustness.
- Quality assurance: Adherence to standard diatom identification and counting procedures; explicit documentation of sample composition and counts.
- Metadata availability: Comprehensive metadata included (sampling dates, habitats, transect locations, coordinates, AI, environmental metrics) to enable verification, replication, and downstream analyses.

## Access, reuse, and governance
- Data stewardship: Metadata-rich dataset with clear provenance (collection methods, dates, sites, restoration status, and analytical methods).
- Reuse potential: Designed for cross-site and temporal comparisons between restored and unrestored reaches; suitable for integration into monitoring frameworks and policy evaluations of wildfire impacts and restoration effectiveness.
- Open data considerations: Dataset includes detailed methodological references and standard formats to facilitate sharing and reuse; potential barriers include governance requirements around data sharing and metadata completeness in some contexts.