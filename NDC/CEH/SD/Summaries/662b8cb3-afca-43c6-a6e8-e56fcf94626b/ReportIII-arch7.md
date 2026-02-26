# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- The Sourhope field experiment at MLURI in the Scottish Borders provides a multi-year, plot-based data set on weather, biomass production, soil chemistry, and plant community composition under different nutrient and management treatments.
- The 2001 field season was affected by Foot and Mouth Disease restrictions, with adjusted access and sampling protocols, while core management activities (liming, nitrogen application, pH measurements, biomass collection, vegetation cutting, and point analysis) largely continued under a site-specific plan.
- Data are organized at the plot level (with blocks and treatment matrices) and include detailed botanical surveys (Point Quadrat method) and biomass measurements across multiple surveys in a growing season.

## Introduction (context and aims)

- The study forms part of the NERC Soil Biodiversity Thematic Programme, providing a broad context and year-to-year comparability for detailed groups.
- Baseline data and experimental design are described in the Baseline Data Survey (November 1998).
- Acknowledges changes in site management and personnel in 2001, and external disruption due to FMD restricting site access early in the year.

## Results

### 2.1 Automatic Weather Station
- 2001 weather data generally unremarkable: rainfall near long-term average after a very wet year previously; total radiation similar to prior years; average temperatures slightly lower; average soil moisture modestly higher than earlier years.

### 2.2 Above-ground biomass
- Clear hierarchy in biomass across treatments throughout the sampling period; peak biomass occurred in July or August each year.
- 2001 saw a substantial biomass increase relative to previous years, likely due to a combination of personnel changes and a shift from manual cutting to mechanical shears.
- When normalised to the control (C1), nitrogen and lime treatments produced the strongest biomass responses; nitrogen plus lime was particularly effective.
- Separate analyses (ANOVA on ln-transformed biomass) showed:
  - Significant differences between improved (N and/or L) and unimproved plots.
  - A significant interaction between treatment and year.
  - No significant differences between blocks.

### 2.3 Soil pH
- Surface soil pH (0–5 cm) rose with lime: ~6.19 in limed plots and ~6.38 in nitrogen plus lime plots by Oct 2001.
- Nitrogen addition alone also raised pH, but to a lesser extent.
- Control plots showed little change since baseline (Aug 1998).

### 2.4 Botanical composition
- July 2001 Point Quadrat survey mirrored 2000 methods; no significant difference between surveyors.
- Total hits in 2001 were 58% higher than in 2000, suggesting increased sward density (possibly from grazing removal in 1998).
- Treatment effects on species composition:
  - Agrostis capillaris declined across all treatments in 2001, remaining dominant only in Control and Limed plots.
  - Festuca species (ovina and rubra) increased across treatments, especially in nitrogen and/or lime plots.
  - Fertilised plots favored species associated with improved pastures (Festuca rubra, Poa pratensis, Poa trivialis, Holcus mollis); unimproved plots favored less fertile pasture species (Anthoxanthum odoratum, Nardus stricta).
- Species richness:
  - 24 species identified in unimproved (Control and Biocide) plots vs 18 in Nitrogen and Lime plots, suggesting possible early declines in diversity in the more productive plots.
- Multivariate analysis:
  - Principal Components Analysis (PCA) showed clear separation of nitrogen- and/or lime-treated plots from control/biocide plots.
  - Improved plots tended to cluster at extreme PCA scores; a strong association between Festuca rubra presence, Poa pratensis, and higher biomass.
  - In plots with higher biomass, abundances of Festuca rubra and Poa pratensis increased; abundances of Anthoxanthum odoratum, Nardus stricta, bryophytes (Rhytidiadelphus squarrosus and others) declined.
  - Increased litter observed in nitrogen- and/or lime-treated plots, reflecting faster vegetation turnover with higher soil fertility.

## Site heterogeneity

### 3.1 Variation in surface soil pH and plant community composition
- Spatial patterning evident: columns E and F (slope-facing right) contained more acidic plots than columns on the left, though this is partly confounded by a higher proportion of unimproved or biocide-treated plots in those columns.
- Underlying spatial heterogeneity across the site is suggested by pH differences among columns, particularly in Nitrogen and/or Lime treatments.

### 3.2 Variation in vegetation Biomass
- Biomass values show spatial variation across plots, with several outliers (low biomass) scattered across treatments.
- Higher biomass generally associated with more central site locations (e.g., Nitrogen and Lime plot 2E; Lime plot 2C; Biocide plot 2D; Control 1 plot 2B).
- There is a strong positive correlation between surface soil pH and biomass.
- No significant difference in biomass between blocks (statistical test results reported).

## Data and GIS-oriented notes for exploitation

- Spatial design: plots arranged in blocks with defined treatments (including control plots and combinations such as Nitrogen, Lime, Nitrogen + Lime, and Biocide), enabling map-based visualization of treatment effects and spatial heterogeneity.
- Variables suitable for GIS mapping:
  - Biomass: annual sums or season-by-season sums (1999–2001) by plot; mid-season peak values (e.g., July–August).
  - Soil pH: 0–5 cm depth, October 2001 vs baseline 1998 measurements; treatment-specific pH changes.
  - Botanical composition: species-level relative abundance (hits) per plot; PCA scores per plot; rank-based species abundance by treatment.
  - Weather context: site-level climatic variables (annual rainfall, radiation, temperature, soil moisture) to contextualize biomass and phenology.
- Data collection scales and methods:
  - 0.5 m2 quadrats with subplots S/T/U/V for biomass sampling across five mowing events per year.
  - Point Quadrat surveys with 100 cells per quadrat (5 cm grid) for species hits and composition.
  - Annual and multi-year aggregation allows time-series mapping and trend analysis.
- Data quality and comparability:
  - 2001 field access disrupted by FMD; sampling proceeded under a defined protocol to maintain comparability with prior years.
  - Inter-surveyor consistency checked for the 2001 Point Quadrat survey.
- Analytical considerations for GIS:
  - Normalize biomass by control where comparing treatment effects across years.
  - Use PCA scores and species-hit data to create thematic layers of vegetation communities.
  - Analyze pH-biomass relationships spatially to identify localized soil fertility effects.
  - Map spatial autocorrelation and potential spatial clustering of high-biomass or low-pH zones.

## Key takeaways for GIS specialists

- There is a strong, map-relevant link between soil fertility (pH via liming and nitrogen) and above-ground biomass, with notable spatial heterogeneity across the Sourhope site.
- Nitrogen and lime, alone or in combination, consistently promote biomass and shift botanical composition toward species associated with improved pastures (e.g., Festuca rubra, Poa pratensis).
- The Point Quadrat and biomass data enable detailed spatial analysis of plant community structure, turnover (litter), and species dominance across treatments and years.
- The site’s heterogeneity (columns, slopes, and central vs peripheral plot locations) should be incorporated into GIS models to avoid confounding treatment effects with spatial structure.
- The dataset supports multi-year, plot-level GIS products, including biomass and pH maps, species distribution maps, and PCA-based vegetation typology, useful for policy, land management, and public communication.