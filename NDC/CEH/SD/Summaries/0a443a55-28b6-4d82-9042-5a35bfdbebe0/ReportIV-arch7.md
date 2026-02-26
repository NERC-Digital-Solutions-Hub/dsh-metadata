# Soil Biodiversity Thematic Programme: Sourhope Site Summary

- Overview
  - Four-year summary of the NERC Soil Biodiversity Thematic Programme at Sourhope, focusing on aboveground productivity, plant community composition, and diversity.
  - Site: Macaulay Land Use Research Institute, Sourhope Farm, Scottish Borders.
  - Key management factors driving botanical changes: mowing, fertilisation (nitrogen and/or lime), and insecticide application.
  - Main data streams: biomass production, plant species abundance, and community diversity; automated weather data; soil pH and moisture; bryophyte presence; point-analysis plant surveys; and CSR-based functional classification.

- Site design, treatments, and management
  - Experimental setup: Rigg Foot site with 5 replicate blocks along downslope gradients; each block contains 6 main plots, subdivided into 10 sub-plots; 0.5 m x 0.5 m cells for end-user research group allocation.
  - Treatments (plot-level): Control 1, Control 2 (no treatment), Nitrogen, Lime, Nitrogen & Lime, Insecticide (formerly Biocide, Dursban 4 OPA).
  - Site-level management: monthly mowing May–September to ~6 cm; insecticide applied after mowing on insecticide plots; spring fertiliser (N and/or lime) applied to designated plots.
  - Data collection co-ordination: 1998 baseline botanical survey; annual biomass sampling; July/August point-analysis surveys (2000, 2001, 2002); soil pH (5 cm depth) and moisture; on-site Automatic Weather Station data since 1999; additional small-scale botanical and soil surveys.

- Data collection methods and outputs
  - Above-ground productivity: seasonal biomass from 0.5 m2 cells within sub-plots; samples oven-dried and weighed.
  - Botanical surveys: 25-point baseline quadrant (1998); 100-point point analysis (2000–2002) within selected cells; bryophyte identification enhanced in 2002.
  - Soil metrics: pH at ~5 cm depth; soil moisture via theta probe in 2002; periodic soil sampling since 1998.
  - Data analyses: split-plot ANOVA for biomass by treatment and year; PCA on point-analysis species data; Shannon diversity index (species diversity) across years; functional-group (CSR) analysis (stress-tolerant, competitive-stress-ruderals, and combinations).

- Key results (2002 findings and trends)
  - Biomass and productivity
    - General long-term rise in biomass across most treatments since 1999, with the Nitrogen+Lime plots remaining the most productive.
    - 2002 biomass declined relative to 2001 across most treatments; Control 2 plots showed the largest relative drop.
    - A slope-position effect: lower on Block 1 (bottom) and higher on Block 5 (higher fall in productivity), indicating spatial heterogeneity.
  - Fertilisation and soil chemistry
    - Lime dramatically increased soil pH to near 7.0 in the upper profile; nitrogen also raised pH but to a lesser extent.
    - Higher pH generally associated with higher biomass; however, the positive relationship weakened when both nitrogen and lime were applied together.
    - A negative correlation between soil moisture and pH; drier, limed plots tended to be more productive.
  - Insecticide effects and diversity
    - Insecticide plots show higher Shannon diversity indices over time, though causality between reduced herbivory and diversity is not definitively established.
    - The insecticide regime may favour certain palatable species that can persist under reduced herbivory, contributing to maintained or increased diversity.
  - Mowing effects
    - Consistent decline in Agrostis capillaris and Agrostis vinealis across most treatments since 2000, suggesting a site-wide mowing response rather than treatment-specific effects.
    - Festuca rubra expands particularly in more fertile, lime- or nitrogen-treated plots; bryophytes (mosses) increase across the site, especially under unimproved conditions.
  - Community composition and functional groups
    - Point-analysis shows greater abundance of legumes and grasses typical of improved pastures (e.g., Festuca rubra, Poa pratensis) in fertilised plots; unimproved plots retain more stress-tolerant taxa (e.g., Festuca ovina, Agrostis spp., bryophytes).
    - CSR-based functional groups shift with treatments: unfertilised plots favour stress-tolerators; N+L plots favour competitive-stress-ruderal assemblages; SR/CS-R groups decline with increased disturbance removal (mowing) and fertilisation patterns.
    - By 2002, significant treatment differences emerge across all functional groups; N&L plots show dominance of C-S-R types; stress-tolerators remain more prominent in unimproved plots.
  - Vegetation structure and bryophytes
    - Bryophyte abundance rises across the site, contributing to an increasing share of total hits and biomass, particularly in unimproved plots.
    - Moss expansion aligns with mowing and reduced disturbance; Agrostis declines accompany bryophyte increases.

- Data visualization and interpretation (GIS-relevant)
  - Spatial mapping opportunities
    - Plot-level treatments overlaid on block grids with year-by-year biomass and diversity surfaces.
    - pH, moisture, and biomass rasters by year to identify spatial correlations with slope position and treatment effects.
    - PCA scores and loadings mapped by plot to display treatment-driven clustering of vegetation communities.
    - Functional group distribution maps (S, CSR, SR/CSR) by plot to illustrate shifts in ecological strategies over time.
  - Temporal analysis
    - Time-series layers for biomass, soil pH, and Shannon diversity (1999–2002) by treatment.
    - Mapped mowing events and insecticide applications as temporal layers to assess their spatial footprint relative to vegetation responses.
  - Species and bryophyte distribution
    - Point-analysis results provide species-level and bryophyte-level presence data suitable for species distribution mapping and hotspot analysis.
    - Rank-abundance data and changes in dominant taxa by year and treatment can be visualized as stacked bar maps or area-weighted charts.

- Data availability and considerations for GIS work
  - Dataset structure: hierarchical blocks → plots → sub-plots → 0.5 m2 cells; multiple annual data streams (biomass, species hits, pH, moisture, weather).
  - Appendices provide comprehensive species lists, biomass tables, and diagnostics (e.g., PCA loadings, diversity indices).
  - Data caveats: 2002 weather data includes missing periods due to on-site weather-station issues; some smaller surveys were limited to certain plots or years; certain plots (Control 2) were not surveyed in some years.
  - Potential GIS outputs: year-specific and year-over-year biomass maps by treatment; pH and moisture distribution surfaces; species richness and diversity heatmaps; functional-group composition maps; bryophyte distribution layers.

- Implications for GIS-enabled data products
  - Create clear, map-based visualisations of treatment effects on productivity, soil conditions, and plant community structure.
  - Enable end users (policy colleagues, clients, public) to explore how management actions (mowing, fertilisation, insecticide) influence habitat quality, biodiversity, and functional traits in a grassland system.
  - Support time-series analyses and scenario planning by integrating biomass, soil chemistry, and diversity metrics into interactive GIS dashboards.