# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- Intensive field study at Sourhope, Scottish Borders as part of the NERC Soil Biodiversity Thematic Programme.
- Aimed to contextualize detailed studies with broad monitoring across weather, biomass, soil pH, and botanical composition.
- 2001 management and external events (FMD restrictions and staff change) affected site operations but core measurements continued per the 2001 Site Management Plan.

## Datasets and Measurements
- Automatic Weather Station: headline measures (rainfall, radiation, temperatures, soil moisture) for 1999–2001.
- Above-ground biomass: biomass estimates by treatment throughout the summer, with peak production in July/August; 2001 biomass higher than previous years.
- Soil pH: upper 5 cm pH measured in baseline (1998) and October 2001; lime and nitrogen-plus-lime treatments increased pH.
- Botanical composition: Point Quadrat surveys (July 2001) with species hits; 24 species in unimproved plots vs 18 in improved plots; changes in relative abundances by species; PCA analysis to explore treatment associations.
- Site activity data: schedule of soil sampling, measurements, and mowing events; detailed methods for biomass sampling (0.5 m2 quadrats, mowing, drying, and weighing).

## Experimental Design and Site Characteristics
- Location: Sourhope Farm, MLURI; field experiment with plots organized into columns and blocks, under treatments including Control, Nitrogen, Lime, Nitrogen & Lime, and Biocide.
- Treatments: Nutrient additions (N, Lime), combination (N&L), and Biocide; clear hierarchy in biomass response (N and/or Lime > control/biocide).
- Site heterogeneity: spatial variation across the slope; columns E and F exhibited more acidic plots, contributing to pH heterogeneity.
- Data handling: biomass analyses ln-transformed; ANOVA used to assess treatment effects; PCA used to explore species composition shifts.

## Key Results

### 2.1 Automatic Weather Station
- 2001 rainfall near long-term average; radiation similar to prior years; average temperatures slightly lower; soil moisture modestly higher than previous years.

### 2.2 Above-ground Biomass
- Clear treatment hierarchy: inputs of nitrogen and/or lime increased biomass; peak production still in mid/late summer (July–August).
- 2001 biomass higher than 1999–2000, likely due to personnel changes and switch from manual cutting to mechanical shears.
- After normalization to C1, nitrogen and/or lime plots continued to show positive productivity; significant differences between improved vs non-improved plots; significant year-by-treatment interaction; no significant block effects.

### 2.3 Soil pH
- Lime raised topsoil pH; October 2001 averages: limed plots ~6.19; nitrogen+lime plots ~6.38.
- Nitrogen alone also increased pH but to a lesser extent.
- Control plots remained near baseline pH since August 1998.

### 2.4 Botanical Composition
- July 2001 point-quadrat survey replicated previous methodology; no significant difference between surveyors.
- Total hits were 58% higher in 2001 vs 2000, suggesting increased sward density, possibly from grazing stock removal in 1998.
- Species shifts by treatment:
  - Agrostis capillaris declined across all treatments in 2001.
  - Festuca spp. increased across treatments; F. rubra especially prominent in N and N&L plots.
  - Fertilized plots (especially N+L) showed more Festuca rubra and associated species (e.g., Poa pratensis).
  - Less fertile-associated species (Anthoxanthum odoratum, Nardus stricta) more common in unimproved plots.
- Species richness: 24 species in unimproved treatments vs 18 in N&L plots, indicating possible early decline in diversity with improved plots.
- PCA indicates clear separation of improved (N and/or Lime) vs unimproved (Control/Biocide) plots; dominant species linked to improved plots (e.g., Festuca rubra, Poa pratensis) vs unimproved plots with bryophytes and Acidic-preferring species.
- Biomass correlation: higher biomass plots correlated with increased abundance of Festuca rubra and Poa pratensis; lower abundance of Anthoxanthum odoratum, Nardus stricta, bryophytes with higher biomass.
- Litter and vegetation turnover increased in plots receiving nitrogen and/or lime.

## Site Heterogeneity

### 3.1 Variation in Surface Soil pH and Plant Community
- Spatial heterogeneity present; columns E/F showed more acidic conditions, intensifying differences in N and/or Lime plots within these columns.
- Heterogeneity supported by visual/quantitative separation in PCA and pH maps.

### 3.2 Variation in Vegetation Biomass
- Outlier plots with low biomass across treatments tended to cluster in less central areas; higher biomass generally in more central plots (e.g., N+L in 2E, Lime in 2C, Biocide in 2D, Control 1 in 2B).
- Positive pH–biomass relationship overall; no significant block-level differences in biomass.

## GIS-Relevant Insights and Data Products

- Spatially explicit datasets at plot level (plot_id, column, block, treatment, year) with:
  - Biomass data: seasonal sums and annual totals; normalized values relative to C1.
  - Soil pH: upper 5 cm pH (baseline vs 2001).
  - Botanical composition: species hits per plot, major species abundances, diversity indicators.
  - Weather context: annual rainfall, radiation, temperature, soil moisture.
- Potential map products:
  - Biomass heatmaps by plot for 1999–2001 and cumulative biomass.
  - pH gradient maps by plot and by column, highlighting lime and nitrogen effects.
  - Species distribution maps showing dominant species per plot and changes from 2000 to 2001.
  - Difference maps illustrating treatment effects (improved vs unimproved) on biomass and species composition.
  - Spatial correlation maps (pH vs biomass) and overlay with site heterogeneity (columns, slope orientation).
- Temporal layers:
  - Yearly snapshots (1999, 2000, 2001) and cumulative measures; note 2001 events (FMD restrictions, staff changes) as metadata.
- Data integration opportunities:
  - Link plot-level GIS data with field management events (lime application dates, nitrogen applications, mowing schedules) to explain temporal variations.
  - Incorporate the Automatic Weather Station series as a basemap for environmental context.
- Analytical products:
  - PCA/biplot overlays on maps to show how species assemblages align with treatments spatially.
  - Regression surfaces for biomass against pH and other covariates to identify hotspot drivers.

## Data Quality, Methodology and Notes
- Biomass measurements were taken with mowing across five summer cuts per year; values were ln-transformed for ANOVA.
- Point Quadrat botanical surveys used standardized 25-cell sampling within 0.5 m2 subplots; cross-survey consistency tested with Genstat.
- Normalization against the C1 control helped isolate treatment effects across years with changing personnel/mowing methods.
- Spatial analysis recognizes ongoing site heterogeneity and potential slope-related effects, particularly in columns E and F.

## Implications for Future GIS Work
- Ensure consistent plot ID mapping across years and treatments to enable robust time-series analyses.
- Maintain metadata on field operations (mowing method, personnel) to interpret year-to-year biomass variations.
- Develop standardized GIS schemas for integrating multiple data types (biomass, pH, species, weather) into a cohesive Sourhope field data model.
- Leverage spatial statistics to quantify and visualize the influence of site heterogeneity on treatment outcomes.