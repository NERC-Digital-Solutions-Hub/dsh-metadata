# The Glastir Monitoring and Evaluation Programme (GMEP)

## Purpose and scope
- Wales implements agri-environment schemes (AES) since the early 1990s; Glastir is the current scheme.
- GMEP, established in 2013 by the Welsh Government, monitors the effects of Glastir on the environment.
- Aims:
  - Collect evidence on the effectiveness of bundles of management interventions for outcomes related to climate change, biodiversity, soil and water quality, and woodland expansion.
  - Quantify status and trends in the environment generally.
  - Synthesis and analysis to identify environmental impacts driven by factors such as land use, climate, and pollution beyond Glastir interventions.

## How this aligns with the Analyst Monitoring the Environment archetype
- Involves verifying, quality assuring, cleaning, and transforming data from established sources.
- Applies standardized analytical methods to produce outputs (e.g., assessments of environmental health against standards).
- Presents findings via clear formats (reports, maps, charts) and stores datasets in appropriate data portals for reuse and scrutiny.
- Addresses challenges around increasing dataset value and improving access to underlying data.

## The unified peat map: purpose and significance
- Purpose: Support GMEP by mapping peat extent and condition in Wales; informs understanding of peatlands’ role in climate, biodiversity, and land-use dynamics.
- Context: Commissioned by Welsh Government; developed by the UK Centre for Ecology and Hydrology (CEH) with support from the British Geological Survey (BGS) and Natural Resources Wales (NRW).
- Key takeaway: Provides a more comprehensive and detailed picture of deep peat distribution across Wales, including many small lowland peat units, and highlights major upland peat areas.

## Generation methods (how the unified peat map was created)
- Data sources combined (via GIS union) to produce the GMEP_Unified_Peat_Map.shp:
  - i) Areas mapped as peat in the British Geological Survey (BGS) superficial geology map (1:50 000).
  - ii) Soil data from Forestry Commission Wales (FC Wales) records; soil codes 8a–14w indicate peat thickness >45 cm.
  - iii) Deep peat boundary (>0.5 m) from the Lowland Peatland Survey of Wales programme.
  - iv) Habitat polygons indicating deep peat presence (E class, except E2) from the Habitat Survey of Wales (Phase I).
- Output: A unified dataset describing peat with thickness of at least 45 cm, created by sequentially joining the layers in ArcMap GIS.

## Quality control and limitations
- Final product quality depends on the quality of input datasets from national agencies.
- Data provenance is documented (Lawley 2009; Pyatt 1982; Kennedy 2002; Jones et al. 2011; Bosanquet et al. 2013; Blackstock et al. 2010).
- Boundary precision is higher in lowlands and less precise in uplands due to vegetation mosaics and mapping limitations.
- The product name and format: GMEP_Unified_Peat_Map.shp (ESRI Shapefile, multipart polygon) with standard GIS fields (FID, Shape_Area, Shape_Len, etc.).

## Data product details
- File: GMEP_Unified_Peat_Map.shp
- Type: ESRI Shapefile (multipart polygon)
- Attributes:
  - FID: Unique polygon identifier
  - Shape_Area: Area in square metres
  - SHAPE_LEN: Perimeter length in metres
  - DESC_: Description of polygons ('Peat')
- Purpose: Delineates peat soils in Wales, based on thickness criteria and multiple data sources as described.

## Implications for monitoring and data sharing
- Supports ongoing monitoring of peat extent and condition as part of environmental status and trend reporting.
- Data are intended for reuse within environmental monitoring frameworks; any products derived require explicit acknowledgment of the source (Welsh Government and partner organizations) and BGS content where applicable.
- Highlights the value of integrating multiple data sources to enhance peat resource mapping and the monitoring of greenhouse gas emissions and land-use impacts.

## References and further reading
- Key technical reports and foundational studies informing the map and methodology (e.g., Evans et al. 2015; Blackstock et al. 2010; Jones et al. 2011; Bosanaquet et al. 2013; Lawley 2009; Pyatt 1982; Kennedy 2002; ECOSSE 2007; Vanguelova et al. 2012; and CEH/GMEP final reports).
- Acknowledgment requirements for data usage are specified, including copyright and data-provider statements.