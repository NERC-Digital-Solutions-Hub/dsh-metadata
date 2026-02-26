# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- An in-depth field experiment at Sourhope Farm (Scottish Borders) under the NERC Soil Biodiversity Thematic Programme, documenting 1999–2001 measurements to help relate broad datasets to site context and enable year-to-year comparisons.

## Overview of what the study covers
- Monitored automatic weather, above-ground biomass, soil pH, and botanical composition across a structured field layout with multiple treatments.
- Aimed to identify links between soil chemistry, vegetation, and management practices, and to characterize spatial heterogeneity across the site.
- Included data management and methodological notes relevant for GIS-based data integration and visualization.

## Datasets and Measurements

- 2.1 Automatic Weather Station
  - 2001 weather data generally near long-term averages after exceptionally wet preceding year.
  - 2001: rainfall ~839 mm; radiation ~3473 MJ m-2; average soil moisture 0.37 m3 m-3; average air temperatures around 7–7.7°C at 2 m depth.

- 2.2 Above-ground Biomass
  - Biomass showed a consistent treatment hierarchy, with peak summer production in July–August.
  - 2001 saw a notable biomass increase vs. prior years, attributed to staff changes and switch from manual cutting to mechanical shears.
  - Nitrogen and Lime (N & L) treatments most strongly promoted biomass; ANOVA: significant differences between improved (N and/or L) vs. unimproved plots; significant year × treatment interaction; no significant block effects.
  - Biomass values were standardized by normalizing to a common reference plot (C1) to assess treatment effects over time.

- 2.3 Soil pH
  - Liming raised topsoil pH consistently; October 2001 averages: limed plots 6.19, N&L plots 6.38.
  - Nitrogen alone also increased pH but to a lesser extent; control plots showed little change since baseline (1998).

- 2.4 Botanical Composition
  - Point Quadrat surveys (July 2001) compared with July 2000; no significant inter-surveyor difference.
  - Increased total hits in 2001 (58% higher than 2000), suggesting greater sward density, possibly from reduced grazing since 1998.
  - Species shifts by treatment:
    - Agrostis capillaris declined across all treatments in 2001; most abundant in Control1 and Limed plots.
    - Festuca species and Poa pratensis increased in fertilized plots; particularly Festuca rubra in Nitrogen and Lime plots.
    - Species associated with improved pastures (Festuca rubra, Poa pratensis) were more common in fertilized plots; N/L plots carried the greatest shift.
  - Biodiversity: unimproved treatments (Control and Biocide) contained 24 species, while improved (N and/or L) plots had 18 species, suggesting a potential decline in diversity with fertility improvements.
  - Principal Components Analysis (PCA) largely separated nitrogen and/or lime plots from control/biocide plots; improved plots plotted at the extremes with higher Festuca rubra presence and lower bryophyte/Agrostis predominance.
  - Correlations between species abundance and biomass:
    - Festuca rubra and Poa pratensis positively correlated with biomass.
    - Anthoxanthum odoratum, Nardus stricta, bryophytes (Rhytidiadelphus squarrosus) tended to decrease as biomass increased.
  - Increased litter presence in N and/or Lime plots linked to faster vegetation turnover with higher soil fertility.

## Spatial Structure and Site Heterogeneity

- 3.1 Variation in surface soil pH and plant community composition
  - Spatial heterogeneity: columns E and F showed comparatively more acidic plots than columns on the left, with an apparent trend influenced by plot type distribution (more Controls or Biocide plots in those columns).

- 3.2 Variation in vegetation Biomass
  - Biomass values varied across plots, with outliers typically corresponding to plots at the site periphery or extremes of the design.
  - Central plots tended to have higher biomass (e.g., Nitrogen and Lime plot 2E; Lime plot 2C; Biocide plot 2D; Control 1 plot 2B).
  - Strong positive correlation observed between surface soil pH and biomass.

## Temporal and Treatment Insights

- Biomass response patterns:
  - All treatments peaked in biomass in mid to late summer, with a notable 2001 increase across treatments.
  - Nitrogen and Lime together yielded the strongest biomass response, followed by individual N or Lime effects.

- Species and diversity trends:
  - Fertilized plots favored species associated with improved pastures (Festuca rubra, Poa pratensis).
  - Unimproved plots retained higher relative abundances of nutrient-poor pasture species (Agrostis capillaris; Nardus stricta) and bryophytes.

- Data patterns across years:
  - Inter-year ANOVA showed significant treatment effects and year × treatment interactions for biomass, indicating changing treatment impacts across years.
  - PCA highlighted divergence between improved vs unimproved plots in species composition, with biomass increases aligning with shifts toward grasses typical of fertilized systems.

## Data Analysis Approaches

- Split-plot ANOVA for annual biomass assessments (1999, 2000, 2001).
- Inter-year ANOVA to examine treatment-by-year effects (1999–2000; 1999–2001).
- Principal Components Analysis (Genstat) on the July 2001 point quadrat data to explore dominant species associations and treatment effects.
- Species abundance analysis via “hits” per species per treatment, enabling cross-year and cross-treatment comparisons.

## Implications for GIS and Data Products

- Potential GIS layers and analyses
  - Plot-level biomass maps by year (1999–2001) with blocks and sub-plots (S, T, U, V) to capture within-plot variability.
  - Soil pH maps by plot and depth (top 5 cm), including 1998 baseline vs. 2001 measurements, to visualize liming effects and pH-biomass relationships.
  - Species distribution maps derived from point-quadrat hits, showing treatment-associated community shifts (e.g., Festuca rubra, Poa pratensis, Agrostis capillaris) and biodiversity changes.
  - Spatial heterogeneity indicators, such as columns E/F vs other columns, to identify consistent spatial patterns across years.
  - Biomass vs. soil pH correlation layers to identify high-biomass areas associated with higher pH.
  - PCA-derived teamable layers (e.g., axis scores by plot) to summarize community composition gradients for map visualisation.

- Practical considerations for GIS
  - Use consistent plot, subplot, and block identifiers to join multiple data streams (biomass, pH, species hits, weather proxies).
  - Account for documented site heterogeneity (columns and slope orientation) when scaling up to landscape-level interpretations.
  - Consider temporal alignment (mid-summer biomass vs. July survey data) for accurate cross-year comparisons.
  - Acknowledge data provenance changes (staff changes, mowing method shift, FMD-access restrictions) when assessing year-to-year variability.

## Contextual notes and limitations

- Foot and Mouth Disease (FMD) restrictions in 2001 reduced site access and visitor numbers, though field measurements and sampling continued following an approved protocol.
- Staffing change occurred in 2001, potentially contributing to observed differences in biomass measurements.
- A shift from manual mowing to mechanical shears in 2001 likely influenced biomass estimates.
- Measurements rely on plot-based sampling with limited replication at the micro-plot level, but with five blocks and multiple sub-plots per plot, enabling robust within-site comparisons.

## Key Takeaways for GIS Specialists

- The Sourhope dataset provides a rich, geo-referenced basis for visualizing how soil chemistry (pH) and management practices (N, Lime, N+L, Biocide) influence biomass production and plant community structure across a heterogeneous field site.
- Strong spatial patterns emerge: central, higher-pH plots tend to yield higher biomass; fertilized plots shift communities toward grasses typical of improved pastures.
- Biodiversity metrics change with fertility, indicating potential trade-offs between productivity and species richness that can be mapped and analyzed over time.
- The combination of biomass, pH, and species composition data across years offers opportunities to create multi-layer GIS products (temporal maps, correlation surfaces, and PCA gradient maps) for policy, land management, or public-facing information.