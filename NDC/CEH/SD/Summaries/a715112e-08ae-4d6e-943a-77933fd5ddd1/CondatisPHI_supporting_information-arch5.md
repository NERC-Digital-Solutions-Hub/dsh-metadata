# Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

## Overview
- Study evaluates connectivity across England’s priority habitat networks (PHI) and protection of this connectivity.
- Uses Condatis, a circuit-theory–inspired tool, to model multi-generational range expansion across habitat networks and to assess the impact of protecting habitat patches.

## Data Sources and Preparation
- Data sources:
  - Priority Habitat Inventory (PHI), Sites of Special Scientific Interest (SSSIs), National Nature Reserves (NNRs) from Natural England Open Data Geoportal.
  - England polygon boundaries from Ordnance Survey OpenData Border-Line Layer.
- Rasterization and habitat preparation:
  - PHI polygons converted to 50 m raster; cell value reflects the polygon’s habitat type via centroid intersection.
  - When cells intersect multiple habitat types, the rarest type takes precedence.
  - Habitats merged into functionally similar groups (two groupings described).
  - Minimum mapping unit: 0.1 ha; raster resolution effectively 0.25 ha.
  - Condatis network resolution determined by RAM constraints: 2 km for deciduous woodland; 1 km for all other habitats.
  - 50 m rasters aggregated (via rgdal and raster in R 3.5.0) to produce proportional habitat cover per larger cell.
- Losses and practicality:
  - Small patches may be lost during rasterization (mean area loss ~1.8%), considered unlikely to bias results.
- Outputs and tools:
  - Analysis performed in R with rgdal and raster packages.
  - 16 habitat networks analyzed; three mean dispersal distances used in Condatis.

## Condatis Analysis: Method and Settings
- What Condatis does:
  - Adapts circuit theory to model multi-generational range expansion, incorporating reproduction within breeding habitat.
  - Each habitat cell with breeding habitat is a node; colonisation resistance is defined by a kernel (not by a spatial resistance surface).
- Key model components:
  - Colonisation rate between cells i and j is proportional to p_i p_j R α^2/(2π) exp(-α d_ij) (Eqn 1).
  - p: habitat area of a cell; R: reproductive rate; α relates to mean dispersal distance (2/α is mean dispersal distance); d_ij is distance between cells.
  - Matrix outside breeding habitat is homogeneous; cannot breed there.
- Outputs used:
  - Circuit conductance (overall network connectivity) and flow (per-cell importance for connectivity).
  - Flow indicates each cell’s contribution to connectivity; loss of a high-flow cell reduces conductance.
- Experimental design:
  - 16 priority habitat networks; three dispersal-distance options: 2, 4, and 8 km.
  - Reproductive rate fixed at R = 100 (one emigrant per hectare); relative comparisons preserved across networks.
  - Source/target placement: along the south coast (sources) and northern border with Scotland (targets) to mimic poleward range shifts.
- Patch-level assignment and protection:
  - Habitat rasters converted to patches (contiguous grid cells sharing edges/vertices).
  - Patch flow assigned proportionally based on intersecting habitat cells; flow across patches summed if they cross multiple cells.
  - Flow rank for patches computed as geometric mean of patch flow across the three dispersal distances.
  - Patches classified as “protected” if >50% of patch area overlaps protected areas (PAs, i.e., SSSIs/NNRs).
- Patch-level results:
  - Outputs include patch flow, flow rank, patch area, and protection status across networks and dispersal distances.

## Differences from Other Circuit Theory Approaches
- Condatis vs Circuitscape:
  - Condatis models multi-generational range expansion with a colonisation kernel; does not use a resistance surface for between-patch landscapes.
  - Nodes are habitat cells only (not all landscape cells); resistors connect all nodes, not just adjacent ones.
  - Ground/targets in Condatis represent successful range expansion endpoints; sources are initial expansion points.
  - This approach trades off some realism of barriers for computational scalability over large networks.

## Data Structure and Outputs
- Dataset composition:
  - Five shapefiles
  - Two CSV files (Patchflow_all.csv and flow_increases.csv)
  - One raster
  - Two R scripts
  - One Rdata file and one text file
- Data categories:
  - Study data: patch flow, conductance, flow values; network-level and patch-level metrics.
  - Demonstration data: example network, demonstration code, and coordinates for reproducing Condatis outputs.
  - Reproduction figures: scripts and data for generating figures (e.g., source/target rasters, England boundary, protected patches).
- Key files and purposes:
  - Patchflow_all.csv: per-patch and per-network metrics including habitat code, patch ID, area, cond_min/cond_max/cond_mean, av_flow, flow_ha, protected_portion, designated, proflow_min/proflow_max/proflow_av.
  - Flow_increases.csv: results of flow-led protection scenarios (1%, 10%, 25% PA increases), including network-level flow protection before/after augmentation.
  - Supporting files: demonstration_code.R, demo_hab.shp, source_target.tif, protected_patches.shp, protected_sites.shp, England.shp, and related spatial data.

## Quality Control and Reproducibility
- Quality control:
  - Condatis results checked for floating-point arithmetic errors; implicated results removed as needed.
- Reproducibility:
  - Code and data intended for open, repeatable analyses (R scripts, demonstration data, and figure scripts).
  - Clear documentation of data sources, processing steps, and file structure to enable replication.

## Practical Considerations for Data Stewards
- Data provenance and governance:
  - Track origin, licensing, and access terms for Natural England Open Data and OS boundary datasets.
  - Maintain clear metadata for each dataset: spatial reference (likely OSGB/British National Grid), resolution, processing steps (rasterization, aggregation, patch detection), and versioning.
- Data management and storage:
  - Large raster and network outputs require organized storage, with provenance links back to original PHI/SSSI/NNR sources.
  - Separate raw inputs from processed outputs; preserve R scripts and demo data for reproducibility.
- Metadata and documentation:
  - Document transformation steps (50 m to 1–2 km aggregation, cell-to-patch assignment, flow ranking, protection classification).
  - Describe the meaning of outputs (conductance vs. flow; patch-level metrics; protection attribution).
- Data sharing considerations:
  - Ensure licensing compliance for all included data; provide access to code and outputs to enable reuse.
  - Include clear guidance on how to interpret flow-based patch rankings and protection scenarios for conservation planning.

## Key Takeaways
- The study integrates open habitat data with a scalable, multi-generational connectivity model (Condatis) to identify critical patches and assess protection scenarios across England’s priority habitats.
- Data preparation involves careful rasterization and aggregation choices, with attention to patch delineation and loss during processing.
- Outputs include detailed patch-level metrics and scenario analyses to inform conservation investments in protected areas, underpinned by robust quality control and reproducibility practices.