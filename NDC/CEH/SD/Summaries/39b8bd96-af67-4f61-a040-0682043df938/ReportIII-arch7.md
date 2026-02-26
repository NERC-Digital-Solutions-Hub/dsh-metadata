# RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- Location and scope: Field experiment at Sourhope Farm, Macaulay Institute, part of the NERC Soil Biodiversity Thematic Programme; aims to provide context for detailed studies and enable cross-year comparisons.
- Experimental design: Plot-level treatments including Control, Nitrogen, Lime, Nitrogen & Lime, and Biocide; regular monitoring of above-ground biomass, soil pH (0–5 cm), and botanical composition via point quadrats; weather data from an automatic weather station.
- Data collection and management: Measurements and sampling coordinated with end-user groups; 1999–2001 data collection schedule described (mowing, biomass harvesting, botanical surveys, soil sampling, and related activities). 2001 impacted by Foot and Mouth Disease restrictions and a change in site management personnel.
- Data notes for GIS use: Data cover spatial plots across the Sourhope site with repeated measures over three years; includes biomass (annual and per-cut), soil pH (top 5 cm), and species abundance from point quadrats; weather variables available; unit codes and species codes provided to support geospatial interpretation.

## Introduction (context and aims)

- Full site description and experimental rationale available in Baseline Data Survey (Nov 1998).
- The report provides a broad monitoring framework to contextualize groups’ detailed studies and facilitate year-to-year comparisons.
- Management changes in 2001: FMD-related access restrictions and a change in site Officer in Charge.

## Results

- 2.1 Automatic Weather Station
  - 2001 weather was generally unremarkable; rainfall near long-term average; radiation similar to prior years; slightly lower average temperatures; higher soil moisture than earlier years.

- 2.2 Above-ground biomass
  - Clear hierarchy of biomass across treatments; peak biomass typically in July/August.
  - 2001 biomass higher than previous years, likely due to personnel changes and switch from manual to mechanical cutting.
  - When normalised to the Control 1 (C1), nitrogen and lime (and their combination) show strongest positive effects on productivity.
  - ANOVA indicates significant differences between improved (N and/or L) vs non-improved plots; year-by-treatment interaction significant; no significant block effects.

- 2.3 Soil pH
  - Lime raises topsoil pH; October 2001 pH: limed plots ~6.19; nitrogen + lime plots ~6.38.
  - Nitrogen alone also raises pH but less strongly.
  - Control plots show no significant pH change since baseline (August 1998).

- 2.4 Botanical composition
  - July 2001 Point Quadrat survey replicated July 2000 protocol; high inter-observer consistency.
  - Overall hits in 2001 were 58% higher than 2000, suggesting increased sward density (likely from grazing removal in 1998).
  - Treatment differences: Festuca rubra and Poa pratensis increase in fertilised/improved plots; Agrostis capillaris declines across most treatments.
  - Diversity: unimproved plots show 24 species; nitrogen and lime plots show fewer (18), hinting at reduced diversity with higher fertility.
  - Multivariate analysis (PCA) separates improved plots (N and/or L) from unimproved plots; biomass correlates positively with Festuca rubra and Poa pratensis abundance; higher biomass linked with increased litter and faster vegetation turnover.

## Site Heterogeneity

- 3.1 Variation in surface soil pH and plant community composition
  - Spatial heterogeneity observed; columns E and F show more acidic plots, particularly in nitrogen- and/or lime-treated columns, suggesting slope-area spatial effects.

- 3.2 Variation in vegetation biomass
  - Outliers with low biomass scattered across treatments; higher biomass tends to occur on central plots.
  - Strong positive correlation between surface soil pH and biomass.
  - No significant differences in biomass between blocks.

## Data and Methods relevant for GIS (for map-based data products)

- Plot-level data: Biomass (summer harvest totals and cumulative 1999–2001), treatment type, and plot coordinates for geospatial mapping; log-transformed biomass used for ANOVA.
- Soil data: Topsoil pH (0–5 cm) measured October 2001 (baseline August 1998 for comparison); lime and nitrogen effects on pH documented.
- Vegetation data: Point Quadrat survey results (July 2001) with species-level hits per plot; principal components analysis to illustrate community shifts; species codes provided for mapping of community composition.
- Weather data: Annual measures from Sourhope Automatic Weather Station (rainfall, radiation, temperature, soil moisture) for context in spatial analyses.
- Spatial heterogeneity: Page highlights slope-associated differences and columnar variation; maps can depict pH, biomass, and dominant species to illustrate heterogeneity.

## Considerations for GIS-based interpretation

- Data quality and comparability: 2001 fieldwork affected by FMD restrictions and staffing changes; interpretation should account for potential sampling and measurement discontinuities.
- Resolution and scale: Plot-level data are suitable for local-scale analyses; cross-year comparisons require normalization (e.g., biomass relative to C1) and careful alignment of sampling dates.
- Data integration: Combine biomass, pH, and species composition with weather data to assess spatial-temporal drivers of vegetation responses.
- Interpretive outputs: Potential map layers include biomass by plot and year, topsoil pH by plot, dominant species per plot, and PCA-derived community shift indicators.

## Site heterogeneity synthesis (implications for mapping)

- Spatial structure (slope-facing columns) influences both pH and biomass, with central plots showing higher biomass and certain pH patterns, implying the need to include environmental context in GIS analyses (e.g., slope, column design).

## Acknowledgements

- Recognition of individuals and staff contributions to data collection and site management.