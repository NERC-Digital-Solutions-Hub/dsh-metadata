# Plant species cover and carabid beetle species counts (2018) and bird species counts (2019) in ungrazed native reforestation areas and grazed/ungrazed unforested and mature forest areas in the Scottish Highlands

## Aim and scope
- Assess biodiversity value of native reforestation in the Scottish Highlands relative to grazed/un-grazed unforested areas and mature Caledonian pineforest.
- Compare plants, carabid beetles, and birds across habitat statuses (reforestation, unforested, mature forest) and grazing regimes (grazed, ungrazed).
- Data collected for plants and carabids in 2018; birds in 2019; designed to inform restoration effectiveness and habitat value.

## Study area and experimental design
- Location: Glen Affric and Glen Moriston, central Scottish Highlands.
- Sites: Fourteen fenced native reforestation sites established between 1990 and 2012 by Trees for Life, Forestry Commission Scotland, and the National Trust for Scotland.
- Landscape context: Contains mature Caledonian pineforest, conifer plantations, unforested heathland, and regenerating native forest.
- Grazing exclusion: Sites fenced to exclude grazing (primarily deer); some areas within fences still experience limited grazing by other animals.
- Matched design: For each reforestation site, paired plots in the nearest unforested grazed area and in the nearest unforested ungrazed area; five pairs also include grazed and ungrazed mature Caledonian pineforest plots.
- Plot setup: 
  - Plants and carabids: 10 × 10 m plots.
  - Birds: 50 m radius plots.
  - Distances: 30–400 m between plant/carabid plots; 150–450 m separation between bird plots and their nearest plots.

## Treatments and plot representation
- Forest status: Reforestation, Unforested, Mature forest.
- Grazing status: Grazed, Ungrazed.
- All combinations represented except Reforestation × Grazed (deer grazing pressure prevents this pairing).

## Data collection methods
- Plant surveys:
  - Dates: 22 June – 5 July 2018.
  - Method: Three random 1 × 1 m quadrats per plot; species identified; percent cover recorded using the DOMIN scale.
  - Scope: Full plot-level list plus quadrat data; vascular plants to species level; some non-vasculars to genus/morphospecies.
- Carabid beetle surveys:
  - Dates: 7 June – 18 August 2018.
  - Method: Six pitfall traps per plot (near quadrat locations); traps filled with 1:3 propylene glycol:water; sampling intervals of two weeks initially, then four weeks; specimens identified to species.
  - Vouchers deposited in Oxford University Museum of Natural History.
- Bird surveys:
  - Dates: Two surveys per plot during 23 May – 1 June 2019 and 5 – 14 June 2019.
  - Method: 15-minute surveys between 6:00 and 11:30 AM; two surveyors per plot; birds identified visually or by song/call; weather noted.
  - Note: Some logistical constraints led to missing surveys in certain mature/un grazed plots; absence of records indicates no birds recorded during surveyed times.

## Data structure and datasets
- plant_carabid_plot_locations.csv
  - Contains locations and treatment details for the 10 × 10 m plots; includes plot type, forest status, grazing status, establishment year, grid references, and pitfall trap dates.
- bird_plot_locations.csv
  - Contains locations for the 50 m radius bird plots; includes plot type, forest and grazing status, year, grid references, and weather notes for each survey.
- plants.csv
  - Plant species data by site/plot/quadrat/date; includes DOMIN % cover, presence of additional species, seedling frequency, and taxonomic details.
- carabids.csv
  - Carabid species counts per plot/time; includes site, plot, time of sampling, species, and frequency.
- birds.csv
  - Bird records per plot; includes date, time, site, plot, distance from plot center, species, how recorded, and other metadata.
- Appendix 1 (roles of authors) and Table 2 (site-level details)
  - Site-specific information: year established, number of trees planted, planting method, presence of mature forest, and coordinates for each reforestation site.

## Data considerations and potential analyses
- Data richness across three trophic groups (plants, invertebrates, birds) enables multi-taxa biodiversity comparisons across habitat statuses and grazing regimes.
- Matched-pairs design supports inference on the effect of grazing exclusion and reforestation status on biodiversity.
- Temporal alignment: plant and carabid data from 2018; bird data from 2019; cross-taxa temporal consistency should be considered in analyses.
- Spatial scale and access: data come from multiple plots across diverse sites; researchers should account for site-level heterogeneity and potential spatial autocorrelation.
- Limitations and challenges (relevant for analysts):
  - Some plots (especially certain mature forest plots) have limited replication (fewer sites) and incomplete survey coverage due to logistics.
  - Reforestation × Grazed combination is absent, which constrains certain interaction analyses.
  - Data come from field surveys with potential detection biases (e.g., birds harder to detect in ungrazed vs grazed areas; weather conditions noted but not controlled).
  - Access to site metadata and long-term comparability may require careful metadata handling and data provenance checks.

## Implications for decision-making and reporting
- Provides a robust, multi-taxa assessment framework to inform native forest restoration and deer management policies in upland Scotland.
- Enables evaluation of whether fenced reforestation areas deliver biodiversity benefits relative to grazed and ungrazed unforested areas and mature pineforest.
- Data can support predictive modeling of biodiversity responses to restoration actions, grazing pressure, and landscape context.