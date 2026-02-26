# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- Location: Sourhope field experiment, Macaulay Land Use Research Institute, Sourhope Farm, Scottish Borders, UK.
- Context: Part of the NERC Soil Biodiversity Thematic Programme; aims to monitor a large field experiment to contextualise detailed studies and enable cross-year comparisons.
- Design highlights: Treatments include Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, and Biocide; measurements span above-ground biomass, soil pH, botanical composition, and weather data across 1999–2001; layout consists of plots within blocks, enabling assessment of spatial/site variability.

## Data Collected and Methods (1999–2001)

- Above-ground productivity: measured via five summer mowing events per year, with 0.5 m2 sub-plot sampling; dried biomass aggregated annually and ln-transformed for analysis.
- Soil pH: upper 5 cm measured for treatment effects; pH tracked against baseline (1998) and over time.
- Botanical composition: Point Quadrat surveys (July 2001) across plots; identification of dominant species and relative abundance (hits per species); cross-year comparison with 2000 data.
- Weather data: Automatic Weather Station on-site; records include rainfall, radiation, soil moisture, and air/soil temperatures.
- Site activity notes: 2001 events impacted by Foot and Mouth Disease controls (restricted site access Feb–May); one management role change (Officer in Charge).

## Key Findings by Data Type

### 2.1 Automatic Weather Station
- 2001 rainfall near long-term average; prior year wetter.
- Total radiation similar across years; slight overall cooling in 2001.
- Average soil moisture modestly higher in 2000–2001 than earlier years.
- On-site weather data provide context for biomass and growth patterns.

### 2.2 Above-ground Biomass
- Clear, consistent hierarchy of biomass across treatments; peak growth typically in July/August.
- 2001 biomass generally higher than 2000, likely due to personnel change and switch from manual cutting to mechanical shears.
- When normalized to C1, nitrogen and lime (N and/or L) largely drive biomass increases; Nitrogen & Lime often the most effective combination.
- ANOVA findings: significant differences between improved (N and/or L) vs non-improved plots; significant treatment × year interaction; no significant block effects.

### 2.3 Soil pH
- Liming raises surface soil pH: October 2001 measurements ~6.19 in limed plots and ~6.38 in Nitrogen & Lime plots.
- Nitrogen alone also raises soil pH, but to a lesser extent.
- Control plots show little change since August 1998 baseline.

### 2.4 Botanical Composition
- 2001 Point Quadrat survey: total hits 58% higher than 2000, suggesting denser sward (possible grazing stock removal effect in 1998).
- Treatment differences in dominant species:
  - Agrostis capillaris declines across all treatments in 2001.
  - Festuca spp. (ovina and rubra) increase across treatments; most frequent in N and Biocide, and N&L plots respectively.
  - Improved plots (N and/or Lime) show higher abundance of Festuca rubra and Poa pratensis; weed- and low-fertility associated species (Anthoxanthum odoratum, Nardus stricta) more common in unimproved plots.
- Diversity: unimproved plots show 24 species; nitrogen+lime plots show 18 species, suggesting diversity changes with fertility improvements.
- Multivariate analysis: PCA separates improved from unimproved plots; increased Fri–Po a pratensis and Festuca rubra association with biomass; higher litter incidence with nitrogen and/or lime, indicating faster turnover with increased fertility.

## Site Heterogeneity

- 3.1 Spatial variation in surface pH and plant communities: columns E and F show relatively more acidic plots; pH differences in nitrogen-and/or-lime plots may reflect underlying spatial heterogeneity.
- 3.2 Variation in vegetation biomass: outlier plots with low biomass exist across treatments, while central plots tend to have higher biomass (e.g., N&L 2E, Lime 2C, Biocide 2D, Control 1 2B).
- Positive correlation observed between surface soil pH and biomass; no significant differences between blocks in biomass, indicating strong within-site heterogeneity rather than block-level effects.

## Data and GIS-Oriented Implications

- Data products suitable for GIS:
  - Map of above-ground biomass by plot (1999–2001), with year-to-year change and treatment overlays.
  - Soil pH maps by plot, showing lime-treated vs untreated and interaction with nitrogen.
  - Species distribution rasters or polygon layers from Point Quadrat results, highlighting dominant species and shifts under different treatments.
  - Site heterogeneity layers capturing spatial patterns (columns, central vs edge plots) and their relation to pH and biomass.
  - Weather context layers (annual rainfall, soil moisture, radiation) to support interpretation of biomass and phenology.
- Considerations for visualization:
  - Normalize biomass by treatment baseline (e.g., C1) to compare across years with protocol changes.
  - Use PCA results to illustrate separation between improved and unimproved plots.
  - Include field management events (FMD restrictions, biocide application timing) as metadata affecting temporal comparisons.
- Data quality notes:
  - Inter-surveyor consistency confirmed for 2001 botanical data.
  - Missing events in 2001 (biocide timing) should be flagged when analyzing treatment effects.
  - Spatial heterogeneity should be incorporated into analyses to avoid misattributing location effects to treatment effects.

## Concluding Insight for GIS Practice

- The Sourhope experiment provides a rich, spatially explicit dataset linking management treatments to biomass production, soil chemistry (pH), and vegetation composition under varying weather conditions. For GIS-focused data products, prioritize spatially-resolved biomass, pH, and species distribution layers, annotated with treatment, year, block, and metadata on site events (e.g., FMD-related access restrictions) to support robust, map-based interpretation and cross-year comparisons.