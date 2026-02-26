# Otter Collection and Post Mortem Examination

## Overview
- Otter carcasses submitted by local authorities, environmental organisations, and the public to Cardiff University Otter Project.
- For each otter: recorded location (National Grid Reference, min 6 figures) and collection date; post-mortem conducted per a standard protocol.
- Collected data include phenotypic characteristics (sex, length, weight, age class) and a condition score derived from body metrics.
- Liver tissue samples retained at -20°C; study analysed 278 liver samples from 2006–2017, as a stratified random sub-sample, mainly from England and Wales with three animals from Scotland.

## Biological and sample data
- Otters categorized by size into juvenile, sub-adult, or adult based on developmental features.
- Detailed post-mortem data and metadata captured using a structured schema (e.g., Unique University of Wales Cardiff reference number, sex, age class, year found, weight, body condition index, geographic coordinates, etc.).

## Laboratory analysis
- Two 1 g subsamples taken from each liver: 
  - Subsample 1: acid digested and analyzed by inductively coupled plasma mass spectrometry (ICP-MS) for trace elements.
  - Subsample 2: oven-dried to determine dry matter content (105°C for 18 hours) and re-weighed.
- Concentrations expressed on a dry weight basis (μg/g). No recovery correction applied; reported recoveries deemed consistent across periods.
- Metals measured include a suite of elements (e.g., Ag, As, Cd, Cr, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Se, Zn) with additional elements sometimes recorded (e.g., Al, Sr). Data are organized in a detailed, multi-parameter format across batches (2009, 2011, 2017).

## Spatial data collection and sources
- Compiled spatial data describing variation in stream/soil biochemistry, weather, and anthropogenic contaminant sources.
- A model-derived map of predicted nanosilver concentrations in surface water (Dumont et al., 2015) used as a proxy for exposure.
- Spatial data represented as continuous rasters or points in ArcGIS (ArcMap, v10.4.1).

## Spatial data processing and otter exposure area
- Otter linear home range along rivers estimated between 5 and 40 km; analysis used a 20-km-diameter circular area centered on the carcass to approximate exposure area.
- Geospatial Modelling Environment (GME, v0.7.4) used to extract area-relevant data with isectpolypoly tooling.
- For each otter area, raster data extracted for a range of geological and anthropogenic variables (summarised as means for soil elements, soil pH, sediment elements, river pH, rainfall, predicted nanosilver, and population density) or sums for:
  - Number of consented discharges to controlled waters
  - Annual mass inputs of metals to controlled waters
- Distance from the otter carcass to the coast calculated by snapping otter locations to the 1:50,000 Watercourse Network and measuring downstream to the mouth; shortest river-coast distance computed with RivEx.
- Otters located outside the relevant coastal catchment (N=4) excluded from scoring due to uncertainty about river catchment relevance.

## Data sources and column definitions (Table 1)
- Geological and anthropogenic contaminant data sources include:
  - Soil elements, soil carbon, soil pH (GB 1 km resolution; various historical time frames)
  - Sediment elements (high-resolution grids; 1968–2004)
  - River/stream pH (500 m grid; 1968–2004)
  - Predicted silver nanoparticle concentrations in surface water
  - Rainfall (5 km grid; 1981–2010 average)
  - Mining sites (past & present within 10 km; multiple datasets)
  - Consented discharges to controlled waters (within/upstream 10 km; multiple sources)
  - Annual mass inputs of metals to controlled waters (within/upstream 10 km)
  - Human population density (polygon data then rasterized; 2001)
  - Other environmental and anthropogenic indicators (e.g., urban/industrial density)
- Each data layer includes units, spatial resolution, time period, and bibliographic references.
- The table also documents a detailed mapping of otter-level and environmental variables (e.g., X/Y coordinates, dry matter, body condition indices, liver element concentrations, soil and water pH, sediment metals, rainfall, distance to coast, discharge counts, mining presence, metal inputs, and population density).

## Data notes and interpretation
- ND = not detected; NA = data not available for the otter’s area; n/a = not applicable.
- The liver concentrations are not recovery-corrected; regional and temporal variation in recoveries were considered acceptable based on cross-period consistency.
- Study relies on multiple external data sources with varying resolutions and time frames, integrated at the otter level to explore associations between liver metal burdens and environmental exposure metrics.

## References
- Includes extensive citations for geospatial tools (ArcGIS, GME, RivEx), laboratory methods (ICP-MS, dry matter determination), and environmental data sources (soil geochemical atlases, mining inventories, emissions inventories, population data, nanosilver exposure modeling, etc.).