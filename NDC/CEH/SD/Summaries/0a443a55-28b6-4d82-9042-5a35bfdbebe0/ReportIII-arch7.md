# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- The NERC Soil Biodiversity Thematic Programme study site at Sourhope (Scottish Borders) was monitored intensively to provide context for group-specific work. The report summarizes automatic weather data, above-ground biomass, soil pH, and botanical composition across 1999–2001, with attention to how site management events and treatment differences shape results.
- Experimental design and management are described in baseline documentation (Baseline Data Survey, 1998). The 2001 period experienced government-made restrictions due to Foot and Mouth Disease (Feb–May), with ongoing management and a change in the site officer.

## Key Results

- Automatic Weather Station (2.1)
  - 2001 weather showed near-average rainfall after a very wet previous year; radiation similar to long-term values; average temperatures slightly lower; soil moisture modestly higher than prior years.

- Above-ground biomass (2.2)
  - Clear hierarchy of treatment effects on biomass; peak growth in July/August each year.
  - 2001 biomass higher than 1999–2000, likely due to staff changes and shift from manual cutting to mechanical shears.
  - When normalised to the C1 treatment, nitrogen and/or lime generally boosted productivity; nitrogen plus lime yielded the strongest biomass increases.
  - ANOVA on ln-transformed biomass indicates significant differences between improved (N and/or L) vs. non-improved plots and a significant year-by-treatment interaction; no significant block effects.

- Soil pH (2.3)
  - Liming continued to raise pH: ~6.19 in limed plots and ~6.38 in nitrogen-plus-lime plots (October 2001) versus baseline measures from 1998.
  - Nitrogen addition alone raised pH too, but to a lesser extent; control plots remained largely unchanged.

- Botanical composition (2.4)
  - July 2001 Point Analysis mirrored July 2000 in methodology; surveyors showed no significant difference in results.
  - Total hits in 2001 rose 58% compared with 2000, suggesting denser sward (potentially from grazing removal in 1998).
  - Treatment-related shifts in species abundance:
    - Agrostis capillaris declined across all treatments in 2001, remaining dominant only in Control and Limed plots.
    - Festuca spp. (ovina and rubra) increased across all treatments, notably in fertilised plots (Festuca rubra with N or N&L; Festuca ovina with N).
    - Species associated with improved pastures (Festuca rubra, Poa pratensis) became more common in fertilised plots; less fertile-associated species (Anthoxanthum odoratum, Nardus stricta) were more common in unimproved plots.
  - Diversity: 24 species in unimproved treatments vs. 18 in Nitrogen & Lime plots, suggesting potential early diversity decline in more intensified plots.
  - PCA of point quadrat data largely separated nitrogen- and/or lime-treated plots from control/biocide plots; litter frequency increased in plots with nitrogen and/or lime, indicating faster turnover with higher soil fertility.
  - Biomass vs. species abundance: Festuca rubra and Poa pratensis positively correlated with biomass; Anthoxanthum odoratum, Nardus stricta, bryophytes (e.g., Rhytidiadelphus squarrosus) declined as biomass rose.

## Site Heterogeneity

- Variation in surface soil pH and plant communities
  - Columns E and F showed comparatively more acidic plots, potentially due to underlying spatial heterogeneity and treatment composition (many Controls or Biocide in those columns).

- Variation in vegetation biomass
  - Some plots consistently outliers with the lowest biomass; central plots tended to have higher biomass (e.g., Nitrogen+Lime 2E; Lime 2C; Biocide 2D; Control 1 2B).
  - Strong positive correlation between surface soil pH and biomass; no significant differences across blocks.

## Data Collection and Methods (context for GIS use)

- Main data collection and schedule
  - Measurements included 0–5 cm soil sampling, above-ground biomass harvesting at five summer cuts, Point Quadrat surveys with a 100-cell grid, and targeted vegetation surveys around mini-rhizotron tubes.
  - Weather data were from a site Automatic Weather Station (downloaded regularly).

- Analytical approaches
  - Biomass analyses used ANOVA on ln-transformed sums with block, plot, treatment, and year factors; (significant) treatment effects and year-by-treatment interactions reported.
  - Botanical composition analyzed via Point Quadrat surveys; species relative abundance tracked by hits per species per treatment; PCA used to explore community shifts.
  - Biomass-versus-species relationships and litter incidence were examined (e.g., correlations with biomass and treatment effects).

## Implications for GIS and Data Products

- The study provides spatially structured, plot-level time-series data across multiple response variables (biomass, pH, species composition, weather) with explicit treatments and management history, suitable for map-based visualization and spatial analysis.
- Key GIS-ready insights:
  - Treatment effects and year-to-year changes can be visualized via thematic maps showing biomass density, pH changes, and species shifts across plots.
  - Site heterogeneity and spatial clustering (e.g., central vs. edge plots; Columns E/F acidity) can be explored through spatial autocorrelation or hotspot mapping.
  - PCA results offer a basis for mapping plots by “biotic state” (e.g., nutrient-limited vs. fertilised profiles) to compare with pH and biomass maps.
- Considerations for data curation
  - Ensure consistent data standards across years (treatment codes, plot identifiers, species codes).
  - Maintain metadata on management events (FMD period, officer change) that influenced sampling and processing.
  - Preserve measurement protocols (e.g., Point Quadrat methodology, mowing schedules) to support reproducibility and cross-year comparisons.