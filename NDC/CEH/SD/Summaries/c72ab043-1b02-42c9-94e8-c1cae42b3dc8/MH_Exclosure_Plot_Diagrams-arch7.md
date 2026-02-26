# Plot layout at Little Dun Fell

- Overview
  - Describes spatial layout and sampling design for vegetation study across multiple sites, focusing on grid-based plots, quadrats, transects, and marker posts. Includes references to grazed and enclosed plots and to a Juncus squarrosus grassland layout.

- Spatial design and components
  - Plot grid and boundaries:
    - 10 by 6 plots identified by corner posts and grid references.
    - Plots are gridded into quadrats (approximately 18 quadrats per plot according to the description).
  - Quadrats and sampling:
    - In the Hill study area, 40 quadrats are randomly chosen within grazed enclosed plots.
    - Layout uses subdivided plots into 10 transects, each with 10 frame positions for point quadrat studies.
  - Site features:
    - Regions described include Little Dun Fell, Troutbeckhead, Hill area, bogs, and a Juncus squarrosus grassland plot (Jl).
    - Some diagrams are noted as not to scale (e.g., Hill study).

- Data collection design and workflow
  - The sampling layout is designed to be implemented across both grazed and enclosed plots, with a consistent grid-based framework to support spatial analysis.
  - Marker posts and enclosure edges are part of the mapped features to delineate study boundaries.

- GIS data products and schema inferences
  - Suggested spatial layers:
    - Plot polygons (10 x 6 grid).
    - Quadrat polygons (per plot, based on the grid).
    - Transect lines (10 per plot, subdividing each plot).
    - Frame-position points (10 per transect for point quadrat measurements).
    - Marker posts and enclosure boundary lines.
  - Suggested attributes:
    - Site/area name, plot_id, quadrat_id, transect_id, frame_number, sampling_type, and any vegetation metrics collected.
  - Alignment and integration:
    - Layouts reference multiple sites; ensure consistent coordinate reference system and alignment across plots and sites for integrated GIS analyses.

- Notes and considerations
  - Some figures are described as not to scale, indicating the need for field verification when converting to spatial data.
  - The document emphasizes a grid-based, repeatable sampling framework across grazed vs enclosed plots and across different habitat types (e.g., Juncus grassland, bogs).