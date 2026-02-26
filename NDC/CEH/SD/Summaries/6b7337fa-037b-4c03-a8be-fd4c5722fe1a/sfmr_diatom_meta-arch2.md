# Diatom data

## Overview
- Purpose: Assess diatom response to wildfire in restored and unrestored sites of the South Fork McKenzie River, contributing to environmental monitoring and policy performance assessment over time.
- Location: South Fork McKenzie River, Oregon, USA (Lat/Long: 44.17, -122.30).
- Context: Post-wire wildfire data collected after the Holiday Farm Fire (Sept 2020); restoration status across transects.
- Temporal and sampling scope: Data from February 2022 and September 2021; 23 sites total (10 in Feb 2022; 13 in Sep 2021); restoration status across transects.

## Data and files
- Data type: Monitoring data.
- Interpreted by: All authors.
- Collection purpose: To evaluate diatom response to wildfire in restored vs unrestored reaches.
- Files:
  - 1) A description of key column names (Sample Unit, Area, AI, Diatom Identification, Technician, Mean Velocity, Mean Depth, Rock Area) for the main data file.
  - 2) A file containing genus-level counts of diatoms and other site characteristics for each of the 23 sites.
- Dataset structure: The dataset is named SFMR_Diatom_Data and includes:
  - Status (restored or unrestored), date.coll, year, habitat (e.g., pool, riffle), Season, transect, site.id.
  - AI (Autotrophic Index), mean.depth (cm), mean.velocity (m/s).
  - Rock area measurements: rock1.area.cm2, rock2.area.cm2, rock3.area.cm2.
  - Diatom counts by genus (e.g., Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Nitzschia, Cocconeis, Gomphonema, Diatoma, Navicula, Achnanthes, Reimeria, Cyclotella, Cymbella, Frustulia, Synedra, Rhopalodia, Eunotia, Pinnularia, Rhicosphenia, Amphora, Caloneis, Surirella, Asterionella).
  - Sample descriptive columns for each sample (date.coll/year, habitat, Season, transect, leftLon/leftLat/rightLon/rightLat).
- Data collection details:
  - 10 sites sampled in February 2022 (5 restored, 5 unrestored) and 13 sites in September 2021 (7 restored, 6 unrestored).
  - Transects: T1 and T2 in restored reach; T8, T9, T10, T11 and T8.5 in unrestored reach.
- Autotrophic Index (AI): Ratio of organic mass per cm2 in periphyton to chlorophyll a per cm2 in periphyton.

## Methods and quality control
- Collection methodology:
  - Periphyton sampled from riffles and pools in both restored and unrestored reaches using standard methods.
  - At each location, toothbrush scrubbing of five randomly selected cobbles, rinsed, and composited into a single sample; split into three subsamples.
  - One subsample preserved in 37% formalin for diatom composition; two subsamples analyzed for chlorophyll a and ash-free dry mass.
  - At least 500 diatom valves counted per sample; diatoms identified to genus level.
- Diatom identification: Conducted using standard laboratory techniques; genus-level classification.
- Quality control: Diatoms counted and processed following standard procedures; note on sample size: “minimum sample size of <500 valves per sample to ensure robustness” (as described in the data).
- Referenced standard methods:
  - Baird, B. R., Eaton, D. A., & Rice, W. E. (2017). Standard methods for the examination of water and wastewater (23rd ed.).
  - Kelly, M. G. et al. (1998). Recommendations for routine sampling of diatoms for water quality assessments in Europe.

## Data management and accessibility
- Provenance: Data interpreted by all authors; collected to enable standardized assessment of diatom communities and periphyton metrics.
- Data handling: Dataset prepared with clear column definitions and site-specific characteristics; designed for storage and upload to appropriate data portals to support reuse and broader access.

## Relevance for Analysts Monitoring the Environment
- Provides a standardized, genus-level diatom dataset linked to restoration status and wildfire impact, enabling longitudinal environmental health assessment.
- Combines diatom community data with periphyton biomass and AI metrics to gauge ecosystem recovery and restoration effectiveness after wildfire.
- Supports cross-site and temporal comparisons, contributing to monitoring performance and policy evaluation over time.