# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- NERC Soil Biodiversity Thematic Programme field experiment at Sourhope Farm (Scottish Borders) to provide context for biodiversity studies and data integration across multiple disciplines.
- Yearly data streams include: automatic weather data, above-ground biomass, soil pH, and botanical composition from plot-based surveys.
- Experimental design features main plots with sub-plots across blocks and treatments: Control, Nitrogen, Lime, Nitrogen & Lime, and Biocide; assessments include biomass harvesting, pH measurements, and Point Quadrat botanical surveys.
- 2001 site operations affected by Foot and Mouth Disease restrictions and a change of site officer, but core activities (liming, N application, pH measurements, biomass collection, vegetation cutting) proceeded per plan.

## Key Results by Topic

### 2.1 Automatic Weather Station
- 2001 weather metrics generally unremarkable.
- Rainfall near long-term average; radiation stable; average temperatures slightly lower; soil moisture modestly higher than previous year.

### 2.2 Above-ground biomass
- Clear hierarchical biomass response: some plots consistently higher biomass, especially with nitrogen and/or lime.
- 2001 biomass markedly higher than prior years, likely due to staff change and shift from manual cutting to mechanical shears.
- When biomass is normalised to the Control (C1) year-to-year, nitrogen and/or lime show the strongest positive effects on productivity.
- Statistical results: significant differences between improved (N and/or L) vs non-improved plots; significant year-by-treatment interaction; no significant block effect.

### 2.3 Soil pH
- Lime application raised surface soil pH (0–5 cm) to about 6.19 in limed plots and 6.38 in Nitrogen & Lime plots.
- Nitrogen addition alone also increased pH, but to a lesser extent.
- Control plots remained close to baseline pH (measured August 1998).

### 2.4 Botanical composition
- July 2001 Point Quadrat survey: higher total hits in 2001 (58% more than 2000), suggesting denser sward after reduced grazing since 1998.
- Species-level shifts by treatment:
  - Agrostis capillaris declined across treatments (dominant in 2000, remaining only in some controls).
  - Festuca species (ovina and rubra) increased across treatments; strong association with fertilised plots, especially those with nitrogen and/or lime.
  - Improved plots (N, L, or N&L) show more Poa pratensis, Festuca rubra, Poa trivialis; unimproved plots retain species typical of poorer pastures (e.g., Agrostis vinealis, Nardus stricta).
- Diversity: unimproved plots harboured 24 species; the Nitrogen & Lime plots had 18 species, suggesting potential decline in diversity with improved fertility.
- Multivariate pattern (PCA): nitrogen- and/or lime-treated plots cluster separately from control/biocide plots; unimproved plots tied to bryophytes and low-diversity assemblages.
- Biomass vs species abundance: Festuca rubra and Poa pratensis abundance positively correlated with biomass; Anthoxanthum odoratum, Nardus stricta, bryophytes tend to decline as biomass rises.
- Litter presence increases in plots receiving nitrogen and/or lime, indicating faster vegetation turnover with higher fertility.

## Site Heterogeneity

### 3.1 Variation in surface soil pH and plant community composition
- Spatial heterogeneity observed: columns E and F (sloping right/up-slope) show comparatively more acidic plots.
- Underlying heterogeneity linked to a higher incidence of low pH in nitrogen- and/or lime-improved plots within these columns.

### 3.2 Variation in vegetation Biomass
- Biomass values vary across plots; several outliers show the lowest biomass, while central plots tend to have higher biomass (e.g., N&L plots 2E, Lime 2C, Biocide 2D, Control 1 2B).
- Positive relationship between surface soil pH and biomass.
- No significant biomass difference detected among blocks (statistically non-significant).

## Data and GIS-Ready Insights

- GIS-ready layers implied by the study:
  - Plot-level biomass by year (1999–2001) with subplots (S, T, U, V) per plot.
  - Plot-level soil pH at surface (0–5 cm) and changes over time (baseline 1998 vs Oct 2001).
  - Botanical composition: relative abundance (hits) per species per plot by year, including major indicator species (e.g., Festuca rubra, Poa pratensis, Agrostis capillaris).
  - Treatment layer (N, L, N&L, Biocide, Control) to map management regime.
  - Spatial heterogeneity indicators: column-based spatial grouping and central vs edge plot location.
  - Weather-derived layers: annual rainfall, radiation, and soil moisture as context layers.
- Practical GIS use:
  - Create thematic maps of biomass by plot-year, pH by plot, and dominant species distribution per treatment.
  - Develop change-detection visuals showing 1999→2001 trends in biomass, pH, and community composition.
  - Overlay management treatments with biomass and pH to assess treatment efficacy spatially.
  - Explore correlations: biomass vs pH, biomass vs key species abundance.

## Considerations and Context

- 2001 operational disruptions due to FMD; field sampling largely resumed under controlled protocols.
- A shift in personnel and mowing method (manual -> mechanical) likely influenced biomass measurements in 2001.
- Spatial heterogeneity is an important driver of observed patterns; landscape-scale interpretation should account for column and central-peripheral effects.

## Takeaways for Map-Based Data Products

- Plot- and sub-plot–level datasets tie directly to map layers for biomass, pH, and species composition, enabling spatial analyses of treatment effects and site variability.
- Temporal dimension (1999–2001) supports animated or stepped maps showing how fertility treatments alter biomass and community structure over time.
- Strong links between soil fertility (N, Lime) and vegetation outcomes (biomass, species shifts) support thematic layers indicating fertility status and ecological succession indicators.