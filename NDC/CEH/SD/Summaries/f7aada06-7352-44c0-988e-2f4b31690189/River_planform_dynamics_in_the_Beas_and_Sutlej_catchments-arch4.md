# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system

## Overview
- Describes and analyzes a dataset linked to the study by Vercruysse and Grabowski (2021), which evaluates human impacts on river planform dynamics in the Himalayan Sutlej-Beas system.
- Aims to systematically assess changes in river planform across centennial, annual, seasonal, and episodic timescales; link observed patterns to human–environment drivers; and conceptualize geomorphic changes as timescale-dependent evolutionary trajectories.
- Core dataset elements cover post-monsoon wet river area, active gravel bars, active channel area, active channel width, historic channel width, and anabranching index.
- Spatial-temporal scope focuses on Beas and Sutlej rivers, 1989–2018, with river reaches defined as Reach 1 (below dams) and Reach 2 (plains). Reach 2 is further subdivided into multiple sections.

## Data products and formats
- Delivered primarily as ESRI Shapefiles with associated mandatory and optional files, plus csv files for key metrics.
- Main data types:
  - Wet river area (annual, post-monsoon 1989–2018)
  - Active gravel bars (annual, post-monsoon 1989–2018)
  - Active channel area (maximum extent 1989–2018)
  - Active channel width (annual 1989–2018)
  - Historic channel width (1847–1850)
  - Anabranching index (annual 1989–2018)
- Coordinate system: WGS84.
- File groups and key outputs include:
  - Wet river area shapefiles for Beas and Sutlej
  - Active gravel bars shapefile
  - Active channel area shapefiles for Beas and Sutlej
  - Active channel width shapefiles for Beas and Sutlej
  - Historic width shapefiles (1847)
  - Metrics CSVs for Beas and Sutlej plus a reaches/sections shapefile

## Variables, measurements, and methods
- Wet river area: derived from Landsat 5–8 imagery (1989–2018) using post-monsoon mNDWI threshold (>0.15); manual editing then polygon conversion.
- Active gravel bars: identified by high red reflectance (>0.16) in post-monsoon Landsat images; within buffers defined by maximum wet-area extent.
- Active channel area: created by aggregating annual wet-area shapefiles (1989–2018) to define the multi-year wetted extent.
- Active channel width: measured as the width of the wet area (including enclosed gravel bars), computed automatically every 2 km; also derived from the 1847 map (The Trans-Sutluj Division) for historical width; widths measured perpendicular to the riverbanks; mean values calculated by reach/section.
- Anabranching index (AI): quantifies the number of active channels separated by bars/islands across at least 10 cross sections; computed for each reach/section.
- Data provenance and methods are detailed in the associated paper (Vercruysse & Grabowski, 2021) and referenced methodological sources.

## Spatial extent and reach definitions
- Beas River: Pong Dam to confluence with Sutlej.
- Sutlej River: Bhakra Dam to confluence with Beas.
- Reaches: Reach 1 (downstream of dams) and Reach 2 (plains); Reach 2 subdivided into 4 Beas sections and 5 Sutlej sections.
- Data definitions and reach/section topology are provided in the Metrics shapefile.

## Data quality and validation
- Landsat-based observations supplemented by quality assessment bands to select cloud-free imagery.
- Processing included project-team-led steps with spot validation against aerial photography.
- Quality checks performed at all stages by Cranfield University personnel.

## Governance, discoverability, and reuse
- Data assets are organized with clear file naming and structure (per river, per metric, per reach/section) to support discoverability and reuse.
- Metadata implied through file attributes (e.g., Year, Width) and accompanying shapefiles and CSVs.
- Suitable for cross-disciplinary use, enabling examination of long-term and short-term river dynamics, and informing data-driven river management, policy, and planning across partnered networks.

## Potential applications and implications for data strategy
- Enables evaluation of how human activities and environmental drivers shape river planforms over multiple timescales, informing adaptive management and risk assessment.
- Supports cross-sector collaboration by providing a structured, multi-temporal geospatial dataset with clear lineage from remote sensing to derived metrics.
- Highlights data governance needs for large, multi-temporal hydrological datasets: standardized formats, robust metadata, quality controls, and documentation of methods for reproducibility and future updates.