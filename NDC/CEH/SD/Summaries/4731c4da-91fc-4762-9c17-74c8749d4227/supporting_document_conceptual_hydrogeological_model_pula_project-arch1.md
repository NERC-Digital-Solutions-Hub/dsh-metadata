# PULA Conceptual Hydrogeological Cross-section dataset

- The PULA Conceptual Hydrogeological Cross-section dataset provides a scaled, semi-quantitative hydrogeological cross-section of the Gaborone Catchment, Botswana, in a raster image at 600 dpi, with accompanying cross-section geographic coordinates in CSV.
- It combines quantitative data (terrain elevation, geological unit boundaries with dip/strike, regional faults and dykes, water table elevations in boreholes, locations of streams, dams, and reservoirs) with qualitative interpretation (water table profile, hydraulic gradients, groundwater flow directions, recharge processes, groundwater–surface water interactions, and surface runoff).
- Groundwater level data reflect average conditions for 2016–2018, sourced from the Botswana Department of Water Affairs and the PULA project.

- Purpose and scope
  - Designed to understand the long-term groundwater response to the 2016–2017 floods in terms of water level and basic physicochemical parameters, and to assess spatial variability in this response.
  - Part of the NERC-funded PULA project evaluating broader impacts of extreme rainfall and flooding on water quality across surface and groundwater in a region with diverse physiography (geology, land use).

- Cross-section coverage
  - Selected to provide a continuous model from upstream boundary to the catchment outlet, encompassing major geological units and areas with existing hydrological information (monitored well fields, streams, dams, reservoirs) and geophysical information.

- Data collection and transformation workflow (11 steps)
  - (1–3) Polyline transect selection, extraction of end coordinates, and topography along the transect using Google Earth Pro; elevation profile generated and vectorised in Inkscape.
  - (4–6) Delineation of geological unit boundaries and regional faults at the surface, extrapolation of units/faults at depth, and identification of surface water bodies (streams, reservoirs, dams) using Google Earth imagery and published geological maps; alluvial deposits delineated from aerial imagery with thickness from borehole logs.
  - (7–9) Projection of nearby boreholes/wells onto the transect; spatial/temporal averaging of closely located wells; interpolation of water table across the cross-section constrained by hydraulic gradients; inference of groundwater flow directions from gradients, geological structure, and recharge/discharge indicators.
  - (10) Integrated interpretation using the water table profile, DWA groundwater monitoring data, and PULA groundwater and water-quality data.
  - (11) Export of the final vector cross-section as a 600 dpi raster image.

- Data sources and supporting maps
  - Uses published primary maps and datasets (e.g., Pre-Kalahari geological maps, Botswana National Map, and other regional hydrogeology references) as part of constructing the conceptual cross-section.

- Data products and structure
  - Two files are provided:
    - PULA_Conceptual_Cross-section_coordinates.csv: contains cross-section point coordinates with three columns (point names A–G, latitude, longitude) in WGS84.
    - PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section.png: raster image of the cross-section at 600 dpi.

- Units and geography
  - Spatial units: meters for distances and elevations; elevations are absolute values from Google Earth.
  - Geographic coordinates: degrees, minutes, seconds (DMS) in WGS84.

- Quality control and limitations
  - Quality control is not explicitly applicable; based on available, quality-controlled information.
  - Assumptions and uncertainties include:
    - Fault and dyke dipping angles assumed vertical due to lack of data.
    - Delineation of alluvial deposits relies on aerial imagery; thickness estimates come from borehole logs.
    - Interpolation of water table constrained by hydraulic gradients and aquifer productivity; averaging across nearby wells when multiple wells are near each other.
    - Boundaries and features adjusted to align with high-resolution imagery.

- Provenance and contributors
  - Collected and synthesized by a team from the Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.
  - Part of the NERC-funded PULA project to analyze the impacts of extreme rainfall and floods on groundwater and surface water quality.