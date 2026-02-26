# Parsonage Down experiment

- Two linked field studies conducted at Parsonage Down:
  - Experiment 1: Assess how different plant functional groups (FGs) influence soil carbon storage and nutrient cycling, using a mix of hand weeding and herbicide spot spraying to create distinct plant communities.
  - Experiment 2: Use seven herbicides to alter plant communities and examine resulting carbon and nitrogen cycling dynamics.

## Experimental design and spatial layout (GIS perspective)

- Field layout:
  - 7 plots across (width) by 6 plots down (length), forming a grid of 42 plots per replication.
  - Treatments are arranged so that across each row all three plant functional groups (FG1, FG2, FG3) appear in various combinations; this scheme is replicated across six rows.
  - Plots are described with FG combinations (e.g., FG1, FG2, FG3, FG1&2, FG1&3, FG2&3, FG1&2&3) to create a full factorial design (three factors with combinations).
  - Some plots are located on different field positions (e.g., bottom of slope), implying a potential slope/terrain layer for spatial analysis.
- Temporal scope:
  - Treatments implemented in 2013–2015 (years of manipulation and monitoring).
- Plot coding:
  - Each plot has a coded treatment assignment (e.g., FG1, FG2, FG3, and their combinations) mapped to a 7×6 grid; several lines in the document show the pairing of plots across columns and rows to ensure replication.

## Plant functional groups and species (data attributes for mapping)

- FG1: Deep, thick tap roots; simple root structure; thin, large leaves. Includes many annuals, biennials, and some long-lived species.
  - Predicted indicators: higher soil carbon storage due to deep root carbon inputs.
  - Representative species listed (e.g., Sanguisorba minor, Daucus carota, Dactylis glomerata) and a broader long species list provided.
- FG2: Small rosettes with very small tap roots.
  - Predicted indicators: lower above-ground biomass contribution and potentially lower carbon inputs to soil.
  - Representative species listed (e.g., Bellis perennis, Festuca rubra, Primula veris, Thymus pulegioides) and extensive species list.
- FG3: Large plants with shallow, thin roots and fast, high microbial activity; rapid carbon and nitrogen cycling.
  - Predicted indicators: potentially lower soil carbon storage due to fast turnover; more rapid organic matter processing.
  - Representative species listed (e.g., Vicia cracca, Avenula spp., Ranunculus spp.) and extensive species list.
- Species inventories are provided as dense lists per group, indicating per-plot presence could be captured as species-level or functional-group indicators.

## Experiment 2: Herbicide treatments (data attributes for mapping)

- Seven herbicides used to alter plant communities:
  - 2,4D: kills broadleaf weeds
  - Foundation: kills perennial broadleaf weeds and tree seedlings
  - Fusilade Max: kills wild oats and grass weeds
  - Kerb: kills blackgrass and other grasses and broadleaf weeds
  - MCPB: kills broadleaf annual and perennial weeds (e.g., thistle, buttercup)
  - Shield: kills perennial broadleaf weeds
  - Starane: broad range of broadleaf weeds
- Purpose: examine how different shifts in plant community composition influence soil carbon and nutrient cycling, within the same grid framework.

## GIS-ready data considerations

- Spatial data to capture:
  - Plot polygons (7×6 grid) with coordinates and relative location (e.g., bottom slope) as geospatial layers.
  - Treatment attributes per plot: FG composition (single group or combination: FG1, FG2, FG3, FG1&2, FG1&3, FG2&3, FG1&2&3).
  - Replicate/row identifiers for statistical mapping and QA.
  - Slope position and terrain features to enable spatial analyses of microtopography effects.
  - Herbicide treatment layer for Experiment 2 (per plot, which herbicide(s) were applied, timing if available).
  - Plant functional group assignment per plot along with potential species presence indicators (for more detailed habitat mapping).
- Temporal data:
  - Multi-year treatment records (2013–2015) and corresponding measurements of carbon and nitrogen cycling rates; enables time-series GIS analyses.
- Outputs to map or visualize:
  - Spatial distribution of FG treatments and their combinations.
  - Predicted carbon cycling indicators by plot and by year.
  - Overlay of slope/topography with treatment response to explore environmental gradients.
  - Herbicide regime maps linked to resulting community composition and soil metrics.
- Data quality and integration notes:
  - Ensure consistent coding for FG1/FG2/FG3 and their combinations across the dataset.
  - Align plot coordinates with field notes (e.g., bottom slope areas) to maintain accurate spatial representation.
  - Integrate species lists at the plot level if species-level mapping is desired (may require standardized taxonomy).

## Potential GIS products and use cases

- Interactive map of the 7×6 plot grid showing per-plot FG treatments, replicate information, and slope position.
- Time-enabled maps/3D surfaces of soil carbon and nutrient cycling indicators by plot across 2013–2015.
- Spatial analysis of treatment effects by topography (e.g., slope vs bottom slope plots) and their influence on carbon storage.
- Layered visualization of Experiment 2: herbicide regimes overlaid with plant community outcomes and soil metrics.
- Dashboard-style summaries for policy colleagues, clients, or the public to explore how plant functional groups influence soil processes spatially.

## Summary of aims and challenges relevant to GIS specialists

- Aims alignment:
  - Create map- and plot-based data products to enable exploration of how plant functional groups and herbicide treatments affect soil carbon and nutrient cycling.
  - Use the grid experimental design to compare spatial patterns and treatment effects across the field site.
- Key challenges to anticipate:
  - Integrating complex species- and treatment-level data into coherent geospatial datasets.
  - Managing multi-year data with consistent plot identifiers and spatial coordinates.
  - Handling potential data gaps or inconsistencies in plot location (e.g., slope-position notes) and ensuring reproducible spatial analyses.