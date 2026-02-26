# Structure and composition of woodlands across Mozambique: supporting documentation

## Overview
- Quantitative dataset describing woodland structure and composition from 431 plots across 27 villages in three districts of Mozambique (Gaza, Niassa, Zambezia).
- Data collected 2014–2015 as part of the ACES project within the ESPA programme to understand how land use affects ecosystem services and human well-being.
- Measurements cover tree stems (>5 cm DBH), litter and grass biomass, coarse woody debris, and canopy cover; plots are circular with 20 m radius (0.126 ha).
- Data are intended for linking woodland structure to ecosystem services and broader landscape-scale analyses (with household surveys and remote sensing).

## Spatial and sampling design
- Study sites and village selection
  - Mabalane (Gaza Province): 7 villages plus pilot study.
  - Marrupa (Niassa Province): 10 villages.
  - Gurue (Zambezia Province): 10 villages.
- Plot layout and location
  - Circular plots with 20 m radius within defined village sampling areas.
  - Mabalane: village sampling areas defined by 5 km radius from village center (representing typical household access to woodland resources).
  - Marrupa and Gurue: village boundaries determined via local leaders and geographic references due to overlaps; plots randomly placed within village limits.
- Plot and subplot design
  - Mabalane, Marrupa, Gurue: 24 plots per village in Mabalane; 12 plots per village in Marrupa and Gurue.
  - Pilot study used varying plot designs (nested sub-plots) to test methods; larger plots up to 25 m with smaller nested plots for stems.
- Plot location data
  - Plot center coordinates recorded and stored (origin_local_x, origin_local_y) with projection details (WGS84, UTM zone).

## Data content and structure
- Datasets (CSV files)
  - cwd.csv: measurements for each coarse woody debris (CWD) piece.
  - cwd_decomposition.csv: qualitative decomposition class descriptions and correction factors for biomass.
  - plot_metadata.csv: plot-level metadata (coordinates, plot radius/area, date, slope, canopy observations, completeness flags, missing data notes).
  - quadrat_data.csv: biomass weights (leaf litter, woody litter, grass) and four canopy cover estimates per plot.
  - tree_stem_data.csv: all tree stems >5 cm DBH within plots (diameter, species, local name, status, stump height, etc.).
  - tree_stem_data_pilot.csv: tree stem data for the pilot study (nested plot design); similar fields to tree_stem_data.csv but with subplot identifiers.
- Key identifiers and linking
  - survey_id identifies site: 4 = pilot, 5 = Mabalane, 6 = Marrupa, 7 = Gurue.
  - plot_id uniquely identifies each plot; survey_id and plot_id link across datasets.
  - subplot_id used for pilot study (nested plots); transect_id and quadrat_id link to specific transects/quadrats within plots (east/north/south/west or corresponding quadrants).
- Measured variables and units
  - Trees: DBH in cm, POM (point of measurement), species_name, recorded_local_name, live/dead, cut, fallen, broken, inclining, pcent_missing, stump_height_m, observations.
  - Coarse woody debris: length_m, diameter_intersection_cm, decomposition_class (0–5), recorded_local_name.
  - Decomposition metadata: structure, wood_texture, wood_colour, branch_twig_condition, reduction_factor (0–1).
  - Litter and biomass: wet_weight_g and dry_weight_g for leaf litter, woody litter, and grass; canopy_cover_perc (from Densiometer).
  - Plot metadata: origin_local_x/y, projection, radius, area_ha, date, altitude, slope_obs, burnt, canopy_obs_a, completeness flags (tree_stem_data, litter_data, canopy_data, cwd_data).
- Data quality and completeness
  - Some plots have incomplete data; missing data are indicated in plot_metadata.csv and related datasets.
  - Grass species data omitted due to identification issues in the dry season; soil data collected but not included here.
  - Data were cleaned and checked post-collection; field teams trained; translations from Portuguese to English performed by lead author.
  - Acknowledges methodological evolution across sites; differences highlighted in dataset descriptions.

## Methods and instrumentation
- Field methods
  - Circular plots (20 m radius) with tree stems >5 cm DBH recorded; stumps included; DBH sometimes measured below 1.3 m and adjusted to 1.3 m via a correction function.
  - Litter and grass biomass collected with four 1 m2 quadrats per plot; weights recorded in field and lab.
  - Coarse woody debris measured along four 20 m transects per plot; diameter, length, and decay state recorded.
  - Canopy cover estimated with a Densiometer; multiple measurements per plot when possible.
- Instruments and data capture
  - GPS: Garmin etrex 10/30 for plot centers.
  - DBH measurement: standard forestry DBH tapes (0.1 cm accuracy).
  - Densiometer: canopy cover measurements.
  - Data collection: Android tablets with Open Data Kit (ODK); wet/dry weights with hanging scales; lab weights with high-precision scales.
- Data processing and correction
  - DBH adjustments to 1.3 m height applied when measurements were taken lower; stem taper-based correction function documented for biomass estimation.
  - Data cleaned for outliers and anomalies; missing values documented; observations translated to English from Portuguese.

## Spatial utility for GIS specialists
- The dataset provides geolocated, plot-level spatial data suitable for map-based analyses of woodland structure and composition across Mozambique.
- Linkable via survey_id and plot_id to produce landscape-level maps of canopy cover, biomass components, and coarse woody debris distribution.
- Can be integrated with remote sensing data to scale plot measurements to landscape extent; compatible with GIS workflows in QGIS (used during sampling) or similar platforms.
- Metadata enables spatial quality assessment: coordinates, projection, altitude, slope, canopy observations, and data completeness indicators.

## Limitations, caveats, and guidance for use
- Method evolution across sites: some plots have different designs (pilot vs. standard surveys); harmonize analyses by site or explicitly model design differences.
- Missing data: not all plots have complete measurements; use plot_metadata completeness indicators to filter datasets as needed.
- Grass species data: omitted due to identification issues; biomass estimates exclude species-level grass composition.
- Soil data: not included in these datasets; if soil context is required, separate dataset would be needed.
- DBH corrections: apply the provided taper-based correction when DBH measurements are below 1.3 m for biomass calculations.
- Data provenance: ACES/ESPA project context and references to Waddell 2002 for CWD methodology; ensure citation in analyses.

## Provenance and references
- Project: ACES (Ecosystem Services for Poverty Alleviation), ESPA-funded data collection.
- Related literature and methods:
  - Waddell KL (2002) on coarse woody debris sampling.
  - Baumert et al. (2016) on charcoal supply chains in Mabalane.
  - Woollen et al. (2016) on trade-offs with ecosystem services in Mopane woodlands.
- Data management and quality control described by lead author; data were collected and curated with local community assistance and translated from Portuguese to English.