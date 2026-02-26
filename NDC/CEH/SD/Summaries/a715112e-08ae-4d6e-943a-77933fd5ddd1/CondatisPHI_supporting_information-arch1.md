# Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

## Overview
- Objective: Evaluate national-scale long-distance connectivity and its protection within England's Priority Habitat Inventory (PHI) using Condatis, a conservation decision-support tool that applies circuit theory to multi-generational range expansion.
- Key approach: Convert habitat data into a raster network, model connectivity across habitat patches, assign protection status, and explore how protecting high-flow patches affects overall connectivity.

## Data Preparation
- Data sources:
  - PHI and Sites of Special Scientific Interest (SSSIs) and National Nature Reserves (NNRs) from Natural England Open Data Geoportal.
  - England polygon boundaries from the Ordnance Survey OpenData Boundary-Line Layer.
- Rasterization and habitat processing:
  - PHI polygons converted to a 50 m raster; each cell’s value set to the habitat type of the polygon whose centroid intersects it.
  - When cells intersect multiple habitat types, the rarest habitat type is assigned.
  - Similar habitat types merged (two groups: upland/lowland calcareous grassland; heathland groups).
  - Minimum mapping unit: 0.1 ha; raster resolution effectively 0.25 ha; mean area loss due to rasterization ~1.8%.
  - Condatis requires manageable resolution; 16 habitat networks analyzed with analyzer-friendly resolutions: 2 km for deciduous woodland and 1 km for all other habitats.
  - Raster sums converted to proportional habitat cover per 50 m cell; used to define Condatis network cells.
- Habitats included (ranked by area; values are hectares for each type).
- Network setup considerations:
  - Aggregation from 50 m to 1–2 km resolutions using rgdal and raster packages in R 3.5.0.
  - Table 1 lists all habitats, with large streams like deciduous woodland dominating extents.

## Condatis Analysis
- Concept:
  - Condatis models multi-generational range expansion by treating breeding habitat cells as nodes in a circuit-like network.
  - A colonisation (resistance) kernel defines the rate of movement between cells, influenced by occupied habitat area and distance.
- Mathematical framework:
  - The colonisation rate between cells i and j is p_i p_j R α^2/(2π) exp(-α d_ij), where:
    - p_i, p_j: habitat area in cells i and j
    - R: reproductive rate
    - α: dispersal parameter (2/α is mean dispersal distance)
    - d_ij: distance between cells
  - A homogeneous matrix outside breeding habitat means non-breeding cells do not serve as nodes; movement is allowed but not breeding occurs there.
- Outputs and interpretation:
  - Circuit conductance: overall network connectedness; strongly correlated with speed of range expansion from source to target.
  - Flow: cell-level measure of a habitat cell’s importance to overall connectivity (i.e., its role as a stepping stone).
- Network setup specifics:
  - Sources and targets defined to reflect northward climate tracking: sources along the south coast of England; targets along the northern border with Scotland (10 km raster used to place S and T).
  - For each habitat network and dispersal option, a flow raster is produced (1 km resolution; 2 km for deciduous woodland).
- Assumptions and limitations:
  - Matrix between habitat cells is assumed homogeneous; explicit landscape barriers are not modelled as in Circuitscape.
  - This abstraction enables analysis of large networks and long-term range expansion, but cannot capture complex matrix effects without nesting another model.

## Protection Assignment and Flow Calculations
- Patch-based approach:
  - Habitat cells are grouped into patches (contiguous cells sharing edges/vertices).
  - Flow values from the Condatis raster are assigned to patches proportionally by intersecting cells’ areas; flows are summed for patches intersecting multiple habitat cells.
  - A patch’s flow is averaged geometrically across the three dispersal distances to yield a single patch-level metric.
  - Flow rank: patch’s rank within its network based on flow (higher flow → higher priority for connectivity).
  - Protection status: a patch is classified as 'protected' if >50% of its area is covered by protected areas (PAs: SSSI or NNR).
- Output: for each habitat network (16 in total) and across the three dispersal distances, patch flow, flow rank, and protection status are compiled.

## Flow-led Patch Protection Scenarios
- Protection investment levels:
  - Simulated increases in protected area by selecting unprotected patches in descending order of flow (i.e., highest-flow patches first).
  - Three scenarios: 1%, 10%, and 25% additional PA coverage.
- Method:
  - Identify unprotected patches, rank by flow, and add patches to PAs until the target percentage increase in PA coverage is reached.
  - Flow values are recomputed to reflect the expanded protection scenario; results summarize how protection prioritization affects network connectivity.

## Condatis vs McRae Circuit Theory
- Core differences summarized:
  - Nodes:
    - McRae (Circuitscape): nodes across entire landscape; breeding habitat cells often treated as zero-resistance injection points.
    - Condatis: nodes placed only in breeding habitat cells.
  - Resistors:
    - McRae: resistance surface defined by landscape features; movement biased by low-resistance directions.
    - Condatis: resistance defined by a distance-dependent colonisation kernel between all habitat cells (adjacent or far apart), assuming a homogeneous matrix.
  - Currents/flow:
    - McRae: current through nodes represents movement likelihood through landscape as a whole.
    - Condatis: current through a node represents the likelihood that a habitat cell was used as a stepping stone in successful multi-generational range expansion.
  - Sources/ground:
    - McRae: fixed sources and ground to drive the circuit.
    - Condatis: sources are start points for range expansion; targets define successful range expansion endpoints.

## Data Structure and Files
- Dataset contents:
  - Five shapefiles, two CSV files, one raster, two R scripts, one RData file, and one text file.
- Key study data files:
  - Patchflow_all.csv: per-patch and network-level metrics including habitat code, patch ID, area, cond_min/cond_max/cond_mean, av_flow, flow_ha, protective_portion, designated (protection), and proflow_min/proflow_max/proflow_av.
  - flow_increases.csv: results of flow-led protection scenarios for each habitat network, including the proportion of total network flow protected when adding patches at 1%, 10%, and 25% PA coverage.
- Demonstration and reproduction files:
  - Demonstration_code.R, demo_hab.shp, demoland.csv, demo_flows.csv, and related files to illustrate Condatis usage and proportional flow allocation.
  - figures.R and associated files for reproducing figures in the related paper.
  - source_target.tif and England.shp used for figures and analysis context.
  - protected_patches.shp and related shapefiles marking protected/unprotected patches; lfens_sample.shp and cagra_sample.shp for sample networks.
- Patch-level attributes:
  - P_id: unique patch identifier within a habitat network.
  - Area: patch area in hectares.
  - Desgntd: binary protection description.
  - Top_10: indicator if patch is above the 90th percentile of flow.
  - Area-based and protection-based fields used for downstream analyses.

## Quality Control
- Floating-point checks: Condatis results were checked for floating-point arithmetic errors (as per Goldberg 1991) and any problematic results were removed.

## References (selected)
- Hodgson, J. A. et al. (2012, 2016): foundational Condatis and range-shift methodology.
- McRae, B. H. et al. (2008): Circuitscape/mcRae circuit theory framework.
- Lenoir, J. et al. (2020): species tracking climate warming patterns.
- Natural England (2019) and Ordnance Survey (2019): data sources.
- R Core Team (2019): software environment used.