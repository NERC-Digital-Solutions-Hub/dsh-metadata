# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- Large field experiment at Sourhope Farm (Scottish Borders) under the NERC Soil Biodiversity Thematic Programme.
- Aim: provide context and data for integrated analyses; support map-based data products and cross-study comparisons.
- Yearly monitoring across 1999–2001 to relate management treatments, soil properties, vegetation, and biomass.
- Management and staffing changes in 2001 affected operations; FMD restrictions limited site access Feb–May 2001.

## Key Datasets and Measurements
- Automatic Weather Station (1999–2001)
  - Headline measures: rainfall, radiation, temperatures, soil moisture.
  - 2001: rainfall near long-term average; slightly cooler mean temperatures; higher soil moisture than 2000.
- Above-ground Biomass (1999–2001)
  - Treatments: Control 1/2, Nitrogen, Lime, Nitrogen + Lime, Biocide, Nitrogen + Lime + Biocide, etc. (split-plot design across blocks and sub-plots S, T, U, V).
  - Peak biomass typically in July–August; 2001 biomass higher overall, likely due to personnel changes and switch from manual to mechanical cutting.
  - Normalisation against C1 to compare treatment effects across years.
  - ANOVA indicates significant biomass differences between improved (N and/or L) vs non-improved plots; year-treatment interaction significant.
- Soil pH (0–5 cm)
  - Liming raised pH; October 2001: limed plots ~6.19; N+L plots ~6.38; Nitrogen alone raised pH modestly; Controls unchanged from baseline (Aug 1998).
- Botanical composition (Point Quadrat Survey, July 2001)
  - 50%+ more survey effort in 2001; no significant inter-surveyor difference.
  - 2001 hits were 58% higher than 2000, suggesting increased sward density (likely from decreased grazing since 1998).
  - Species shifts by treatment:
    - Agrostis capillaris declined across most treatments; Festuca spp. and Poa pratensis increased, especially in fertilised plots.
    - Improved plots favored Festuca rubra, Poa pratensis, Poa trivialis; unimproved plots retained species associated with poorer pastures (Anthoxanthum odoratum, Nardus stricta).
  - Diversity: 24 species in unimproved plots vs 18 in Nitrogen + Lime plots (possible early diversity decline with higher fertility).
  - Multivariate analysis (PCA): improved plots (N and/or L) separate from control/biocide; biomass correlates positively with Festuca rubra and Poa pratensis, negatively with Anthoxanthum odoratum, Nardus stricta, bryophytes; increased litter with N and/or Lime indicating faster turnover.

## Site Heterogeneity and Spatial Patterning
- Spatial variation in pH and plant composition
  - Columns E and F showed comparatively more acidic plots, associated with left-vs-right slope orientation and plot composition (notably in N and/or Lime columns).
- Variation in vegetation biomass
  - Central plots tend to have higher cumulative biomass (e.g., Nitrogen + Lime, Lime, Biocide, Control 1 plot 2E/C2 etc.).
  - Strong positive correlation between surface soil pH and biomass observed (higher pH associated with higher biomass).
- No significant difference in biomass between blocks in the 2001 dataset, though notable outliers exist (low biomass in some designated plots).

## Data Collection Timeline and Methods
- Data collection activities span 1998–2001 with multiple measurements per year.
- Core protocols:
  - Above-ground biomass: five mowing occasions per summer; 0.5 m2 plots per sub-plot; drying and weighing of clippings; ln-transformed biomass for analyses.
  - Botanical surveys: Point Quadrat method (100 cells per grid, 25 pins per cell) conducted in July; species hits recorded per plot.
  - Mini-rhizotron-related vegetation surveys and disturbance/nutrient plots in selected subplots.
  - Automatic Weather Station data downloaded and centralized.
- Experimental design:
  - Blocked layout with multiple treatments (e.g., Control 1, Control 2, Nitrogen, Lime, Nitrogen + Lime, Biocide, etc.).
  - Sub-plots per plot designated as S, T, U, V for detailed sampling.

## Notable Findings and Interpretations
- Biomass response: nitrogen and lime inputs most effectively increased above-ground biomass; combined N + Lime produced the strongest response.
- pH and productivity: liming raises pH and is associated with higher biomass; higher biomass correlates with higher pH at the soil surface.
- Biodiversity and community shifts: fertilised/improved plots favor grassland-typical species (Festuca rubra, Poa pratensis); unimproved plots retain bryophyte-rich and nutrient-poor communities with higher relative abundance of Nardus stricta and Anthoxanthum odoratum.
- Density vs diversity: increased biomass in fertilised plots coincides with reduced species richness (fewer distinct species in highly fertilised plots).
- Temporal dynamics: 2001 showed notable changes in biomass and species composition relative to 2000, related to methodological changes and operating constraints.

## Data Quality and Considerations for GIS
- Operational changes in 2001 (staffing, switch to mechanical cutting) likely introduced a bias in biomass measurements.
- Foot-and-mouth disease restrictions reduced site access early in 2001, with limited sampling during that period.
- Data consistency: point quadrat results show treatment-driven patterns; cross-year comparisons require normalization and consideration of measurement protocol changes.
- Spatially explicit data: plots, blocks, and sub-plots provide a rich foundation for geospatial layering (treatments, biomass, pH, species composition) and time-series analysis.

## GIS and Map-Based Visualization Opportunities
- Spatial layers to create:
  - Treatment map: plot-level treatment assignment (Control, N, L, N+L, Biocide, etc.) across blocks.
  - Biomass surface: summer 2001 biomass values per plot/sub-plot; cumulative 1999–2001 biomass.
  - Soil pH map: surface pH (0–5 cm) by plot, with lime- and nitrogen-related shifts highlighted.
  - Species composition: relative abundance maps for key taxa (e.g., Festuca rubra, Poa pratensis, Agrostis capillaris) by plot, with PCA biplot overlays or heatmaps.
  - Heterogeneity indicators: columns or slopes with distinct pH and biomass patterns; correlation maps for pH–biomass relationships.
- Temporal analysis:
  - Time-series layers (1999–2001) for biomass and pH to visualize treatment effects and responses to management changes.
  - Change detection maps illustrating shifts in species composition between 2000 and 2001.
- Multivariate visualization:
  - PCA loadings by plot to identify driving species differences across treatments.
  - Scatter plots or dashboard views linking biomass to major species abundances and pH values.

## Appendix and Data References
- Tables and figures referenced:
  - Table 1: Data collection schedule (field measurements).
  - Table 2: 1998–2001 site activity timeline.
  - Table 3: Weather station headline measures for 1999–2001.
  - Tables 4–5: ANOVA results for biomass by year and across treatments; inter-year treatment effects.
  - Table 6: Rank abundance of species across 2000 and 2001 point quadrat surveys.
  - Figures: biomass trends, PCA outcomes, species-specific abundance, and soil pH relationships.

## Implications for GIS Specialists
- The Sourhope dataset provides a robust, spatially explicit, multi-year foundation to develop map-based data products that communicate treatment effects, soil chemistry shifts, and vegetation community responses.
- Useful for policy or outreach visuals, client dashboards, or public-facing geospatial storytelling around land-use experiments and soil biodiversity.
- When building GIS outputs, account for 2001 methodological and access changes as potential biases; use normalization and cross-year alignment to preserve comparability.