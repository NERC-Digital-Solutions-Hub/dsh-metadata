# Structure and composition of woodlands across Mozambique: supporting documentation

- Aims and scope
  - Quantifies woodland structure and composition across 27 Mozambican villages (431 plots) in three districts and three provinces.
  - part of the ESPA-funded ACES project to understand how land use changes affect ecosystem services and rural wellbeing; data linked to household surveys and remote sensing to scale to landscape level.
  - Data help quantify woodland structure, biomass, and canopy characteristics and support analysis of ecosystem services provision.

- Geographic and temporal coverage
  - 27 villages: 7 in Mabalane District (Gaza), 10 in Marrupa District (Niassa), 10 in Gurue District (Zambezia).
  - 431 plots sampled between 2014 and 2015: Mabalane (May–Sept 2014), Marrupa (May–Aug 2015), Gurue (Sept–Dec 2015).
  - Plots randomly located within village sampling areas; circular plots of 20 m radius (0.126 ha).

- Data collected per plot
  - Tree stems >5 cm DBH: species names (local and scientific), DBH at 1.3 m, status (live/dead/cut/broken), stump height, and other stem attributes.
  - Litter and biomass: leaf litter, woody litter, and grass biomass measured in four 1 m2 quadrats per plot (wet and dry weights for litter/grass; canopy cover via Densiometer).
  - Coarse woody debris: measured along four 20 m transects per plot (length, diameter at intersection, decomposition class, local species).
  - Canopy cover: four measurements per plot (Densiometer).
  - Soils: collected but not included in this dataset; a separate soil dataset exists.
  - Grass species data: initially planned but omitted due to identification difficulties in the dry season.
  - Data linked across datasets via survey_id, plot_id, and, for the pilot, subplot_id.

- Plot and sampling design nuances
  - Mabalane: 24 circular plots per village (pilot village had 19 plots); focus on charcoal production areas and subsistence woodland use.
  - Marrupa and Gurue: 12 plots per village (paired by proximity to reduce travel); gradient of land-use intensity within districts.
  - Pilot study: variable plot sizes and nested sub-plots to test designs; differences in measurement protocols (e.g., limited status data, no stump height, two nested plots with different DBH cutoffs).

- Data structure and datasets
  - cwd.csv: detailed measurements of each coarse woody debris piece per plot/transact.
  - cwd_decomposition.csv: decomposition class descriptions and reduction factors for biomass corrections.
  - plot_metadata.csv: plot-level metadata (coordinates, radius, area, date, slope, burnt status, canopy observations) plus data completeness indicators (tree_stem_data, litter_data, canopy_data, cwd_data) and notes on data quality.
  - quadrat_data.csv: biomass weights for four quadrats per plot and canopy cover per quadrat.
  - tree_stem_data.csv: all stems >5 cm DBH per plot with fields for species, local/scientific names, DBH, measurement point (POM), and stem status flags (dead, stump, cut, fallen, broken, inclining) plus missing data indicators and stump_height.
  - tree_stem_data_pilot.csv: pilot survey stems with subplot_id, similar fields to tree_stem_data but reflecting pilot design.
  - Cross-dataset linkage: survey_id, plot_id, and where applicable subplot_id; transect_id or quadrat_id included to locate measurements within plots.

- Data quality control and processing
  - All data quality assured by lead author; field teams trained; translators used for local languages.
  - Electronic data capture (ODK on tablets) with predefined response options to minimize ambiguity.
  - Post-collection cleaning to remove or correct anomalous values; translations standardized to English.
  - Notes on completeness and potential errors included in plot_metadata; some surveys lack full data due to field challenges.

- DBH estimation and methodological adjustments
  - For stems measured below 1.3 m, a correction function estimates DBH at breast height (DBH at 1.3 m) to avoid biomass overestimation.
  - Function derived from Miombo species measurements in central Mozambique and applied where applicable.

- Important limitations and caveats
  - Methods evolved across sites; some site-specific differences are noted in the documentation and dataset descriptions.
  - Not all plots have complete data for every parameter; missing data are recorded in plot_metadata.csv.
  - Grass species biomass by species was not robustly recorded; soil data collected but not included here.
  - Plot shapes are approximated (edge may be octagonal in practice) for practical measurement purposes; potential scaling considerations when aggregating.

- References and context
  - Methodological references linked to coarse woody debris sampling and canopy/biomass estimation.
  - Related works on charcoal supply chains and land-use impacts on livelihoods provide context for the study objectives.

- Access and reuse notes
  - Datasets are structured for cross-dataset linking via survey_id, plot_id, and (pilot) subplot_id, enabling self-described data products (dashboards, tables, etc.) and analyses across sites.
  - Users should account for site-specific methodological differences and missing data indicators when aggregating or comparing plots across districts.