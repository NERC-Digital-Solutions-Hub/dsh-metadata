# REPORT III
## RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- Overview
  - Large field experiment at Sourhope Farm (Scottish Borders) as part of the NERC Soil Biodiversity Thematic Programme.
  - Objectives include monitoring soil-plant interactions and providing context for other studies; data designed for cross-year comparisons and links between datasets.
  - Study site comprises a structured plot layout with multiple treatments, monitored from 1999–2001; management and site events (notably FMD-related restrictions in 2001) affected operations.

- Spatial design and data types (relevant for GIS mapping)
  - Plot structure: five blocks with multiple treatments replicated across sub-plots; treatments include Control 1, Control 2, Nitrogen (N), Lime (L), Nitrogen & Lime (N&L), and Biocide.
  - Data collected per plot/sub-plot:
    - Above-ground biomass (seasonal, five cuts per year; measurements from 0.5 m² cells; 1999–2001)
    - Soil surface pH (0–5 cm depth; measurements in baseline 1998 and follow-ups in 2001)
    - Botanical composition via Point Quadrat surveys (July 2001; ~100 cells per cell with 25 hits per quadrat; species-level hits)
    - Weather data from an Automatic Weather Station on-site
  - Geospatial outputs suitable for GIS: biomass by plot/year, pH by plot, species composition by plot, site heterogeneity patterns (spatial grid across columns), and temporal change (1999–2001).

- Measurements, methods, and data quality (for GIS data curation)
  - Above-ground biomass
    - Seasonal harvests (May–Sept) across 1999–2001; five cuts per year; 0.5 m² sampling cells.
    - Data normalized to C1 year to compare treatment effects; ln-transformations used for ANOVAs.
    - Key finding: Nitrogen and/or Lime treatments increase biomass; 2001 biomass higher overall due to personnel change and shift to mechanical cutting.
  - Soil pH
    - May show strong liming effect: limed plots ≈ pH 6.19; N&L plots ≈ pH 6.38; nitrogen alone raises pH modestly; control remains near baseline values.
  - Botanical composition
    - July 2001 point-quadrat survey indicates treatment-driven shifts in dominant species.
    - Agrostis capillaris declines across 2001; Festuca spp. increase; improved pastures (Festuca rubra, Poa pratensis) more prevalent in fertilized plots (especially N+L).
    - Species richness higher in unimproved plots (24 species) than in the most improved (18 species in N&L).
    - Multivariate analysis (PCA) separates nitrogen- and lime-treated plots from control/biocide plots; biomass correlates positively with Festuca rubra and Poa pratensis.
  - Site heterogeneity
    - Spatial heterogeneity observed (e.g., columns E and F more acidic; central plots tending toward higher biomass).
    - Positive correlation between surface soil pH and biomass; no major block-level differences detected.
  - Weather (context for GIS layers)
    - 2001 rainfall near long-term average; radiation stable; slight temperature decrease and higher soil moisture vs. 2000.

- Temporal context and data considerations
  - Timeframe: 1999–2001 data with 1998 baseline; annual and multi-year comparisons enabled.
  - 2001 field work impacted by Foot and Mouth Disease restrictions and a change in site personnel, which influenced biomass measurements (notably a shift to mechanical cutting).
  - Data presented include tables and figures (e.g., ANOVA results, PCA, species abundance), with explicit treatment-year interactions and year-to-year effects.

- Implications for GIS-based data products
  - Potential map layers:
    - Biomass by plot and by year (1999–2001), including cumulative biomass.
    - Soil surface pH by plot (baseline vs. follow-up, 0–5 cm depth).
    - Species composition by plot (dominant species per plot, 2001 survey; relative abundance by treatment).
    - Spatial heterogeneity: pH and biomass gradients across site columns and blocks.
    - Correlation maps linking biomass to pH and to key species (e.g., Festuca rubra, Poa pratensis).
  - Considerations for integration:
    - Standardize plot identifiers across years and treatments; incorporate block and column identifiers for spatial queries.
    - Align biomass measurements (five summer cuts per year) into a consistent time-series layer.
    - Include metadata on methodological changes (e.g., switch from manual to mechanical cutting in 2001) to support accurate temporal comparisons.
  - Data quality notes:
    - Consistent surveying between two surveyors in 2001 with no significant difference observed.
    - Use of standardized measurement protocols and transformations (e.g., ln-transformed biomass for analyses) to inform visualization and modeling.

- Summary of key takeaways for GIS work
  - The Sourhope field experiment provides rich, spatially explicit data linking management treatments to biomass, soil chemistry, and plant community composition.
  - Strong spatial structure and site heterogeneity influence biomass and soil pH, yielding meaningful map-based patterns.
  - Temporal dynamics (1999–2001) reveal treatment effects, with notable anomalies in 2001 due to operational changes and external restrictions.
  - The dataset supports multi-layer GIS analyses and visualization to explore treatment impacts, soil-plant interactions, and spatial gradients across the field site.