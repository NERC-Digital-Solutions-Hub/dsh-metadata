# A brief description/overview of the data being described

## Overview
- PULA Conceptual Hydrogeological Cross-section dataset for the Gaborone Catchment, Botswana.
- Contains a raster cross-section at 600 dpi plus geographic coordinates in CSV.
- Combines primary quantitative data (terrain elevation, geological boundaries, dip/strike, faults, water table elevations, streams/dams/reservoirs) with qualitative interpretation (groundwater flow directions, recharge, groundwater-surface water interactions, surface run-off).
- Groundwater water level data reflect 2016–2018 averages from Botswana Department of Water Affairs and the PULA project.
- Developed by a team from the Botswana DWA, BIUST, and the University of Aberdeen.
- Created to understand long-term groundwater response to the 2016–2017 floods and to evaluate broader impacts of extreme rainfall/floods on water quality, within a region with varied geology and land use.
- Cross-section is designed to be a continuous model from upstream boundary to outlet, covering main geological units and monitoring/hydrological features.

## Data content and structure
- Two data files: a CSV of cross-section coordinates and a PNG raster cross-section image.
  - PULA_Conceptual_Cross-section_coordinates.csv: 3 columns plus a header row; includes cross-section segment endpoints labeled A–G, with latitude and longitude in degree-minute-second (DMS).
  - PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section.png: raster image of the cross-section.
- Spatial units: distances and elevations in meters; coordinates in WGS84 (DMS).
- Metadata context: tied to groundwater levels and water quality data from the PULA project and DWA datasets.

## Collection/Transformation workflow (steps)
- Step 1–3: Polyline transect selection, extraction of segment endpoints, extraction of elevation profile; tools include Google Earth Pro, Ruler/Path, Placemark, Elevation Profile, and Inkscape for vectorisation.
- Step 4–6: Delineation of geological unit boundaries and regional faults; extend units and faults to depth; locate surface water bodies; use combined Google Earth imagery and published geological maps; adjust boundaries to imagery; delineate alluvial deposits from aerial imagery; derive alluvial thickness from borehole logs.
- Step 7–9: Project nearby boreholes/wells onto the transect; average water levels within close wells/well fields; interpolate water table across the cross-section under hydraulic gradient constraints; infer groundwater flow directions from gradients and geology.
- Step 10: Integrate water table timeseries, DWA groundwater data, and PULA groundwater/water quality data to interpret groundwater behavior.
- Step 11: Export the final vector drawing as a 600 dpi raster image.

## Data sources and provenance
- Primary maps/datasets used include:
  - Pre-Kalahari geological maps (South Sheet; 1:1,000,000)
  - The Pre-Kalahari Geological map of Botswana (1:1,500,000)
  - The 1998 National Map of Botswana
  - Evolution of the Archaean intracratonic basin (Transvaal Supergroup)
  - Botswana groundwater atlas and related resources
- Supporting datasets:
  - Groundwater monitoring data after 2016–2017 extreme rainfall/floods (Petros & Comte 2021)
  - Water resources quality data following extreme rainfall/floods (Comte, Geris, Franchi 2019)
  - NERC Environmental Information Data Centre references
- Development team includes personnel from the Botswana DWA, BIUST, and the University of Aberdeen.

## Purpose and context
- Aim to understand long-term groundwater response to major floods (2016–2017) in terms of water levels and basic physicochemical parameters, and to assess spatial variability in response due to geology and land use.
- Part of the NERC-funded PULA project to evaluate broader impacts of extreme rainfall/floods on water quality across surface and groundwater bodies in a geologically diverse region.
- Cross-section chosen to provide a continuous model from upstream to outlet, incorporating main geological units and existing hydrological information (monitored wells, streams, dams, reservoirs).

## Units, metadata, and quality
- Units: distances and elevations in meters; geographic coordinates in DMS (WGS84).
- Data quality control: Not applicable for new QC; relies on already quality-controlled information and published sources.
- Metadata considerations: dataset integrates both quantitative measurements and qualitative interpretation; provenance and methods are documented to support transparency and reuse.

## Data governance and sharing (implications for monitoring frameworks)
- Emphasizes integration of multiple data sources and transparent methodology to support monitoring decisions.
- Highlights challenges identified in monitoring contexts: data availability, metadata completeness, and alignment between disparate data sources; indicates a need to document data provenance and maintain linkage to source datasets (e.g., DWA, geological maps, and groundwater-quality datasets).
- Demonstrates a workflow-oriented approach to constructing a governance-friendly, interpretable cross-section that can inform policy decisions and future monitoring (e.g., addressing gaps identified in data and metadata).