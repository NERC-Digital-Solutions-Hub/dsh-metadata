# Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

- Purpose and context
  - Presents methods and data used to evaluate national-scale, long-distance connectivity for England’s Priority Habitat Inventory (PHI) and its protection.
  - Aims to inform monitoring decisions and policy evaluations by linking habitat connectivity to protection status and potential management actions.

- Data sources and preparation
  - Spatial data: PHI, Sites of Special Scientific Interest (SSSIs), and National Nature Reserves (NNRs) from Natural England Open Data Geoportal; England boundaries from OS OpenData Boundary-Line.
  - PHI originally vector; converted to 50 m raster by assigning each cell the habitat type of the polygon centroid. When cells intersect multiple habitats, the rarest habitat type is kept.
  - Habitat merges for functional similarity: upland/lowland calcareous grassland; upland/heath/moorland types; mean area loss from rasterization ~1.8%.
  - Condatis requires finer analysis resolution; raster aggregated to 1–2 km depending on habitat type (2 km for deciduous woodland; 1 km for others) to manage RAM constraints.
  - Habitats analyzed: 16 priority habitat networks (e.g., deciduous woodland, heathland, blanket bog, coastal marsh, calcareous grassland, etc.).
  - Data processing tools: R 3.5.0 with rgdal and raster packages; aggregation converts 50 m cells to proportional cover.

- Condatis analysis (connectivity modeling)
  - Condatis adapts circuit theory to model multi-generational range expansion, incorporating reproduction within breeding habitat to simulate successive waves of dispersal.
  - Network representation: each breeding habitat cell is a node; colonisation resistance between cells i and j is derived from a kernel-based dispersal model.
  - Key formula: colonisation rate p_i p_j R α^2/(2π) exp(-α d_ij); p = habitat area per cell, R = reproductive rate, d_ij = distance.
  - Matrix outside breeding habitat is treated as homogeneous (dispersal through non-breeding cells is not explicitly modeled).
  - Outputs: 
    - Conductance (network-level connectedness) correlates with speed of range expansion.
    - Flow (per-cell importance) indicates each habitat cell’s contribution to connectivity and potential impact of its loss.
  - Limitations: does not model physical barriers explicitly (unlike Circuitscape); relies on a homogeneous matrix and a population-level colonisation kernel for tractability across large networks.

- Model setup and scenarios
  - Networks and dispersal settings
    - 16 priority habitat networks analyzed; three exemplar mean dispersal distances: 2, 4, 8 km (to span a range of taxa; not species-specific).
    - Reproductive rate fixed at R = 100 (one emigrant per hectare); chosen to be plausible for various taxa; changing R scales all flows proportionally and does not affect network ranking.
    - Sources and targets: along the south coast of England (sources) and northern England/Scotland border (targets) to mirror northward range shifts under climate change.
  - Patch flow and protection assignment
    - Flow calculated on a 1 km (and 2 km for deciduous woodland) raster; habitat patches defined as contiguous grid-cell clusters (edge/vertex connected).
    - Flow assignment to patches: flow of intersecting cells apportioned to patches by area; patches crossing multiple habitat cells accumulate flow.
    - Patch ranking: patches are ranked by a geometric average of flow across the three dispersal distances (flow rank).
    - Protection status: patches classified as 'protected' if >50% of their area lies within Protected Areas (PAs).
  - Flow-led protection investment (scenario analysis)
    - Three protection investment levels simulated: 1%, 10%, and 25% increases in PA-covered area.
    - Unprotected patches ranked by flow (highest first) and added to PAs until targets for each investment level are met.
    - Purpose: assess how prioritizing high-flow patches affects overall connectivity protection.
  - Outputs and data products
    - Flow raster outputs per habitat network and dispersal distance.
    - Patch-level data: flow, area, protection status, and flow-based importance metrics.
    - Datasets capturing increases in protected flow under flow-led patch selection.

- Data structure and reproducibility
  - Delivered as five shapefiles, two CSVs, one raster, two R scripts, one Rdata, and one text file.
  - Data categories
    - Study data: Patchflow_all.csv; flow and conductance results; flow_increases.csv.
    - Demonstration/data for method replication: Demonstration_code.R; demonstration coordinates; demo_flows.csv; demo_hab.shp; spatial demonstrations and area in hectares.
    - Reproducing figures: figures.R; source_target.tif; England.shp; protected_sites.shp; protected_patches.shp; lfens_sample.shp; cagra_sample.shp; README.txt with file descriptions.
  - Patchflow_all.csv fields of note: habitat code, patch id (p_id), patch area (ha), cond_min/cond_max/cond_mean (conductance across dispersal distances), av_flow (geometric mean flow), flow_ha, protected_portion, designated (protection flag), proflow_min/max/av (proportion of network flow protected across distances).
  - Quality control: checks for floating-point arithmetic errors; problematic results removed.

- Practical implications for monitoring frameworks
  - Provides measurable connectivity metrics (conductance and flow) that can inform where monitoring and protective actions are most impactful.
  - Identifies high-flow patches as priority targets for protection expansion and policy interventions.
  - Enables scenario analysis to test how incremental protection (1%, 10%, 25%) could improve network connectivity.
  - Produces reproducible data products that can be updated with new PA data or habitat information to track changes over time.

- Assumptions, limitations, and governance considerations
  - Assumptions
    - Matrix between habitat cells is homogeneous; does not incorporate landscape barriers directly.
    - Dispersal modeled via a general kernel rather than species-specific movement paths.
  - Limitations
    - Potential loss of small habitat patches in rasterization (mean ~1.8% area loss).
    - Computational constraints necessitated coarser resolutions for large habitat networks.
  - Governance and data sharing
    - Emphasizes openness by sharing underlying data and methods; notes data governance considerations such as metadata quality and data sharing as practical barriers in monitoring.
    - Data sources are public (Natural England, OS); analyses rely on transparent, reproducible workflows (R-based).

- References and sources
  - Core methodological and data references include Hodgson et al. (2012, 2016), McRae et al. (2008), Lenoir et al. (2020), Natural England Open Data, Ordnance Survey, and standard geospatial R packages (rgdal, raster).