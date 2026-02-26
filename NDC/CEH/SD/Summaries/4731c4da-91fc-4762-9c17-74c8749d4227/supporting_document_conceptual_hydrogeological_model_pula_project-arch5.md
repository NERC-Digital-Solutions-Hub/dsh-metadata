# PULA Conceptual Hydrogeological Cross-section dataset

## Overview
- Conceptual hydrogeological cross-section for the Gaborone Catchment, Botswana.
- Contains a scaled, semi-quantitative cross-section in raster form (600 dpi) and the accompanying cross-section coordinates.
- Combines primary quantitative data (terrain elevation, geological boundaries and dips/strikes, faults/dykes, water table from boreholes, surface water bodies) with qualitative interpretation (water table profile, hydraulic gradients, groundwater flow, recharge, groundwater-surface water interactions, surface run-off).
- Groundwater levels reflect 2016–2018 averages from the Botswana Department of Water Affairs and the PULA project, created to study groundwater response to the 2016–2017 floods and broader impacts of extreme rainfall on water quality.

## Data composition and scope
- Two data files:
  - PULA_Conceptual_Cross-section_coordinates.csv (cross-section coordinates; 3 columns: point name A–G, latitude, longitude in degree-minute-second; WGS84)
  - PULA_Gaborone_catchment_conceptual_hydrogeological_cross-section.png (raster conceptual cross-section)
- Spatial units: distances and elevations in meters; coordinates in degrees minutes seconds (WGS84).
- Purpose: provide a continuous catchment model from upstream boundary to outlet, covering major geological units and hydrological features with existing data (monitored wells, streams, dams).

## Data provenance and workflow (collected, generated, and transformed data)
- Primary data sources include terrain elevation, geological maps, regional faults, hydrological features, borehole water levels, and groundwater quality data.
- Groundwater level data for 2016–2018 compiled from Botswana DWA and PULA project data.
- Team composition: Botswana DWA, Botswana International University of Science and Technology, and the University of Aberdeen; the same team performed synthesis and modeling.
- Workflow steps (summary):
  - Define transect, extract coordinates, and derive topography along the transect (Google Earth Pro; Inkscape for vectorisation).
  - Delineate surface geology, extend units/faults with depth, locate surface water bodies (Google Earth imagery; published geological maps; maps georeferenced/reprojected).
  - Extrapolate geology depth, assign dipping/strike; infer alluvial deposits from imagery; thickness from borehole logs.
  - Project boreholes/wells near the transect, average levels when multiple nearby, interpolate water table with hydraulic-gradient constraints, infer groundwater flow directions.
  - Integrate water table profile, DWA timeseries, and PULA groundwater/water quality data for interpretation.
  - Export final raster image at 600 dpi.
- Tools mentioned: Google Earth Pro, Inkscape; referenced maps/datasets from published geological sources.

## Data quality and governance
- Quality control note: Not applicable for this dataset; relies on pre-quality-controlled, existing information.
- Provenance emphasis: multiple authoritative sources and datasets used; cross-section built from both quantitative measurements and qualitative interpretation.
- Metadata indicators:
  - Timeframe for groundwater data: 2016–2018.
  - Cross-section intended to reflect long-term groundwater response to flooding and interaction with surface water processes.
  - Documented processing steps and data sources support reproducibility.

## Governance, accessibility, and interoperability
- Data structure supports discoverability and reuse: explicit file names, formats (CSV and PNG), and coordinate system (WGS84).
- Interoperability considerations:
  - Mixed data formats (vector coordinates with a raster image) and geospatial references require GIS software to integrate.
  - Some assumptions (e.g., vertical faults/dykes due to limited dip data) acknowledged for transparency and future updates.
- Reuse considerations:
  - Useful for groundwater and hydrogeological modeling, flood impact assessments, and regional water quality studies within the PULA project framework.
  - Appropriate citation of primary data sources (DWA, PULA, and referenced scientific reports) is advised.

## Limitations and caveats
- Some geological features (faults/dykes) assumed vertical due to data gaps; actual dips may differ.
- Alluvial thicknesses derived from borehole logs where mapped data were absent.
- Uses aggregated groundwater levels (2016–2018) and may not capture more recent variations.
- Quality assurance relies on the integrity of underlying datasets and published maps.

## Context and references
- Part of the NERC-funded PULA project, examining extreme rainfall/flood impacts on surface and groundwater across a region with variable physiography.
- Data sources include Botswana DWA groundwater monitoring datasets and published geological maps (various 1997–2019 references) used to construct the cross-section.