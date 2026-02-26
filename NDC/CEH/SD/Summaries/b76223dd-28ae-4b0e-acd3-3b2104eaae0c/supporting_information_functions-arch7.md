# Does restoring native forest restore ecosystem functioning? Evidence from a large-scale reforestation project in the Scottish Highlands

- Overview
  - Evaluates whether native forest restoration restores ecosystem functioning by measuring multiple ecosystem functions across reforestation, unforested, and mature forest habitats.
  - Study area spans central Scottish Highlands (Glen Affric and Glen Moriston) with fenced reforestation plots and surrounding landscape.
  - Timeframe: established plots from 1990–2012; data collection in 2018; compares reforestation sites to adjacent unforested and mature habitats.
  - Experimental design mirrors a hierarchical, space-for-function approach to capture effects of forest status and grazing exclusion on ecosystem processes.

- Study Area and Timeline
  - Locations: Glen Affric and Glen Moriston, central Scottish Highlands; landscapes include mature Caledonian pinewood, conifer plantations, heathland, and regenerating native forest.
  - Reforestation sites fenced to exclude grazing (primarily deer; some low-level feral boar and sheep present elsewhere in the landscape).
  - Mature forest plots exist at three sites; five pairs of grazed/ungrazed mature-forest plots established.
  - Plot establishment and planting details vary by site, with native Caledonian pinewood species planted from local seed sources.

- Experimental Design and Treatments
  - Treatments and combinations represented across plots:
    - Forest status: Unforested (unplanted), Reforestation, Mature forest
    - Grazing status: Grazed, Ungrazed
    - All combinations present except Reforestation × Grazed (not observed due to deer pressure)
  - Sampling units: 10 × 10 m plots
  - Hierarchical design: 14 focal reforestation sites, associated unforested areas, and three sites with associated mature forest; plot spacing 30–400 m within sites.
  - Sampling framework includes matched pairs for reforestation plots (ungrazed) with corresponding unforested grazed and unforested ungrazed plots to disentangle effects of establishment and grazing.

- Plot Layout and Sampling Design
  - Total plots: 52 plots across 14 sites (spanning reforestation, unforested, and mature forest with grazed/ungrazed statuses).
  - Plot placement: Reforestation plots positioned as best-case forest establishment in each site; paired with nearby unforested plots representing prior land-use conditions.
  - Data collection targets multiple ecosystem functions and components to enable cross-habitat comparisons.

- Data Collected and Methods
  - Aboveground tree carbon
    - Measurements: dbh for all trees (and multi-stemmed stems); species-specific allometric equations used to estimate biomass.
    - Carbon conversion: biomass to carbon using published carbon concentrations (approx. 49–50% depending on leaf type); plant-level estimates aggregated to plot level (kg/m2).
  - Topsoil carbon and nitrogen
    - Sampling: top 10 cm soil cores (3 cores per plot, 3 per bulk-density core); some plots had reduced sample sizes (n = 12) due to wet conditions.
    - Analyses: bulk density; total carbon and nitrogen via CN analyser following ISO protocols; stocks calculated per m2 using bulk density and percentage carbon/nitrogen.
  - Decomposition rate
    - Method: Tea Bag Index with six pairs of teabags per plot (green tea and rooibos) buried at 8 cm depth for ~54–67 days.
    - Outcome: decomposition rate constant (k) per plot.
  - Soil invertebrate feeding
    - Method: bait lamina sticks (six per plot) with perforations containing a cellulose/wheat bran/activated charcoal substrate; exposure ~30 days with staged retrieval to assess feeding activity.
    - Outcome: per-perforation feeding indicators and overall proportion of sticks showing feeding activity.
  - Tree regeneration
    - Assessment: all young trees with dbh < 2.5 cm counted within plots; categorized by height classes.
  - Ground-layer and moss height
    - Ground-layer: three 1 × 1 m quadrats per plot; measured mean shrub height and moss depth at multiple points per quadrat.
  - Shrub layer and moss depth (additional metrics)
    - Shrub height: mean height across three quadrats per plot; focus on typical understory species.
    - Moss depth: mean depth across three quadrats per plot.

- Data Structure and Accessibility
  - plot_locations.csv: spatial layout and plot-level metadata
    - Fields include: ID, Site, Plot type (reforestation ungrazed; unforested grazed; unforested ungrazed; mature forest grazed; mature forest ungrazed), Forest_status, Grazing_status, Year established, Grid_ref.
  - aboveground_carbon.csv: plot-level aboveground carbon (kg/m2)
  - topsoil_C_N.csv: topsoil carbon (%), nitrogen (%), bulk density, and derived stocks (kg/m2)
  - decomposition_rate.csv: Tea Bag Index results; k values per plot
  - soil_invert_feeding.csv: bait lamina feeding data; per-bait and per-plot summaries; includes proportion and binary Eaten indicator
  - seedling_regeneration.csv: seedling counts by species and height category
  - shrub_height.csv: mean shrub layer height per plot
  - moss_height.csv: mean moss layer depth per plot
- Data Characteristics and GIS Relevance
  - Spatial granularity: 10 × 10 m plots enabling high-resolution mapping of carbon stocks, soil properties, and biodiversity indicators across habitat types and grazing regimes.
  - Multifunctional metrics: enables mapping of aboveground carbon, soil carbon/nitrogen stocks, decomposition, invertebrate activity, regeneration, and understory structure.
  - Hierarchical design supports spatial comparisons among reforestation, unforested, and mature habitats, as well as grazing versus ungrazed conditions.

- Limitations and Considerations for GIS and Mapping
  - Grazing × reforestation interaction unavailable (no observed instances) which limits some interaction mapping.
  - Some soil data have reduced sample sizes (n = 12) due to field constraints.
  - Heterogeneity across sites (drainage/topography/topsoil conditions) may influence plot-level comparisons.
  - Data are time-stamped to 2018 for sampling; temporal dynamics beyond this snapshot are not included in the dataset.

- Key Implications for GIS Products
  - Enables creation of maps showing spatial patterns of ecosystem function across habitat types and grazing statuses.
  - Supports spatial prioritisation for restoration by highlighting areas with greater potential for carbon sequestration, soil health, and regeneration.
  - Provides a rich, harmonised dataset for integrating ecological function metrics with habitat and management layers in map-based data products.