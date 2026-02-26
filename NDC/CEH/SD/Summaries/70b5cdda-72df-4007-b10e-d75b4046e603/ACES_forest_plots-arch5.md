# Structure and composition of woodlands across Mozambique: supporting documentation

## Overview
- Quantitative datasets on woodland structure and composition from 431 plots across 27 villages in Mabalane (Gaza), Marrupa (Niassa), and Gurue (Zambezia) in Mozambique.
- Data collected from 2014–2015 across three districts; plot radius 20 m (0.126 ha); all trees >5 cm DBH recorded.
- Measurements include tree stems, leaf litter, woody litter, grass biomass, coarse woody debris, and canopy cover; canopy measured with a Densiometer.
- Species identification data submitted separately; soil data collected but not included here; grass species data omitted due to identification challenges; some plots have incomplete data.
- Collected as part of the ESPA-funded ACES project to link woodland structure to ecosystem services and human wellbeing; data linked with household surveys and remote sensing in subsequent analyses.

## Data provenance and scope
- Project: ACES (Ecosystem Services for Poverty Alleviation) funded by ESPA; methodologies co-developed by ACES researchers; data collected by project authors with local assistance.
- Data quality: field teams trained; translations from Portuguese to English performed by the lead author; electronic data capture with tablets and ODK; post-collection cleaning and outlier checks; anomalies corrected or removed as needed.
- Documentation acknowledges evolving methods across sites; differences are noted in text and dataset descriptions.
- Data are organized to support discovery and reuse, with explicit metadata and linkage keys.

## Sampling design and field methods
- Plot design: circular plots of 20 m radius (0.126 ha). Center geolocated with GPS; elevation recorded.
- Village selection and areas:
  - Mabalane: 7 villages; 24 plots per village (pilot village had 19 plots); village sampling area defined as a 5 km radius from village center.
  - Marrupa and Gurue: 10 villages each; plots spatially delineated by village boundaries due to proximity; 12 plots per village with paired design to reduce walking time.
- Measurements within plots:
  - Tree stems >5 cm DBH recorded; status (live/dead, cut/broken), stump height, and point-of-measurement noted.
  - Four 1 m2 quadrats per plot for litter and grass biomass; leaf litter and grass sub-samples dried to determine dry weight; woody litter weighed as wet weight.
  - Coarse woody debris measured along four 20 m transects per plot; diameter, length, decomposition class, and local species name recorded.
  - Canopy cover estimated with Densiometer; qualitative observations of canopy, slope, fire history, etc.
- Plot and data integrity:
  - Some plots lacked complete data due to field issues; plot_metadata.csv records missing data and errors.
  - Grass species data omitted in all sites due to identification difficulties during dry season.

## Data structure and datasets
Six interconnected datasets (CSV format), linked by survey_id, plot_id, and optionally subplot_id or transect/quadrat identifiers:
1. cwd.csv — Coarse woody debris: each piece along transects with length, diameter, decomposition class, and local species name.
2. cwd_decomposition.csv — Decomposition classes with descriptive attributes and reduction factors for biomass corrections.
3. plot_metadata.csv — Plot-level metadata: coordinates, plot radius/area, date, slope, canopy observations, burn status, completeness indicators (tree_stem_data, litter_data, canopy_data, cwd_data).
4. quadrat_data.csv — Per-quadrat biomass weights (grass, leaf litter, woody litter) and canopy cover.
5. tree_stem_data.csv — All stems >5 cm DBH within plots: dbh, species, status flags (dead, stump, cut, fallen, broken, inclining), pOM, stump height, observations.
6. tree_stem_data_pilot.csv — Tree stem data for the pilot survey (separate design): includes subplot_id, tree_id, stem_id, dbh, status, pOM, stump, etc.

Key linkage and units:
- survey_id identifies site (4 = pilot; 5 = Mabalane; 6 = Marrupa; 7 = Gurue).
- plot_id uniquely identifies each plot; subplot_id used only in pilot study.
- Transect_id/quadrat_id link to specific transects or quadrats within each plot.
- Units are specified per dataset (e.g., length_m in meters; dbh in centimeters; weights in grams; canopy_cover_perc in percent).

## Data quality, governance, and metadata
- Quality control: data collected by trained teams; translations ensured; electronic data capture minimized manual entry errors; post-entry cleaning to remove anomalies; missing data explicitly flagged.
- Provenance: clear documentation of site methods, including deviations between sites and the pilot study.
- Metadata completeness: plot_metadata.csv captures coordinates, area, date, and data completeness flags (tree_stem_data, litter_data, canopy_data, cwd_data).
- Accessibility: datasets structured for cross-site discovery; linking keys (survey_id, plot_id, transect_id/quadrat_id) support traceability and reproducibility.
- Documentation notes:
  - Grass species data omitted; soil dataset not included.
  - Differences in methods across sites are acknowledged and described in textual notes and dataset descriptions.
  - DBH corrections provided for stems measured below 1.3 m to estimate DBH at breast height.

## DBH estimation and methodological notes
- When stems were measured below 1.3 m, a correction function was applied to estimate DBH at 1.3 m to ensure consistent biomass estimations.
- The correction uses taper-based parameters derived from central Mozambique Miombo wood species; height of measurement (p) must be less than 130 cm.
- This adjustment is important to maintain comparability across plots and to support allometric biomass calculations.

## Limitations and considerations for reuse
- Method evolution: varying methods across villages/sites may introduce subtle biases; differences are documented and should be considered in comparative analyses.
- Incomplete data: not all plots have complete datasets; missing data are recorded in plot_metadata.csv and should be handled appropriately in analyses.
- Omitted data: soil data and grass species composition for some plots were not included; the grass species data could not be robustly identified during the dry season.
- Spatial design differences: pilot study included nested sub-plots; Marrupa and Gurue used paired plots due to logistics; users should account for sampling design when modeling.

## Access, licensing, and references
- Data are provided with detailed data descriptions and methodological notes to facilitate reuse in studies of woodland structure, ecosystem services, and related ecological analyses.
- References cited for methodological context include Waddell (2002) on coarse woody debris, and project publications on charcoal production and land-use impacts (Baumert et al. 2016; Smith et al. in progress).

References (selected)
- Waddell KL (2002) Sampling coarse woody debris for multiple attributes in extensive resource inventories. Ecol Indic 1:139-153.
- Baumert S et al. (2016) Charcoal supply chains from Mabalane to Maputo: Who benefits? Energy Sustain Dev 33:129-138.
- Woollen E et al. (2016) Charcoal production in the Mopane woodlands of Mozambique: what are the trade-offs with other ecosystem services? Philos Trans R Soc B Biol Sci 371:20150315.