# Structure and composition of woodlands across Mozambique: supporting documentation

- Quantitative datasets describing woodland structure and composition collected from 431 plots across 27 villages in three Mozambican districts (Mabalane, Marrupa, Gurue) and linked to household surveys and remote sensing through the ACES project (ESPA programme).

- Timeframe and locations
  - Mabalane District, Gaza Province: May–Sep 2014
  - Marrupa District, Niassa Province: May–Aug 2015
  - Gurue District, Zambezia Province: Sep–Dec 2015
  - Three districts span different land-use contexts (charcoal production, subsistence agriculture, smallholder commercial agriculture).

- Sampling design and village selection
  - Mabalane: 7 villages; 24 circular plots per village (total ≈ 168 plots); main land use focused on charcoal production; village sampling area defined as 5 km from village centre.
  - Marrupa: 10 villages; 12 plots per village (total ≈ 120 plots); woodland mainly Miombo; boundaries defined by village leaders to avoid overlap.
  - Gurue: 10 villages; 12 plots per village (total ≈ 120 plots); similar sampling logic to Marrupa.
  - Plot centers located within defined village sampling areas; plots randomly placed within those areas; Mabalane used a 5 km village radius, Marrupa and Gurue relied on village boundary delineations due to spatial overlap.

- Plot design and measurements
  - Main plots: circular plots with a 20 m radius (0.126 ha); within-plot measurements of all tree stems > 5 cm DBH.
  - Subplots/quadrat sampling:
    - Four 1 m^2 quadrats per plot to collect and weigh leaf litter, woody litter, and grass biomass.
    - Coarse woody debris (CWD) measured along four 20 m transects radiating from plot centre (in cardinal directions).
    - Canopy cover estimated with a Densiometer from plot centre in each cardinal direction.
  - Field notes: general plot observations on canopy, recent fire damage, slope; GPS waypoint for centre; elevation recorded.
  - Plot design variations: pilot study within Mabalane used nested sub-plots and varying plot radii to test designs; other sites followed the standard 20 m radius design.

- Measurements and data collected
  - Tree stems: all stems > 5 cm DBH recorded (local names, DBH at measurement point, status such as live/dead/cut/fallen, stump height if applicable).
  - Canopy: four measurements per plot (via Densiometer) as part of canopy cover assessment.
  - Litter and biomass: wet weights in the field for leaf litter, woody litter, and grass; subsamples dried in lab to determine dry weights; litter and grass sub-sample weights include field and lab measurements.
  - Coarse woody debris: length, diameter at intersection with transects, decomposition class, and local species name.
  - Soil samples were collected but the soil dataset is not included in these supporting data (to be submitted separately).

- Data structure and content
  - Six spreadsheets (datasets) with links via survey_id, plot_id, and, for the pilot, subplot_id:
    1) cwd.csv — measurements of each coarse woody debris piece along transects per plot.
    2) cwd_decomposition.csv — qualitative decomposition class and reduction factor for biomass corrections.
    3) plot_metadata.csv — plot-level metadata: coordinates, plot size, date, canopy observations, litter/grass weights, and data completeness indicators.
    4) quadrat_data.csv — biomass data (grass, leaf litter, woody litter) and canopy cover per quadrat.
    5) tree_stem_data.csv — tree-stem measurements for all stems > 5 cm DBH within plots (dbh, position, status, species, etc.).
    6) tree_stem_data_pilot.csv — tree-stem measurements from the pilot study (nested plots in pilot).
  - Data linkage: survey_id identifies site (4 = pilot, 5 = Mabalane, 6 = Marrupa, 7 = Gurue); plot_id identifies plots; subplot_id used only for pilot; transect_id/quadrat_id link data within plots.

- Quality control and data handling
  - Data collection trained field teams; translators aided fieldwork (Portuguese translation).
  - Electronic data capture (ODK on Android tablets); in-field checks for errors; post-collection cleaning to remove outliers and erroneous entries; all data translated to English where needed.
  - Missing or incomplete data flagged in plot_metadata.csv; not all plots have complete data across all datasets.
  - Grass species data omitted due to identification challenges in the dry season; soil dataset excluded from this release.
  - Grass and litter weights include a wet weight measure with lab-dried weights; some canopy and other qualitative observations recorded as notes.

- Data nuances and limitations
  - Method evolution across sites means small methodological differences are possible; any differences will be documented in the text and dataset descriptions.
  - Grass species identification issues led to omission of grass composition by species; dominant grasses recorded but species-level biomass data unavailable.
  - Soil data not included here; the fieldwork did collect soil samples.
  - Plot shapes are approximated (edge delineation may yield octagonal shapes in practice); DBH measurement corrections applied when stems were measured below 1.3 m to estimate at breast height (1.3 m).
  - DBH correction for sub-breast measurements uses a taper-based function derived from central-Mozambique Miombo species; the function adjusts dm to dbh based on measurement height p.

- Key references and context
  - ESPA ACES project framework and aims: linking land-use change to ecosystem services and rural wellbeing.
  - Coarse woody debris classification and biomass correction framework (Waddell 2002).
  - Charcoal production and land-use studies informing site selection and interpretation (Baumert et al. 2016; related works in progress).

- Practical use for analysts
  - Rich multi-layered data to analyze woodland structure, biomass partitioning (litter, grass, woody debris), canopy characteristics, and tree-stem demographics across multiple land-use contexts.
  - Potential to link plot-level woodland structure with household-level wellbeing and landscape-scale remote sensing data (as part of the ACES/ESPA framework).
  - Datasets enable correlation analyses between woodlands and ecosystem services, with attention to data completeness and site-specific methodological differences.