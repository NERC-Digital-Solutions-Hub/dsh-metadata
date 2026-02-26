# Supporting Information for Evaluation of national scale, long-distance connectivity (and its protection) in England's priority habitat inventory

- Data preparation
  - Inputs: Priority Habitat Inventory (PHI), Sites of Special Scientific Interest (SSSIs) and National Nature Reserves (NNRs) for England; England boundary polygons from OS OpenData Boundary-Line.
  - PHI originally vector; converted to 50 m raster in ArcMap 10.6. Each 50 m cell assigned the habitat type of the intersecting polygon’s centroid; if a cell overlapped multiple habitat types, the rarest type was chosen.
  - Habitat merging: combined upland and lowland calcareous grassland; combined upland heathland, lowland heathland, and mountain heathland with Willow Scrub.
  - Rasterization details: minimum mapping unit 0.1 ha; raster cell ~0.25 ha; estimated mean area loss due to rasterization ~1.8%.
  - Condatis analysis resolution: to balance network size and RAM, 2 km for deciduous woodland and 1 km for all other habitats; 50 m raster aggregated to these resolutions to produce proportional habitat cover per cell using R packages rgdal and raster (R 3.5.0).
  - Habitat networks: 16 priority habitat networks with listed habitats and their total areas (e.g., Deciduous Woodland, Heathland, Blanket Bog, etc.).

- Condatis analysis overview
  - Purpose: model multigenerational, long-distance range expansion through habitat networks; used as a conservation decision support tool.
  - Network construction: each breeding habitat cell is a node; resistance between nodes i and j derived from a colonisation kernel (Equation 1) using habitat area and mean dispersal distance; matrix outside breeding habitat is homogeneous and not part of the calculation.
  - Key metrics: circuit conductance (overall network connectivity; correlates with speed of range expansion) and flow (cell-level importance to connectivity).
  - Computation framework: Kirchhoff’s and Ohm’s laws applied to the resistor network; current through cells indicates relative importance.
  - Sources and targets: sources along the south coast of England; targets along the northern border with Scotland (10 km raster used to place S and T).
  - Dispersal scenarios: three exemplar mean dispersal distances corresponding to 2, 4, and 8 km (represented as 2/α in Equation 1); reproductive rate R fixed at 100 (one emigrant per hectare). This setup focuses on network-level patterns rather than species-specific predictions.
  - Patch-flow and protection assignment: flow outputs at 1 km resolution (2 km for deciduous woodland); habitat patches defined as contiguous cells; flow attributed proportionally to patches intersecting one or more habitat cells; patches intersecting multiple cells have flows summed; patches intersecting multiple patches have flows divided by patch areas; patch flow averaged geometrically across the three dispersal distances; patches classified as 'protected' if >50% of their area lies within protected areas (PAs).
  - Flow-led protection analysis: three investment scenarios increasing protected habitat by 1%, 10%, and 25% by ranking unprotected patches by flow (highest flow first) and adding until the target protection increase is achieved.

- Data handling and outputs
  - Data structure: five shapefiles, two CSVs, one raster, two R scripts, one Rdata file, and one text file.
  - Categories of files:
    - Study data: patchflow_all.csv, flow and conductance data, flow_increases.csv (increases in protected flow due to flow-led protection).
    - Demonstration files: demonstration_code.R, demo_land coordinates, demo_flows.csv, demo_hab.shp, associated demonstration data.
    - Figures/reproduction: figures.R, source_target.tif (locations of sources/targets), England.shp, protected_sites.shp, protected_patches.shp, lfens_sample.shp, cagra_sample.shp, README.txt with file descriptions.
  - Patchflow_all.csv fields: habitat code, patch ID, patch area (ha), cond_min/cond_max/cond_mean (conductance across dispersal distances), av_flow (average patch flow), flow_ha (flow per ha), protected_portion (proportion of patch covered by protected areas), designated (1 protected, 0 not), proflow_min/proflow_max/proflow_av (min/max/avg proportion of network flow protected across distances).
  - Flow_increases.csv fields: habitat code, 1/10/25 (levels of additional protected flow achieved by adding patches, with corresponding flow values).

- Quality control
  - Condatis results checked for floating-point arithmetic issues; any errors removed as needed.

- Differences from other circuit theory approaches
  - Condatis uses habitat cells as nodes and a kernel-based resistance between all node pairs, rather than a surface-based resistance between adjacent cells.
  - It models multi-generational dispersal rather than within-generation movement; the landscape between patches is assumed homogeneous (no explicit barriers in the matrix).
  - Outputs emphasize lineage-based patch colonisation probability (flow) and network-wide conductance rather than current through a broad landscape network.
  - Potential future enhancements could incorporate matrix complexities by nesting models (computationally intensive).

- References and software context
  - Key references for Condatis and related methods, plus software tools (rgdal, raster) and foundational circuit theory work.
  - Tools used: ArcMap 10.6 for rasterization, R 3.5.0 with rgdal and raster packages for raster aggregation and analysis.