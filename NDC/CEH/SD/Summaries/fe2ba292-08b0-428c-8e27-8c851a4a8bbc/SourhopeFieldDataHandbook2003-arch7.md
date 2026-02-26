# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview for GIS Specialists
- Provides spatially explicit, map-based data relationships to support GIS-based analysis and data products.
- Multi-scale sampling framework (blocks, plots, subplots, Ecotron) enabling hierarchical spatial visualization and modeling.
- Rich dataset combining vegetation surveys, soil profiles, chemistry, moisture, horizon descriptions, and site metadata.

## Spatial design and data architecture
- Five-block layout along a slope with multiple nested units: blocks → plots → subplots → Ecotron plots.
- Block 4, Block 5 details included in this chunk, plus ECOTRON PLOT data, illustrating the grid structure and spatial partitioning for rigorous spatial analysis.
- Detailed site coordinates, altitude, slope, drainage, soil series, and parent material support accurate GIS georeferencing and layer construction.

## Data types collected
- Soil analyses
  - Auger samples: measured %N, %C, C:N ratio, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH (H2O and CaCl2).
  - Horizon-by-horizon measurements for profile pits (e.g., FH, H, Ah, AB, Bg, BCg, Cg) with depth ranges, descriptions, and sample weights.
- Vegetation surveys
  - Presence/absence data, counts, and species totals by plots/subplots.
  - Documentation of dominants and indicator species across subplots.
- Site and horizon metadata
  - Grid references, altitude, slope, drainage, soil series, and parent materials.
  - Formal soil profile descriptions for blocks (e.g., Block 5 soil profile from 0–100 cm with named horizons).

## Variables and attributes (examples)
- Soil chemistry and physical properties: %N, %C, C:N, Ca (meq/100g), Na, K, Mg (meq/100g), %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
- Soil moisture and horizon data: depth ranges for each horizon, color, structure notes, root presence.
- Vegetation metrics: species incidence, totals per plot/subplot, indicator species (as observed in Twinspan/NVC analyses).
- Spatial descriptors: block, plot, subplot IDs, Ecotron labels, grid references, altitude, slope, drainage status.

## Data organization and GIS readiness
- Appendix A provides block- and plot-level data, soil pits, horizon descriptions, and quantitative measurements suitable for GIS layer creation.
- Spatial data potential includes:
  - Horizon-level soil property layers (e.g., pH, %N, %C, %LOI) by depth interval.
  - Plot-level summaries of soil chemistry and moisture.
  - Species distribution layers derived from presence/absence matrices and vegetation surveys.
  - Classification overlays (NVC and Twinspan groupings) with indicator species.
- Hierarchical GIS workflows can link treatment metadata with vegetation and soil data across blocks, plots, and subplots.

## GIS use-cases and data products
- Multi-scale mapping of soil gradients and biodiversity:
  - Visualize spatial variation in soil pH, C/N, nutrients, and moisture across blocks and plots.
  - Map community types (U4d, U5b-like patches) and indicator species distributions.
- Habitat and biodiversity modeling:
  - Overlay vegetation data with soil properties to model habitat suitability and ecosystem responses to perturbations (e.g., lime, nitrogen, biocide treatments).
- Temporal and comparative analyses:
  - Compare Ecotron versus external plots to assess controlled-environment effects on soil-vegetation dynamics.
- Data for reproducible GIS workflows:
  - Clear linkage between treatment allocations, sampling schemes, and spatial data enables replication and map-based reporting.

## Data quality and considerations
- Dataset is rich but contains incomplete/missing values and some transcription/formatting inconsistencies in this chunk (common in field data compilations).
- Users should validate coordinate references, horizon labeling, and unit consistency before GIS integration.
- Careful data cleaning and harmonization recommended to ensure reliable spatial analyses and interoperable layers.

## Practical takeaways for GIS workflows
- Leverage the clear hierarchical grid (blocks → plots → subplots → Ecotron) to build scalable GIS layers and multi-resolution maps.
- Build horizon-specific raster or vector layers for soil variables, complemented by plot-level summaries and species presence/absence rasters.
- Integrate site metadata (grid refs, altitude, slope, drainage) to contextualize soil and vegetation patterns within spatial models.
- Utilize Appendix A and ECOTRON datasets to create benchmark GIS datasets for spatial analysis, visualization, and biodiversity mapping.