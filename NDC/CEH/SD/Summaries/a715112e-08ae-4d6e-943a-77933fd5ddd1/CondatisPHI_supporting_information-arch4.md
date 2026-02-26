Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

## Purpose and approach
- Evaluates national-scale, long-distance connectivity and its protection within England's Priority Habitat Inventory (PHI) using a circuit-theory–inspired, multi-generational model (Condatis).
- Focuses on habitat networks across 16 priority habitats to identify important patches for connectivity and how protection can be optimized.
- Compares Condatis outputs to traditional circuit theory approaches, highlighting multi-generational range expansion.

## Data Preparation
- Data sources: PHI, Sites of Special Scientific Interest (SSSIs) and National Nature Reserves (NNRs) from the Natural England Open Data Geoportal; England boundary from the Ordnance Survey OpenData Boundary-Line Layer.
- PHI polygons converted to a 50 m raster, with habitat type determined by polygon centroid; rarest habitat type selected when overlapped.
- Similar habitat types merged (two groupings) to reflect functional similarity.
- Rasterization introduces some loss (mean area lost ~1.8%); concerns mitigated by focusing on larger-scale patterns.
- Condatis network cells (habitat) created by aggregating 50 m rasters to 1–2 km resolution (depending on habitat size) to balance detail with memory constraints.
- Habitat networks defined for 16 priority habitat types with varying mapped extents.

## Condatis Analysis and Modelling
- Condatis models multi-generational range expansion using a colonisation kernel between habitat cells i and j.
- Nodes: habitat cells containing breeding habitat; edges (resistors) defined between all pairs of nodes using a distance-dependent colonisation rate.
- Key equation for colonisation rate (simplified): p_i p_j R α^2/(2π) exp(-α d_ij), where p_i/p_j are habitat cell areas, R is reproductive rate, α relates to mean dispersal distance, and d_ij is distance between cells.
- Matrix outside breeding habitat is assumed homogeneous (non-breeding landscape not modeled as a resistance surface).
- Outputs include circuit conductance (network-wide connectivity) and flow (cell-level contributions to connectivity).
- Sources and targets defined to reflect northward range shifts: sources along the south coast of England; targets along the northern border with Scotland.
- Calculations performed for three mean dispersal distances (2, 4, 8 km) with fixed reproductive rate R = 100 (one emigrant per hectare). This choice emphasizes network structure rather than species-specific predictions.

## Model Assumptions and Limitations
- Assumes homogeneous matrix between habitat cells; does not model landscape barriers explicitly (unlike Circuitscape).
- Resilience to computational constraints by not simulating full matrix heterogeneity; notes potential future work to nest models for matrix complexity.
- Nodes defined only at breeding habitat cells; patches used to assess contribution to connectivity.

## Protection, Patches, and Ranking
- Flow results mapped to 50 m habitat rasters, then patches identified as contiguous cells (edge/vertex sharing).
- Flow assigned to patches proportional to intersecting cell flows; patches intersecting multiple habitat cells had flows summed and proportionally allocated.
- Patch flow rank calculated as the geometric average of flow across three dispersal distances; higher flow indicates greater importance for connectivity.
- Patches classified as 'protected' if at least 50% of their area is within protected areas (PAs, i.e., SSSIs/NNRs).

## Flow-Led Patch Selection Scenarios
- Investigated three protection investment levels by flow: 1%, 10%, and 25% increases in protected habitat across each network.
- Within each network, unprotected patches were ranked by flow (highest flow first) and added to the PA network until the target protection level was reached.
- This approach assesses how prioritizing high-flow patches could improve overall network protection.

## Data Outputs and Structure
- Data products include: 
  - Patchflow_all.csv: patch-level conductance metrics, area, protection status, and flow-derived indicators (cond_min, cond_max, cond_mean, av_flow, flow_ha, protected_portion, designated, proflow_min, proflow_max, proflow_av).
  - flow_increases.csv: results of the 1%, 10%, and 25% flow-protection scenarios.
- Additional materials to support reproducibility and demonstrations:
  - Demonstration_code.R, demo_hab.shp and related files, demonstration datasets (demoland.csv, demo_flows.csv), and figures.R to reproduce study visuals.
  - Spatial data and shapefiles for England, protected patches, and example networks (e.g., lfens_sample.shp, cagra_sample.shp) with fields describing patch area, protection status, and flow-derived metrics.
- Quality control: checks for floating-point arithmetic errors; problematic results removed.

## Differences from Circuitscape and McRae-Style Circuit Theory
- Condatis uses a colonisation kernel to define resistance between all habitat cell pairs, rather than a landscape-resistance surface between adjacent cells.
- Nodes are placed only in breeding habitat cells (not across the entire landscape), and network conductance is tied to multi-generational colonisation rather than single-step movement.
- Flow measures indicate the likelihood that a habitat cell is used as a stepping stone in successful range expansion, not just the amount of current through a landscape.
- The approach trades off detailed matrix heterogeneity for tractable analysis of large networks and long-term expansion dynamics.

## Reproducibility and governance implications for Data Leaders
- Demonstrates a structured workflow from data acquisition to rasterization, network construction, modeling, and protection prioritization.
- Emphasizes the importance of data standardization, metadata, and documentation (clear data structures, field definitions, and reproducible code) to enable reuse and audits.
- Highlights the value of integrating data across multiple sources (PHI, protected areas, administrative boundaries) and maintaining up-to-date, discoverable datasets for planning and policy support.
- Reveals practical data-management considerations (resolution choices, patch delimitation, protection overlap thresholds, and quality control) that affect analysis outputs and decision-making.