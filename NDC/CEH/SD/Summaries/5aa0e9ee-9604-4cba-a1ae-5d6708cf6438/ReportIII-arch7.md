# RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- Overview
  - Large field experiment at Sourhope, Scottish Borders, part of the NERC Soil Biodiversity Thematic Programme.
  - Provides context for various sub-studies with regular, multi-parameter measurements across plots treated with different inputs (Nitrogen, Lime, Nitrogen & Lime, Biocide) and controls.
  - 2001 activities affected by Foot and Mouth restrictions and a change in site management; otherwise management activities (liming, nitrogen, pH measurements, biomass collections, vegetation cutting) largely continued.

- Data collected and measurement types
  - Automatic Weather Station
    - 1999–2001 weather data; 2001 rainfall near long-term average; slight drop in average temperature; soil moisture modestly higher than prior years.
    - Headline measures include rainfall, radiation, soil moisture, and air/soil temperatures at multiple depths.
  - Above-ground biomass
    - Biomass measured across five mowing occasions per summer; peak biomass typically in July–August.
    - 2001 showed a notable rise in biomass relative to 1999–2000, attributed to staffing changes and switch from manual cutting to mechanical shears.
    - Biomass levels higher in plots receiving nitrogen and/or lime; statistical analyses (split-plot ANOVA) show significant treatment effects and year-by-treatment interactions; little to no block effect.
    - Separate analyses used to normalize biomass against a reference plot (C1) to compare treatment impacts.
  - Soil pH
    - pH measured at the upper 5 cm; lime addition increased pH (e.g., limed plots ~6.19; N+L plots ~6.38 in Oct 2001); nitrogen alone also raised pH but to a lesser extent; control plots remained broadly unchanged since baseline (Aug 1998).
  - Botanical composition (Point Analysis)
    - July 2001 Point Quadrat survey; two surveyors with no significant inter-surveyor bias.
    - 2001 hits were 58% higher than 2000, suggesting increased sward density, possibly from grazing removal in 1998.
    - Clear treatment differences in dominant species:
      - Agrostis capillaris declined across all treatments in 2001 (except remaining most abundant in Control 1 and Limed plots).
      - Festuca species (ovina, rubra) increased across all treatments, especially in N and/or Lime plots.
      - Species associated with improved pastures (Festuca rubra, Poa pratensis) were more frequent in fertilized plots (notably N+L).
      - Species associated with poorer pastures (Anthoxanthum odoratum, Nardus stricta) more common in unimproved plots (Control and Biocide).
    - Diversity patterns: unimproved plots contained 24 species; the Nitrogen & Lime plots had 18 species, suggesting potential diversity reduction with stronger fertility improvements.
    - PCA indicates clear separation of improved plots (N and/or Lime) from unimproved (Control and Biocide) plots; increased frequency of Festuca rubra in limed plots; overall directional shifts in species composition with fertility changes.
    - Biomass and species composition are correlated: higher biomass associated with increases in Festuca rubra and Poa pratensis, while Anthoxanthum odoratum, Nardus stricta, bryophytes decline as biomass rises.
    - Increased litter frequency in N and/or Lime plots suggests faster vegetation turnover with higher soil fertility.

- Spatial patterns and site heterogeneity
  - Variation in surface soil pH and plant communities across the site
    - Noted spatial heterogeneity: columns on the right-hand side (E and F) tended to have more acidic plots, particularly in areas with many Control or Biocide plots.
    - Underlying spatial pattern persists, with lower pH in N and/or Lime plots in certain columns.
  - Variation in vegetation biomass
    - 2001 biomass showed outliers with the lowest values in several plots, while higher biomass tended to cluster in more central site locations.
    - Positive correlation observed between surface soil pH and biomass; no significant differences in biomass between blocks.
  - Implications for GIS mapping
    - Spatially explicit data exist at the plot and sub-plot level (plots, blocks, sub-plots S–V, with treatments assigned to plots).
    - Soil pH, biomass, and botanical composition can be mapped over time to illustrate treatment effects, site heterogeneity, and temporal trends.
    - Central site regions may require different interpretation due to spatial clustering of high biomass.

- Key findings relevant to data interpretation and GIS use
  - Treatments with nitrogen and/or lime consistently promote higher above-ground biomass, with lime contributing to pH increases and associated plant community shifts toward species typical of improved pastures.
  - Nitrogen and lime together (N&L) often yield the strongest responses in biomass and shift in species composition (e.g., increased Festuca rubra and Poa pratensis).
  - The sward density increased by 2001, potentially affecting mapping density estimates derived from field surveys.
  - Botanical composition shows clear, treatment-linked trajectories: improved plots favor grasses associated with enhanced fertility; unimproved plots retain more ruderal and bryophyte-dominated communities.
  - The site exhibits spatial heterogeneity that interacts with treatments; this should be considered when designing GIS visualizations and when attributing observed effects to treatments alone.

- Data collection timeline and context for GIS
  - Baseline data collected in 1998; field experiment operated 1999–2001 with periodic measurements.
  - Mowing and sampling events occurred multiple times per year (e.g., five summer cuts; July point quadrat survey; additional surveys in August).
  - Weather data and site management notes (FMD-related access restrictions in 2001; management plan maintained despite disruptions).

- Considerations for GIS-based data products
  - Data layers to create or link:
    - Plot-level biomass by year (1999–2001) and cumulative biomass (1999–2001).
    - Plot-level soil pH (1998 baseline and 2001 values; lime- and nitrogen-driven changes).
    - Botanical composition indicators (dominant species per plot; relative abundance; PCA scores per plot).
    - Treatment map (Nitrogen, Lime, Nitrogen & Lime, Biocide, Control) with spatial arrangement across blocks.
    - Weather/time-series layer (annual rainfall, radiation, soil moisture, temperatures) for contextual environmental background.
  - Spatial scale and alignment
    - Data exist at plot/sub-plot resolution within a block design; ensure coordinates align to a site map or GIS shapefile for Sourhope with plot identifiers.
  - Temporal dimension
    - Include yearly data (1999–2001) and cumulative measures; indicate whether 2001 data reflect methodological changes (mechanical cutting) and any potential comparability caveats.
  - Analytical outputs for end users
    - Maps showing treatment-driven biomass patterns and pH shifts.
    - Species distribution maps highlighting shifts toward Festuca rubra, Poa pratensis, and declines in Agrostis capillaris in response to fertility treatments.
    - PCA-score based thematic maps to illustrate community structure shifts across the site.
  - Data quality notes
    - Be aware of changes in mowing method in 2001 affecting biomass readings.
    - Spatial heterogeneity exists; consider including a spatial covariate or using geostatistical approaches to separate treatment effects from underlying site structure.

- Endnotes and references
  - The document provides detailed statistical tables (ANOVA results, PCA results) and species codes for botanical analysis; these can be used to annotate GIS layers with confidence intervals and species-level attributes.
  - Appendix and figures support interpretation of treatment effects and spatial patterns (e.g., PCA plots, biomass vs. pH relationships).