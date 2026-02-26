# The PULA Conceptual Hydrogeological Cross-section dataset

## Overview
- A scaled, semi-quantitative hydrogeological cross-section of the Gaborone Catchment (Botswana) provided as a 600 dpi raster image plus cross-section geographic coordinates in a CSV.
- Combines primary quantitative data (terrain elevation, geological boundaries and dip/strike, regional faults and dykes, borehole water table elevations, surface water bodies) with qualitative interpretation (water-table profile and hydraulic gradients, groundwater flow directions, recharge processes, groundwater–surface water interactions, surface runoff).
- Groundwater levels reflect average conditions for 2016–2018, sourced from the Botswana Department of Water Affairs and the PULA project.
- Produced by a collaboration among the Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.
- Purpose: understand the long-term groundwater response to the 2016–2017 floods and assess broader impacts of extreme rainfall and flooding on water quality across surface and groundwater bodies in a varied physiographical region.

## Contents and data structure
- Two data files:
  - PULA_Conceptual_Cross-section_coordinates.csv (CSV): 3 columns (point name A–G, latitude, longitude in degree-minute-second, header row included).
  - PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section.png (PNG): raster image of the cross-section at 600 dpi.
- Spatial units: distances and elevations in meters; coordinates in degrees/minutes/seconds (DMS) using the WGS84 system.

## Methodology and workflow
- Eleven-step workflow to generate the cross-section:
  1) Select polyline transect
  2) Extract segment end coordinates
  3) Retrieve topography along the transect
  4) Delineate surface geological units and regional faults
  5) Extend geological units and faults to depth
  6) Locate surface water bodies (streams, reservoirs, dams)
  7) Project monitoring boreholes and delineate water table
  8) Interpolate water table across the cross-section
  9) Infer groundwater flow directions
  10) Interpret recharge, runoff, and groundwater–surface water interactions
  11) Export the final raster at 600 dpi
- Tools and data sources:
  - Steps 1–3: Google Earth Pro with 2022 imagery; elevation profiles generated and vectorised in Inkscape.
  - Steps 4–6: Google Earth Pro and published geological maps; boundaries and faults mapped, with depth extrapolation of geology.
  - Step 7–9: Borehole data from Botswana DWA and PULA groundwater data; temporal/spatial averaging for nearby wells; interpolation guided by hydraulic gradients and aquifer productivity.
  - Step 10: Integrated analysis using time-series groundwater data and water quality data from PULA and DWA.
  - Step 11: Raster export in Inkscape.

## Provenance and sources
- Uses published primary maps and datasets to construct the cross-section, including:
  - Pre-Kalahari geological maps of Botswana (various editions and publishers)
  - The Pre-Kalahari Geological Map of the Republic of Botswana
  - The 1998 edition of the National Map of Botswana
  - Evolution of an Archaean intracratonic basin (transferred context)
  - Botswana groundwater atlas and African groundwater maps guides
  - Groundwater resources quality data following extreme rainfall and floods (NERC datasets)
  - Groundwater monitoring data following 2016–2017 extreme rainfall and floods in the Gaborone catchment
- References cited include works by Mathule et al., Key et al., Franchi & Mapeo, Comte et al., O’Dochartaigh, Petros & Comte (specific years and reports as listed in the dataset documentation).

## Spatial and temporal scope
- Spatial: Gaborone Catchment, Botswana; cross-section designed to span from upstream boundary to outlet, incorporating main geological units and hydrological features.
- Temporal: groundwater levels reflect 2016–2018 averages; imagery and maps used span multiple years (including 2022 imagery for topography and earlier geological maps); supplementary groundwater and water-quality data referenced from 2019–2021 publications.

## Quality, limitations, and assumptions
- Quality control: Not applicable within the dataset itself; relies on data that are already quality-controlled from original sources.
- Limitations and assumptions:
  - Some fault and dyke dips are not known; dip angles for faults and dykes were assumed vertical where data were lacking.
  - Alluvial formations not mapped in the geological maps were delineated from aerial imagery, with thickness inferred from borehole logs.
  - Water-table interpolation constrained by hydraulic gradients and known aquifer productivity.
  - Cross-section is semi-quantitative and meant to provide a continuous model rather than a fully instrumented dataset.

## Usage, applicability, and accessibility
- Intended to enable data exploration and self-serve analysis for stakeholders studying groundwater response to extreme rainfall events.
- Useful for researchers, policymakers, and water managers focusing on groundwater behavior, recharge processes, groundwater–surface water interactions, and water quality implications in heterogeneous catchments.
- Accessible data components:
  - A coordinate CSV with point designations and geolocations
  - A high-resolution raster cross-section PNG
- Coordinate system and units are clearly defined (WGS84, DMS for coordinates, meters for distances/elevations).