# Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

- Purpose: Describe data preparation, methods, and datasets used to evaluate national-scale connectivity and its protection within England's Priority Habitat Inventory (PHI), Sites of Special Scientific Interest (SSSIs) and National Nature Reserves (NNRs).

## Data preparation and habitat rasterization

- Data sources: PHI, SSSIs, NNRs from Natural England Open Data Geoportal; England boundary polygons from OS OpenData Boundary-Line.
- Habitat conversion: PHI polygons converted from vector to 50 m raster; cell value equals the habitat type of the polygon intersected by the cell centroid; in cells with multiple habitats, the rarest type takes precedence.
- Habitat merging: Upland/Lowland calcareous grassland merged; upland heathland/lowland heathland/mountain heathland and willow scrub merged due to functional similarity.
- Mapping unit and resolution: Minimum mapping unit 0.1 ha; raster resolution ~0.25 ha. Condatis analysis used finest feasible resolution (2 km for deciduous woodland; 1 km for all other habitats) by aggregating 50 m raster cells.
- Patch fidelity: A small area loss due to rasterization expected (mean area loss ~1.8%).
- Condatis network: Habitat cells aggregated into 1 or 2 km resolution rasters to define Condatis nodes and conductance.

## Habitats included

- Table 1 (descending area): Deciduous Woodland (wood), Heathland (heath; includes Lowland, Upland, Mountain Heaths/Willow Scrub), Blanket Bog (blbog), Coastal Floodplain Grazing Marsh (marsh), Calcareous Grassland (cgrass; includes Lowland/Upland components), Mudflats (mudfl), Salt Marsh (saltm), Lowland Meadows (lmead), Lowland Fens (lowfens), Traditional Orchard (orchard), Lowland Dry Acid Grassland (agrass), Maritime Cliff and Slope (cliff), Coastal Sand Dunes (dunes), Upland Flushes, Fens and Swamps (upfens), Purple Moor Grass and Rush Pastures (pastures), Lowland Raised Bog (lrbog), Coastal Vegetated Shingle (shingle), Reedbeds (reeds), Upland Hay Meadow (hay), Saline Lagoons (lagoons), Limestone Pavement (pavement), Calaminarian Grassland (calam).
- Notes: Heathland network comprises Lowland Heathland, Upland Heathland, Mountain Heaths and Willow Scrub. Calcareous Grassland network comprises Lowland and Upland components.

## Condatis Analysis (connectivity modelling)

- Concept: Condatis applies circuit theory to model multi-generational range expansion through a habitat network, incorporating reproduction within breeding habitat to produce successive emigrant waves.
- Nodes and links: Each habitat cell with breeding habitat is a node; resistance between cells is determined by a colonisation kernel, not by between-patch landcover; matrix outside habitat is treated as homogeneous (no breeding in non-habitat cells).
- Key equation: Colonisation rate p_i p_j R α^2 /(2π) exp(-α d_ij), where p_i, p_j are habitat areas of cells i and j, R is reproductive rate, α relates to mean dispersal distance, and d_ij is distance between cells.
- Outputs: Circuit conductance (overall network connectedness) and flow (cell-level importance to connectivity). Conductance correlates with speed of range expansion; flow indicates each habitat cell’s contribution and its vulnerability if removed.
- Differences from Circuitscape: Condatis uses a kernel-based resistance between all habitat cells (not between adjacent cells) and focuses on multi-generational spread with a homogeneous matrix; Circuitscape models are typically within-generation with a landcover-based resistance surface.

## Condatis settings and experiment design

- Habitat networks: 16 priority habitat networks analysed; three mean dispersal distances (2, 4, 8 km) to represent broad taxa across habitats.
- Reproduction and dispersal parameters: Reproductive rate fixed at R = 100 (one emigrant per hectare) and varied dispersal distance via 2/α values of 2, 4, and 8 km; this preserves relative network performance, not species-specific predictions.
- Sources and targets: Based on northward climate-shift expectations; sources along the south coast of England, targets along the northern border with Scotland (10 km raster used for input; Fig. 1 in the study shows distribution and S/T cells).
- Flow calculation and patch assignment: Condatis outputs flow across habitat cells at 1 km resolution (2 km for deciduous woodland). Patches are contiguous groups of grid cells; flow is allocated to patches proportionally to intersecting cells’ areas; flows across patches with multiple intersecting cells are summed; a geometric mean of flow across the three dispersal distances yields each patch’s flow score.
- Protection status: Patches classified as 'protected' if >50% of their area falls within protected areas (PAs); resulting dataset includes patch flow ranks and protection status across dispersal scenarios.
- Flow-based protection strategies: Three investment scenarios simulated by increasing PA coverage by 1%, 10%, and 25%—unprotected patches ranked by flow (high to low) are added to protected areas until the target protection increment is reached.

## Differences between Condatis and McRae-style circuit theory

- Node placement: McRae-style uses nodes across the whole landscape; Condatis uses nodes only in breeding habitat cells.
- Resistors: McRae uses adjacent-cell resistors; Condatis uses a pairwise colonisation kernel between all habitat cells.
- Resistance semantics: McRae resistance reflects landscape composition and movement behavior; Condatis resistance is the kernel-defined colonisation rate representing multi-generational colonisation potential.
- Current/flow interpretation: McRae current indicates movement likelihood through landscape; Condatis flow indicates the likelihood a habitat cell was used as a stepping stone in successful range expansion.

## Data structure and outputs

- Dataset composition: Five shapefiles, two CSVs, one raster, two R scripts, one Rdata file, and one text file.
- Main study data: Patchflow_all.csv (habitat network, patch ids, area, conductance stats, flow per patch, protection metrics, etc.); flow_increases.csv (flow protection increases under 1%, 10%, 25% protection scenarios).
- Demonstration data: Demonstration_code.R, demonstration coordinates (demoland.csv), demo_flows.csv, demo_hab.shp, and related demonstration data to illustrate Condatis methods.
- Figures reproduction data: figures.R and related files (source_target.tif, England.shp, protected_sites.shp, protected_patches.shp, and sample shapefiles for specific habitats).
- Patch-level fields in Patchflow_all.csv: habitat code, patch id, patch area (ha), cond_min/cond_max/cond_mean (conductance across dispersal distances), av_flow (geometric mean flow), flow_ha (flow per ha), protected_portion (protected area fraction), designated (protection status), proflow_min/proflow_max/proflow_av (proportion of total flow protected across distances).
- Flow increases data: habitat code and flow proportions for 1%, 10%, 25% protection increments.

## Quality control and reproducibility

- Data checks: Condatis results screened against floating-point arithmetic errors; any anomalies removed to ensure numerical reliability.
- Software and tools: R (v3.5.0) with rgdal and raster packages for spatial processing; references to standard geospatial and ecological modeling tools and literature.

## Key considerations and limitations

- Homogeneous matrix assumption: Condatis assumes a uniform matrix between habitat cells; relaxing this would require nested modeling that is computationally intensive.
- Spatial resolution trade-offs: Choice of 1–2 km analysis resolution balances network scope with computer memory constraints; some fine-scale patch loss is acknowledged but deemed unlikely to bias results materially.
- Interpretive scope: Results inform habitat network prioritization and protection planning rather than precise species-specific forecasts; designed to support monitoring and policy evaluation of connectivity and its protection.