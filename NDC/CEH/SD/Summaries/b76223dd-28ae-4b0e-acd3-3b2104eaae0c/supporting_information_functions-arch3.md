# The response of plants, carabid beetles and birds to 30 years of native reforestation in the Scottish Highlands

- Objective and scope
  - Assess ecosystem functioning responses to native reforestation in the Scottish Highlands.
  - Compare reforestation plots to unforested grazed and ungrazed plots, and to mature Caledonian pinewood where available.
  - Focus on multiple ecosystem processes: carbon storage, soil properties, decomposition, soil invertebrate activity, tree regeneration, and ground-layer vegetation.

- Study area and design
  - Location: Glen Affric and Glen Moriston in the central Scottish Highlands.
  - 14 fenced reforestation sites established 1990–2012 to exclude deer grazing; surrounding landscape includes mature pinewood, conifer plantations, heathland, and regenerating native forest.
  - Treatments and sampling
    - Treatments represented in all combinations: forest status (reforestation, unforested, mature forest) and grazing status (grazed, ungrazed).
    - Reforestation × grazed combination not present due to deer grazing pressure.
    - Three mature-forest plots across five units (grazed and ungrazed) to reflect target habitat.
    - Plot size: 10 × 10 m; hierarchical sampling with 52 plots in total across sites.
    - Each reforestation, ungrazed plot matched to:
      - a nearby unforested, grazed plot
      - a nearby unforested, ungrazed plot
    - Mature forest plots: two pairs per site at two sites, with at least 500 m separation.
  - Planting and site details
    - Native Caledonian pinewood species planted from local seed sources; reforestation sites vary in age and planting methods (hand screefing or machine mounding).
    - Some sites include areas of natural regeneration or mature forest; site-specific information provided in Table 1 (e.g., Athnamulloch One/Two, River Flat, Dundreggan, Allt Fearna, etc.).

- Data collected and ecosystem functions measured
  - Aboveground tree carbon
    - Measurement: all trees with dbh > 2.5 cm; 10 × 10 m plots.
    - Biomass estimated with species-specific allometric equations; carbon assumed as 49% for broadleaves and 50% for conifers.
  - Topsoil carbon and nitrogen (0–10 cm)
    - Sampling: three cores per plot, bulk density characterization, homogenized for analysis.
    - Analysis: total C and N by CN analyser following ISO protocols; bulk density and stocks calculated for kg/m2.
  - Decomposition rate
    - Tea Bag Index method: six pairs of teabags per plot (green and rooibos) buried at 8 cm for ~61 days; final mass used to derive decomposition rate constant k.
  - Soil invertebrate feeding
    - Bait lamina sticks: six per plot, with 16 perforations each; exposure and feeding assessed after 15 and 30 days.
    - Output: proportion of perforations showing feeding and overall bait stick consumption.
  - Tree regeneration
    - Seedling assessment: all young trees with dbh < 2.5 cm categorized by height (<50 cm, 50–100 cm, 100–150 cm, ≥150 cm) and counted per species.
  - Ground-layer and moss vegetation
    - Ground-layer height: mean height across three 1 × 1 m quadrats per plot (measured at five diagonal points per quadrat).
    - Moss depth: mean depth across the same sampling framework.
  - Species and lifeform
    - Planted species and leaf/bark types recorded to support forest structure interpretation.
  - Data collection cadence
    - All measurements collected in the summer of 2018 to compare reforestation plots with adjacent reference states.

- Data structure and accessibility
  - Plot-level and site-level data
    - plot_locations.csv: locations and plot treatment details (site, plot type, forest status, grazing status, year established, grid reference).
  - Ecosystem function datasets (CSV files)
    - aboveground_carbon.csv: total carbon per plot (kg/m2).
    - topsoil_C_N.csv: topsoil carbon (%), nitrogen (%), bulk density, and derived stocks (kg/m2).
    - decomposition_rate.csv: Tea Bag Index k values per plot and teabag type.
    - soil_invert_feeding.csv: bait lamina feeding data per plot, including per-bait perforation results and proportion/eaten metrics.
    - seedling_regeneration.csv: seedling counts by species, height category, and plot.
    - shrub_height.csv: mean shrub layer height per plot.
    - moss_height.csv: mean moss layer depth per plot.
  - Data management notes
    - Data tables include plot IDs, site IDs, plot types, and sampling dates to support cross-comparison and meta-analysis.
    - Appendix 1 documents roles of authors for experimental design, fieldwork, and data collection.

- Key methodological details
  - Biomass and carbon calculations
    - Allometric equations selected by species or genus, prioritizing UK-relevant models and highest R2 values when multiple models exist.
    - Carbon conversion factors: 49% for broadleaves, 50% for conifers.
  - Soil analyses
    - ISO protocols used for carbon and nitrogen analysis; bulk density and carbon/nitrogen stocks calculated from measured bulk density and C/N content.
  - Decomposition and soil biota
    - Tea Bag Index standard protocol (54–67 days exposure) for decomposition rate.
    - Bait lamina method for assessing soil faunal feeding activity.
  - Regeneration and understory
    - Height-based categorization for recruitment; ground-layer and moss metrics provide context for understory development.

- Contextual references and acknowledgments
  - Background literature underpinning methods and site selection (e.g., Mason et al., 2004; Tanentzap et al., 2013; Warner et al., 2021) and standard biomass and soil methods (Muukkonen & Mäkipää, 2006; Zianis et al., 2005; ISO standards).
  - Appendix 1 lists author roles across experimental design, fieldwork, and data collection.

- Appendices and contribution mapping
  - Roles of authors for experimental design, background information, and data collection are documented (Emily Warner, Andy Hector, Owen Lewis, Nick Brown, etc.).