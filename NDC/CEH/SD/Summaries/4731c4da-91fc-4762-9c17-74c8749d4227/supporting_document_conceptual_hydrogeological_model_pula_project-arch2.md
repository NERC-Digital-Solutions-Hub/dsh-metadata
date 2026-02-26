# A brief description/overview of the data being described

## Overview
- The PULA Conceptual Hydrogeological Cross-section dataset provides a scaled, semi-quantitative hydrogeological cross-section of the Gaborone Catchment (Botswana) in a 600 dpi raster and accompanying geographic coordinates (numerical). 
- It combines primary quantitative data (terrain elevation; geological unit boundaries and dip/strike; regional faults and dykes; borehole water table elevations; locations of streams, dams, and reservoirs) with qualitative interpretations (water table profile and hydraulic gradients; groundwater flow direction; recharge processes; groundwater–surface water interactions; surface runoff).

## Purpose and scope
- Aimed at understanding the long-term groundwater response to the 2016–2017 floods in terms of water level and basic physicochemical parameters, and spatial variability in this response.
- Part of the NERC-funded PULA project to evaluate broader impacts of extreme rainfall/flooding on water quality across surface and groundwater systems in a physiographically variable region.
- The cross-section is selected to provide a continuous model from upstream boundary to the outlet, covering main geological units and areas with existing hydrological information.

## Data sources and provenance
- Primary datasets compiled by scientists and students from the Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.
- Groundwater levels reflect 2016–2018 averages reported by the Botswana DWA and the PULA project (Petros and Comte 2021; see Table 1).
- Uses published geological maps (e.g., Pre-Kalahari, Botswana national maps) and DWA borehole data; information integrated to define hydrogeological units, faults, and surface water features.

## Methodology and workflow
- Steps 1–3: Polyline transect selection; extract end coordinates; derive topography along the transect using Google Earth Pro; vectorise in Inkscape.
- Steps 4–6: Delineate geological unit boundaries and regional faults; extend units and faults at depth; identify surface water bodies. Dipping angles for faults/dykes assumed vertical where data are lacking.
- Steps 7–9: Project boreholes onto the transect; average water levels when multiple wells near the same unit; interpolate the water table across the cross-section; infer groundwater flow directions from gradients and geology.
- Step 10: Integrate water table profile, DWA monitoring data, and PULA groundwater/quality data to interpret processes.
- Step 11: Export final raster image at 600 dpi.
- Tools and imagery: Google Earth Pro; Maxar/ CNES-Airbus imagery; Landsat/Copernicus; Inkscape for vector-to-raster workflow.
- Outputs: two files
  - CSV: PULA_Conceptual_Cross-section_coordinates.csv (A–G points with lat/lon in WGS84)
  - PNG: PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section (raster cross-section)

## Data structure and units
- Spatial units: meters for distance and elevation.
- Distances measured from the western end of the cross-section; elevations in absolute levels.
- Geographic coordinates: degree–minute–second (DMS) in the WGS84 system.
- File contents
  - Cross-section coordinates CSV: three columns (points A–G; latitude; longitude).
  - Cross-section image PNG: raster representation of the cross-section.

## Quality and limitations
- Quality control: described as not applicable; based on available, quality-controlled information.
- Limitations and assumptions
  - Fault/dyke dipping angles are assumed vertical due to data gaps.
  - Alluvial deposits delineated from aerial imagery due to lack of mapped detail.
  - Water table values averaged across nearby wells when multiple boreholes are near the same unit.
  - Interpolation constrained by hydraulic gradients and aquifer productivity.
- Data provenance relies on published geological maps and DWA datasets, which underpin the conceptual interpretation.

## Relevance for monitoring and policy
- Provides an integrated, repeatable framework for monitoring groundwater behavior in response to extreme rainfall/flood events.
- Supports assessment of groundwater–surface water interactions, recharge processes, and spatial variability across a catchment with diverse geology and land use.
- Uses standard, accessible tools and yields clearly formatted outputs (coordinates and a raster cross-section) suitable for inclusion in environmental monitoring portals and downstream analyses.