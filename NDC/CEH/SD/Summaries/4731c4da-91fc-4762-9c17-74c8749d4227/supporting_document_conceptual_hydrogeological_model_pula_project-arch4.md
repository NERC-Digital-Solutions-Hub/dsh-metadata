# PULA Conceptual Hydrogeological Cross-section dataset

## Overview
- Scaled, semi-quantitative hydrogeological cross-section of the Gaborone Catchment (Botswana) in raster format at 600 dpi, plus cross-section coordinates in CSV.
- Integrates primary quantitative data (terrain elevation, geological boundaries, dip/strike, faults, water table elevation in boreholes, streams/dams/reservoirs) with qualitative interpretation (water table profile, groundwater flow directions, recharge processes, groundwater–surface water interactions, surface runoff).
- Groundwater levels reflect average conditions for 2016–2018 from Botswana Department of Water Affairs and the PULA project.
- Produced as part of the NERC-funded PULA project to assess wider impacts of extreme rainfall and flooding on water quality across surface and groundwater systems.

## Purpose and Scope
- Provides a continuous model of the catchment from upstream boundary to outlet, covering main geological units and areas with existing hydrological information (monitored wells, streams, dams, reservoirs) and geophysical data.
- Designed to support understanding of long-term groundwater response to 2016–2017 floods and spatial variability in this response.

## Data Content and Structure
- Spatial units: distances and elevations in meters; coordinates in degree-minute-second (DMS) using WGS84.
- Files included:
  - PULA_Conceptual_Cross-section_coordinates.csv: cross-section segment endpoints (A–G) with latitude and longitude.
  - PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section.png: raster cross-section image at 600 dpi.

## Methods and Workflow
- 11-step workflow:
  1) Polyline transect selection; 2) extract segment endpoints; 3) extract elevation along transect; 4) delineate surface geological units; 5) extend units and faults to depth; 6) locate surface water bodies; 7) project boreholes/wells; 8) interpolate water table across cross-section; 9) infer groundwater flow directions; 10) interpret recharge, interactions, and surface water processes; 11) export raster at 600 dpi.
- Tools used: Google Earth Pro for polyline, coordinates, elevation; Inkscape for vectorisation; aerial imagery (Maxar, CNES/Airbus, Landsat/Copernicus) for delineation; geological maps for unit boundaries and faults.
- Alluvial deposits delineated from aerial imagery; thickness derived from Botswana DWA borehole logs.
- Groundwater levels averaged across nearby boreholes when multiple were near each other; interpolation constrained by hydraulic gradients and aquifer productivity.
- Output is a vector (coordinates) and raster (cross-section) pair.

## Provenance and Data Sources
- Primary data compiled by Botswana DWA, Botswana International University of Science and Technology, and the University of Aberdeen.
- Uses published geological maps (e.g., Pre-Kalahari maps; Botswana national maps) and groundwater/quality data from the PULA project and DWA.
- References and data sources are listed in Table 1 (including authors and publication years) and linked to supporting groundwater and hydrogeology studies.

## Quality and Limitations
- Quality control: Not applicable within the dataset; relies on pre-existing, quality-controlled sources.
- Assumptions and adjustments:
  - Faults and dykes treated as vertical due to limited data on dip angles.
  - Boundaries occasionally adjusted to align with high-resolution imagery.
  - Dip/strike information extrapolated to depth based on surrounding units.
  - Alluvial thicknesses based on borehole logs where mapped data were absent.
- Indicates spatial interpolation constrained by known hydraulic gradients and aquifer productivity.

## Data Access and File Details
- Two data files:
  - CSV: PULA_Conceptual_Cross-section_coordinates.csv containing cross-section point identifiers (A–G) and their lat/long coordinates.
  - PNG: PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section.png as the raster cross-section.
- Units and coordinate formats clearly documented in the dataset.

## Use and Applications
- Supports assessment of groundwater response to extreme rainfall and floods and related water quality implications.
- Provides a framework for understanding groundwater–surface water interactions, recharge processes, and spatial variability across a heterogeneous catchment.
- Useful for researchers and policymakers involved in water resources management, hydrogeology planning, and environmental impact studies.