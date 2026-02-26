# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- Location: Sourhope Farm, Macaulay Institute, Scottish Borders, UK; field experiment under the NERC Soil Biodiversity Thematic Programme.
- Purpose: Intensive monitoring to contextualize detailed studies; baseline data collected in 1998.
- Timeframe: 1999–2001 (with management events in 2001); key disruption: Foot and Mouth Disease restrictions Feb–May 2001.
- Treatments: Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, and Biocide; plots arranged in a block/plot design with sub-plots (S, T, U, V) within each plot.
- Data types: Automatic weather data, above-ground biomass, soil pH, botanical (point quadrat) composition, and site heterogeneity (spatial variation across columns and along slope).

## Experimental design and data collection
- Measurements collected annually or seasonally (as per Table 1 in the report) and linked to a baseline 1998 dataset.
- Methods:
  - Above-ground biomass: five summer cuts per year on 0.5 m2 sub-plots; biomass summed yearly; results ln-transformed for analysis.
  - Soil pH: measured in the top 5 cm; lime increases pH; nitrogen also raises pH modestly; controls near baseline.
  - Botanical composition: Point Quadrat surveys in July (2000 and 2001); species hits per treatment; PCA used to explore community shifts.
  - Weather: Automated weather station on site; rainfall, radiation, temperature, and soil moisture tracked.
- Data management notes: 2001 changes in staffing and mowing method (manual vs mechanical) affected biomass readings; ANOVA accounts for year and treatment interactions; blocks showed no significant effect on biomass.

## Key results

### 2.1 Automatic Weather Station
- 2001 rainfall near long-term average; radiation stable; average temperatures slightly cooler; soil moisture modestly higher than prior years.

### 2.2 Above-ground biomass
- Clear hierarchy among treatments throughout the sampling period; peak biomass typically in July/August.
- 2001 biomass substantially higher than 2000, partly due to methodological change (mechanical shears) and personnel shift.
- Normalizing to C1 shows sustained positive response to nitrogen and/or lime, with the Nitrogen & Lime treatment often most effective.
- ANOVA findings:
  - Significant differences between improved (N and/or L) vs unimproved plots.
  - Significant interaction between treatment and year; no significant block effect.

### 2.3 Soil pH
- Lime additions continued to raise surface soil pH.
  - Limed plots: ~6.19 (Oct 2001)
  - Nitrogen & Lime plots: ~6.38 (Oct 2001)
  - Nitrogen alone: modest pH increase
- Control plots remained close to baseline August 1998 measurements.
  
### 2.4 Botanical composition
- July 2001 point-quadrat surveys showed higher total hits (density) than 2000 across treatments.
- Survey consistency: no significant difference between surveyors.
- Species shifts by treatment (relative abundance):
  - Agrostis capillaris declined across treatments in 2001; Festuca spp. increased and were most common in fertilized plots.
  - Improved plots (N and/or L) favored Festuca rubra, Poa pratensis, Poa trivialis, and Holcus species; unimproved plots retained species associated with poorer pastures (e.g., Anthoxanthum odoratum, Nardus stricta).
- Diversity:
  - 24 species in unimproved treatments (Control and Biocide) vs 18 species in Nitrogen & Lime plots; potential early decline in diversity with strong fertility improvements.
- Multivariate analysis:
  - Principal Components Analysis (PCA) largely separates nitrogen- and/or lime-treated plots from controls/biocide.
  - Biomass correlations: Festuca rubra and Poa pratensis positively correlated with biomass; Anthoxanthum odoratum, Nardus stricta, bryophytes decline as biomass increases.
  - Increased litter in N and/or Lime plots indicates faster vegetation turnover with higher soil fertility.

## Site heterogeneity and spatial patterns
- Spatial variation:
  - Columns E and F displayed more acidic conditions than columns on the left; underlying heterogeneity interacts with treatment placement.
  - Central plots tended to have higher biomass (e.g., Nitrogen & Lime plots 2E; Lime plot 2C; Biocide plot 2D; Control 1 plot 2B).
- Biomass and pH relationship:
  - Strong positive correlation between surface soil pH and biomass.
  - No significant differences in biomass between blocks (i.e., block-level spatial replication appeared robust).

## Implications for GIS and data products
- The dataset is well-suited for GIS-based map products and spatial analyses:
  - Plot-level maps of biomass, pH, and key species abundances by treatment.
  - Thematic maps showing treatment effects (N, Lime, N&L, Biocide) versus controls.
  - Spatial heterogeneity analyses across site columns, slope orientation, and central vs edge plots.
  - Temporal layers for 1999–2001 to visualize year-to-year changes and treatment interactions.
  - Integration with weather layers to explore relationships between rainfall/soil moisture and biomass or pH dynamics.
  - PCA/ordination results can be represented geospatially (e.g., overlaying principal component scores or species loadings on site maps).

## Considerations and caveats
- The 2001 shift to mechanical mowing and changes in personnel likely influenced biomass measurements; interpretation should consider method consistency.
- PCA emphasizes dominant species; rare taxa may be underrepresented in ordination results.
- Diversity trends suggest possible declines with higher fertilization (N and L), but sampling effort and year effects should be considered in GIS-derived analyses.

## Takeaways for GIS specialists
- The Sourhope field data provide a rich, spatially structured, multi-parameter dataset ideal for creating interactive map-based data products.
- Useful GIS deliverables include: biomass and pH rasters or polygon maps by plot, species distribution layers by treatment, temporal change visualizations (1999–2001), and spatial correlation analyses (pH vs biomass, central vs peripheral biomass patterns).
- The integration of climate/soil data with plant community and productivity data supports contextual, policy-relevant map visualizations and stakeholder-facing dashboards.