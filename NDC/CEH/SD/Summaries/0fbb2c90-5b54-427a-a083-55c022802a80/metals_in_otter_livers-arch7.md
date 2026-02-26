# Otter Collection and Post Mortem Examination

## Objective
- Describe the collection, post-mortem analysis, and spatial-data integration used to study trace-element concentrations in otters and their environmental context.

## Data collection and sample details
- Otter carcasses submitted by local authorities, environmental groups, and the public to Cardiff Otter Project; recording location (National Grid Reference, min 6 figures) and collection date.
- Post-mortem following a standard protocol (Simpson, 2000) capturing phenotypic data: sex, length, weight, age class (juvenile, sub-adult, adult), and a condition score via scaled mass index (sSMI).
- Liver tissue samples retained for analysis; archived at -20°C.
- Present study: 278 liver samples from otters that died 2006–2017; stratified random sub-sample, mainly from England and Wales with 3 from Scotland.

## Laboratory analysis
- Measured liver concentrations of 13 elements: Ag, As, Cd, Cr, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Se, Zn (note: Zn included; 13 elements listed in text).
- Two 1 g liver subsamples per otter: one acid-digested for ICP-MS analysis; second for dry matter content via oven-drying (18 hours at 105°C).
- Dry matter basis results reported in μg/g dry weight; not recovery corrected due to generally consistent recoveries across periods.

## Spatial data sources and GIS workflow
- Collated spatial data describing variation in stream/soil biochemistry, weather, and anthropogenic contaminant sources.
- Included a map of predicted nanosilver concentrations in surface water derived from a model of household-to-river loadings (Dumont et al., 2015).
- Spatial data mapped in ArcGIS ArcMap (Version 10.4.1) as continuous raster layers or points.
- For pH in streams, stream pH data supplied as point data were converted to raster by inverse distance weighting (IDW) interpolation (cell size 500 m; 12 points; distance 1500 m).

## Otter range and data extraction methodology
- Otters have a linear home range estimated between 5–40 km; the study assumed a 20-km-diameter circular area centered on the carcass as a proxy for each otter’s potential range.
- Used Geospatial Modeling Environment (GME) to extract data for each otter’s 20-km range (Isectpolypoly tool).
- For each area, extracted raster data for a set of geological and anthropogenic variables (Table 1) and summarized as:
  - Mean values for soil elements, soil pH, sediment elements, stream pH, rainfall, predicted nanosilver concentrations, and human population density.
  - Sum values for the number of consented discharges to controlled waters and annual metal inputs to controlled waters.
- Distance to the coast calculated to test diet-related differences in metal accumulation:
  - Otter locations snapped to the 1:50,000 CEH Watercourse Network using ArcGIS; snapping tolerance 5,000 m.
  - River-coast distance along rivers computed with RivEx (Version 10.25).
- Otters outside the defined zone (N=4) excluded due to uncertainty about river catchment relevance.

## Data processing and variables
- Table 1 (data sources) includes:
  - Geological and soil data: soil elements, soil carbon, soil pH, sediment elements, river/stream pH, etc. with resolutions (1 km or 500 m grids) and time periods (e.g., 1978–1982, 1968–2004, 2007, 1981–2010).
  - Environmental contaminants: predicted nanosilver in surface water; past/present mining sites; consented discharges to controlled waters; annual metal inputs to controlled waters.
  - Landscape and demographic data: rainfall (1981–2010 average), human population density (various representations), mining-related datasets.
  - Units and measurement details provided (e.g., mg/kg for soil elements; μg/g dry weight for otter liver metals; ng/L for nanosilver; mm for rainfall; etc.).
- Data handling nuances:
  - n/a indicates not applicable; ND indicates not detected; NA indicates data not available for the otter’s area.
  - Some data sources have specific methodological notes (e.g., pH data transformation, interpolation, or licensing).

## Notes on provenance and references
- Multiple data sources and methods cited for geochemical basemaps, environmental inventories, and GIS tools (e.g., G-BASE, CEH watercourse network, RivEx, ArcGIS ArcMap).
- Key references include methods for otter post-mortems, scaled mass index for condition, and various environmental and geochemical datasets used to contextualize metal exposure.

## Implications for GIS practice
- Demonstrates integration of biological sampling with high-resolution spatial datasets to explore environmental exposure gradients.
- Highlights the importance of consistent GIS workflows (buffer-based exposure areas, raster and vector data merging, extraction tools like isectpolypoly, and distance analyses along hydrological networks).
- Emphasizes careful handling of varying data resolutions, time periods, and data quality, along with transparent documentation of data provenance and processing steps.