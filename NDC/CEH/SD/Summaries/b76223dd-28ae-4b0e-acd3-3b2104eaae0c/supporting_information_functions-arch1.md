# The response of plants, carabid beetles and birds to 30 years of native reforestation in the Scottish Highlands

- Aims and context
  - Examines ecosystem functioning in the Scottish Highlands where native forest regeneration is being prioritized, focusing on the effects of long-term native reforestation compared with unforested, grazed/un-grazed, and mature Caledonian pinewood habitats.
  - Investigates aboveground carbon, soil carbon and nitrogen, decomposition, soil invertebrate feeding, tree regeneration, and ground-layer vegetation as indicators of ecosystem function.

- Study design and site context
  - 14 fenced native reforestation sites in Glen Affric and Glen Moriston, established 1990–2012, with deer grazing excluded to varying degrees.
  - For each reforestation site, paired plots in nearby unforested areas (grazed and ungrazed) were sampled, plus plots in three sites with associated mature Caledonian pinewood (both grazed and ungrazed).
  - A hierarchical sampling design using 10 m × 10 m plots; location and layout detailed in site information.

- Treatments and sampling framework
  - Treatments represented in all possible combinations of forest status (reforestation, unforested, mature) and grazing status (grazed, ungrazed); reforestation × grazed combination not present due to deer pressure.
  - At each site, plots were 30–400 m apart; mature forest plots were located within existing Caledonian pinewood remnants.
  - Sample sizes per forest × grazing category provided (e.g., Ungrazed Unforested, Ungrazed Reforestation, Ungrazed Mature, etc.), with minor exceptions where soil cores could not be extracted.

- Data collection and measurement methods
  - Aboveground tree carbon
    - Measured diameter at breast height (dbh) for all trees; species-specific allometric equations used to estimate aboveground biomass.
    - Biomass converted to carbon using fixed carbon concentrations (49% for broadleaf, 50% for conifers).
  - Topsoil carbon and nitrogen
    - Top 10 cm soil samples collected; three cores per plot combined for analysis; bulk density measured; carbon and nitrogen percent determined via ISO-standard combustion.
    - Stocks calculated from carbon/nitrogen content and bulk density.
  - Decomposition rate
    - Tea Bag Index used: six pairs of teabags per plot buried at 8 cm depth for ~61 days; final mass used to calculate decomposition rate constant k.
  - Soil invertebrate feeding
    - Bait lamina sticks (six per plot) buried to assess feeding activity; 16 perforations per stick monitored for evidence of feeding; proportion and overall feeding recorded.
  - Tree regeneration
    - Seedlings counted in each plot for individuals with dbh < 2.5 cm; categorized by height classes.
  - Ground-layer and moss assessment
    - Ground-layer height measured with three 1 × 1 m quadrats per plot; moss depth averaged across quadrats.
  - Other vegetation metrics
    - Shrub layer height (mean across three quadrats per plot) and moss depth data captured as supplemental habitat structure indicators.

- Data structure and available datasets
  - plot_locations.csv: plot identifiers, site and forest/grazing treatments, year of reforestation establishment, grid references.
  - aboveground_carbon.csv: per-plot total aboveground tree carbon (kg/m2).
  - topsoil_C_N.csv: topsoil carbon and nitrogen (%), bulk density, and derived carbon/nitrogen stocks (kg/m2).
  - decomposition_rate.csv: Tea Bag Index-derived decomposition rate constant (k) per plot.
  - soil_invert_feeding.csv: bait lamina feeding data per plot, including per-bait perforation results and overall feeding indicators.
  - seedling_regeneration.csv: seedling counts by species and height category per plot.
  - shrub_height.csv: mean shrub-layer height per plot.
  - moss_height.csv: mean moss-depth per plot.

- Site-level planting and habitat details
  - Table 1 provides site-level information for each reforestation site (size, year established, number of trees planted, trees per hectare, species composition, planting method, presence of mature forest, coordinates).
  - Planting methods include hand screefing and machine mounding; species categories include Scots Pine (SP), broadleaf mixes (BL), aspen (A), birch (B), and others; some sites include mature forest presence, reflecting legacy habitat context.
  - Several sites are noted as fenced to exclude grazing; some sites show natural regeneration within mature forest.

- Data quality, caveats, and scope
  - Some soil core data were not extractable at two unforested, ungrazed plots, reducing sample size for those categories to n = 12.
  - Data cover a broad suite of ecosystem functions, enabling correlations and modeling to assess how reforestation and grazing modification influence multiple functions and potential trade-offs.
  - Appendix 1 lists author roles (experimental design, field data collection, and project background) and references methodological work underpinning the study.

- Relevance for analysis and interpretation
  - The integrated, multi-function dataset supports analyses of how long-term native reforestation affects carbon storage, soil health, decomposition dynamics, belowground invertebrate activity, and early plant regeneration compared with grazed/un-grazed unmanaged and mature forest states.
  - Enables assessment of whether restoration benefits ecosystem functioning at the plot level and, with appropriate scaling, at landscape scales in the Scottish Highlands.
  - Data are suitable for developing predictive models and for exploring correlations among aboveground and belowground processes in restored versus reference conditions.