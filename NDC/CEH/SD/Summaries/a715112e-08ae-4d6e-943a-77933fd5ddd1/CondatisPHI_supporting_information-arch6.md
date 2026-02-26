# Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

- Objective: Provide data-driven support for evaluating national-scale, long-distance connectivity and its protection within England's Priority Habitat Inventory (PHI) using Condatis, a conservation decision-support tool that adapts circuit theory to multi-generational range expansion.
- Key outputs used for decision-support: conductance (overall network connectedness), flow (cell-level importance for connectivity), and patch-level protection status linked to flow.

## Data Preparation

- Data sources: PHI, Sites of Special Scientific Interest (SSSIs) and National Nature Reserves (NNRs) from Natural England Open Data Geoportal; England boundaries from OS OpenData Boundary-Line Layer.
- Habitat rasterization and processing:
  - PHI polygons converted to 50 m raster; cell value reflects habitat type of polygon centroid intersected.
  - When cells intersect multiple habitat types, the rarest habitat type takes precedence.
  - Similar habitat types merged (two pairs) to reflect functional similarity.
  - Minimum mapping unit: 0.1 ha; raster resolution effectively 0.25 ha; mean area loss from rasterization ~1.8%.
- Habitat network resolution:
  - Condatis requires fine but manageable resolution; 2 km for deciduous woodland due to extent, 1 km for all other habitats.
  - 50 m PHI raster aggregated to 1 km/2 km cells to form habitat cell rasters representing proportional habitat cover.

## Condatis Analysis

- Concept: Condatis models multi-generational range expansion using a circuit-theory framework with a colonisation kernel to define resistance between habitat cells.
- Nodes and network: Each habitat cell containing breeding habitat is a node; resistance between nodes derives from the colonisation kernel (Eqn 1). A full matrix of connections between all habitat cells is considered.
- Matrix assumption: The non-habitat matrix is treated as homogeneous (no explicit barriers), enabling analysis of very large networks but simplifying landscape complexity.
- Outputs:
  - Conductance: overall network connectedness; strongly correlated with speed of range expansion from source to target.
  - Flow: cell-level measure of each habitat cell’s contribution to connectivity; used to infer patch importance and potential vulnerability to patch loss.

## Condatis settings and inputs

- Habitat networks: 16 priority habitat networks analyzed.
- Dispersal distances (mean): three values representing a range of taxa (2, 4, 8 km); these reflect 2/α in Eqn 1.
- Reproductive rate (R): fixed at 100 (one emigrant per hectare) to standardize comparisons; affects absolute flow/conductance but preserves relative differences between networks.
- Sources and targets: southern England coast as sources; northern England/Scotland border as targets (to simulate northward range shifts with climate warming).

## Patch Flow and Protection Assignment

- Flow results: produced as a 1 km (2 km for deciduous woodland) raster of flow across habitat cells.
- Patch definition: patches are contiguous 50 m habitat cells sharing edges/vertices; flow assigned to patches proportionally by their area; for patches spanning multiple habitat cells, flows are summed.
- Protection status: patches classified as 'protected' if >50% of their area lies within protected areas (SSSIs/NNRs).
- Flow ranking: patches receive a flow rank (based on geometric average flow across the three dispersal distances) to indicate relative importance for network connectivity.

## Flow-led Patch Selection

- Investment scenarios: simulate three protection investment levels—1%, 10%, and 25% increases in protected habitat proportion within networks.
- Method: unprotected patches are ranked by flow (highest first) and added to protected areas until the target PA increase is met.
- Purpose: assess how prioritizing high-flow patches for protection could enhance network connectivity.

## Differences from Circuitscape (McRae-style)
- Condatis focuses on multi-generational colonisation with a distance-dependent colonisation kernel rather than a landscape-resistance surface between adjacent nodes.
- Nodes exist only in breeding habitat cells; the matrix is assumed homogeneous.
- Resistors connect all nodes (not just adjacent ones), enabling efficient analysis of large networks and the long-term range expansion process.
- In contrast, Circuitscape typically uses resistance between adjacent cells and emphasizes current flow through a landscape grid.

## Data Structure and Reproducibility

- Dataset contents (five categories):
  - Data from the study: Patchflow_all.csv; flow and conductance data; flow_increases.csv.
  - Demonstration data: Demonstration_code.R; demoland.csv; demo_flows.csv; demo_hab.shp; associated demonstration data.
  - Reproduction figures: figures.R; source_target.tif; England.shp; protected_patches.shp; lfens_sample.shp; cagra_sample.shp; README.txt explaining CSVs and R files.
- Key outputs:
  - Patchflow_all.csv: habitat-level conductance (cond_min, cond_mean, cond_max) and flow per patch; protected_portion; designation status; proflow metrics (min, max, av).
  - Flow_increases.csv: proportion of additional flow protected under 1%, 10%, and 25% PA expansion; flow values associated with those investments.
- Data granularity:
  - Habitat-level results are aggregated to patches; patch-level protection status and flow inform conservation prioritization.

## Quality Control

- Checks conducted for floating-point arithmetic errors; any problematic results were removed to ensure robust outputs.

## References and Data Sources

- Core methodological basis and prior studies cited (e.g., Hodgson et al., McRae et al., Lenoir et al.) and data portals (Natural England Open Data Geoportal; Ordnance Survey OpenData).

- Data support for policy and planning: the dataset enables exploration of how protecting high-flow patches can influence overall connectivity, supporting evidence-based prioritization decisions.