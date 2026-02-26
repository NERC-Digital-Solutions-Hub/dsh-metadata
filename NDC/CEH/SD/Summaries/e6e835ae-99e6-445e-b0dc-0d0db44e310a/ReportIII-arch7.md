# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- Purpose and context
  - Intensive field experiment at Sourhope (Scottish Borders) under the NERC Soil Biodiversity Thematic Programme.
  - Aimed to provide a broad context for partner studies with a standardized monitoring framework.
  - Measurements span 1999–2001 to enable year-to-year comparison and links to end-user data.
  - Site management in 2001 affected by Foot and Mouth Disease restrictions and a change of site officer.

- Experimental design and data scope (GIS-relevant structure)
  - Plot layout: multiple plots organized into blocks with sub-plots (S, T, U, V) within each main plot.
  - Treatments (main nutrients and management): Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Biocide (with some analyses focusing on a subset excluding one control).
  - Data collected include: above-ground biomass (monthly summer cuts), soil pH (top 5 cm), botanical composition via Point Quadrat surveys, and weather variables from an Automatic Weather Station.
  - Methods suitable for GIS workflows: plot-level attributes (treatment, biomass, pH), species abundance, and multiyear change indicators; spatial heterogeneity across columns/blocks noted.

- 2. Results

  - 2.1 Automatic Weather Station
    - 2001 weather: rainfall near long-term average; radiation stable; average temperatures slightly lower; soil moisture modestly higher than prior years.
    - Data provide context for biomass and pH changes and support temporal GIS overlays (year-by-year comparisons).

  - 2.2 Above-ground biomass
    - Consistent hierarchy of biomass across treatments with peak production in July/August each year.
    - 2001 biomass markedly higher than 1999–2000, likely due to personnel changes and switch from manual cutting to mechanical shears.
    - Normalisation against the Control 1 (C1) used to assess relative treatment effects; nitrogen and/or lime additions had the strongest positive effect on biomass.
    - Statistical findings: significant differences between improved (N and/or L) vs unimproved plots; significant interaction between treatment and year; no significant block effects.
    - Implication for mapping: biomass yields and treatment effects can be visualized as yield surfaces across plots, with notable treatment-driven contrasts.

  - 2.3 Soil pH
    - Liming continued to raise soil pH in the top 5 cm: average pH around 6.19 in limed plots; 6.38 in Nitrogen & Lime plots.
    - Nitrogen alone also raised pH but to a lesser extent; control plots remained largely unchanged since baseline (1998).
    - pH changes correlate with biomass patterns, informing GIS-based pH-biomass relationship layers.

  - 2.4 Botanical composition
    - July 2001 Point Quadrat survey: consistent survey methodology with good inter-surveyor agreement; 2001 survey recorded 58% more total hits than 2000, suggesting increased sward density (potentially from grazing stock removal in 1998).
    - Treatment effects on species composition:
      - Agrostis capillaris declined across all treatments in 2001; Festuca species (ovina, rubra) increased across treatments.
      - Fertilised plots (especially Nitrogen and/or Lime) showed more species associated with improved pastures (Festuca rubra, Poa pratensis).
      - Unimproved plots (Control and Biocide) maintained higher presence of species typical of less fertile pastures (Anthoxanthum odoratum, Nardus stricta).
      - Diversity changes: 24 species in unimproved treatments vs 18 in Nitrogen & Lime, suggesting potential diversity decline with intensive treatments.
    - Multivariate pattern: Principal Components Analysis (PCA) largely separates nitrogen- and/or lime-treated plots from control/biocide plots; nitrogen/lime plots show more extreme compositional shifts toward Festuca rubra and associated grasses.
    - Biomass correlations: higher biomass associated with higher relative abundance of Festuca rubra and Poa pratensis; declines in Agrostis vinealis, Nardus stricta, bryophytes, and some litter-associated taxa as biomass increases.
    - Litter and turnover: nitrogen and/or lime treatments linked to increased litter, indicating faster turnover with higher fertility.
    - Implication for GIS: species-dominance maps, PCA-derived ordination layers, and biomass overlays illustrate how nutrient amendments shift community composition over space and time.

- 3. Site heterogeneity

  - 3.1 Variation in surface soil pH and plant community composition
    - Spatial heterogeneity observed: columns or sections (notably right-hand side columns E and F) exhibited more acidic conditions; underlying pattern linked to treatment composition across columns.
    - Implication: spatially explicit pH and community composition maps should account for column-level variability when interpreting treatment effects.

  - 3.2 Variation in vegetation biomass
    - Biomass values show spatial patterns: outliers with low biomass commonly located in edge/isolated plots; higher biomass generally in centrally located plots (e.g., some N and L plots, central locations).
    - Positive correlation detected between surface soil pH and biomass.
    - No significant differences in biomass between blocks, indicating that within-site spatial structure (columns, plot positioning) contributes to variability beyond block effects.

- Data interpretation and GIS-ready takeaways
  - The Sourhope dataset provides rich, plot-level, multi-year spatial attributes (biomass, pH, species composition, litter) linked to explicit treatments and a defined plot layout, suitable for GIS-based analysis and map-based data products.
  - Key GIS layers to consider:
    - Treatment layer per main plot with sub-plot granularity (C1, C2, N, L, N&L, B).
    - Above-ground biomass (summer sums and year-by-year changes) with normalization to C1 for cross-year comparisons.
    - Topsoil pH (5 cm depth) per plot, showing lime- and nitrogen-driven shifts.
    - Species abundance layers per plot (hits per species, major taxa like Festuca rubra, Poa pratensis, Agrostis capillaris, etc.), plus PCA ordination proxies for community composition.
    - Spatial heterogeneity indicators (column-level pH patterns, central vs. edge biomass trends, litter turnover indicators).
  - Practical considerations for end users
    - In years with management disruptions (e.g., 2001 FMD restrictions), interpret data with context about restricted site access and temporary protocol changes (e.g., biocide timing).
    - When comparing years, adjust for procedural changes (e.g., mowing method shift) as they can influence biomass measurements.
    - Use multi-variate analyses (e.g., PCA) alongside raw biomass and pH maps to understand treatment-driven shifts in plant communities.
  - Cited evidence strength
    - Biomass and pH responses show clear, statistically supported treatment effects, with year-to-year interactions and strong correlations between pH and biomass.
    - Botanical composition trends are robust across years, with notable shifts in species dominance aligned to fertilisation and liming treatments; diversity effects appear nuanced, potentially reducing species richness under intensive treatments.

- Acknowledgements
  - Acknowledged personnel contributions and site staff support; data management coordinated with MLURI and associated researchers.