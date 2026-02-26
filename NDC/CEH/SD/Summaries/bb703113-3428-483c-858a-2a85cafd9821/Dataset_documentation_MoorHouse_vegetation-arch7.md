# Vegetation map of the Moor House National Nature Reserve

## Overview
- ESRI Shapefile (MH_Vegetation.shp) containing polygons that represent vegetation areas digitized from Moor House National Nature Reserve in the northern Pennines, England.
- Original map created by Eddy, Welch, and Rawes (1960–1965) at the Nature Conservancy’s Moor House Field Station; mapping conducted in 1960–1961.
- Final map grouped into 16 vegetation units for clarity, based on physiognomy and McVean & Ratcliffe (1962).

## Data content and schema
- File: MH_Vegetation.shp
- Attributes:
  - VEG: text description of vegetation type (as per McVean & Ratcliffe, 1962)
  - SYMBOL: numeric code representing the vegetation description
- Geometry: polygons for vegetation areas
- Spatial reference:
  - Coordinate system: British National Grid (OSGB1936)
  - Projection: Transverse Mercator Great Britain
- Resolution: mapped at 1:10560 (6 inches to the mile)
- Extent and scale details indicate a base map fit to physiognomic units rather than a single uniform grid
- Data lineage notes that units were initially around 30 but final map uses 16 units for clarity

## Classification scheme (codes and descriptions)
- 2 SPHAGNETO-JUNCETUM EFFUSI
  - Occurs along stream/river valleys; gleyed peaty silts; Juncus effusus, Polytrichum commune, Sphagnum recurvum are dominant
- 3 TRICHOPHORO-ERIOPHORETUM
  - Often Calluna vulgaris higher cover; flat blanket bog below 600 m with high water table
- 4 SANDSTONE SCREE
  - Vegetation among scree; soil largely absent; bryophytes and lichens prevalent
- 10 MADE GROUND
  - Areas disturbed by mining/quarrying
- 60 JUNCETUM SQUARROSUS SA (sub-alpinum)
  - Species-poor; constant species Juncus squarrosus
- 69 CALCAREOUS SPRINGS
  - Very small extent; vegetation associated with groundwater emergence; zoned and species-rich
- 117 CALLUNETO-ERIOPHORETUM
  - Uneroded bog; dwarf-shrub dominated by Calluna vulgaris and Eriophorum vaginatum
- 120 FESTUCETUM
  - Grasslands dominated by Festuca spp.
- 129 ERODING BOG
  - Blanket bog with >30% original surface eroded; recolonisation on exposed surface
- 132 PTERIDIETUM
  - Bracken-dominated communities
- 136 AGROSTO-FESTUCETUM
  - Dry, species-rich, heavily grazed grasslands; rich in Agrostis
- 140 SPHAGNETO-CARICETUM ALPINUM
  - Slopes on organic soils; Sphagna with Carices and Eriophorum angustifolium
- 149 NARDETUM SUB-ALPINUM
  - Species-poor; dominated by Nardus stricta
- 161 ERIOPHORETUM
  - Blanket bog dominated by Eriophorum vaginatum
- 171 RECOLONISED PEAT
  - Peat surfaces recolonised by vegetation
- 203 FLUSHED GLEYS
  - Vegetation on base-rich, flushed gleys

## Data provenance and references
- Basis: The vegetation map derived from Moor House Reserve vegetation work (1960–1965)
- Primary publication references for nomenclature and classification:
  - Eddy, Welch & Rawes (1968) Plant Ecology
  - McVean & Ratcliffe (1962) Plant communities of the Scottish Highlands
  - Clapham et al. (1952) Flora of the British Isles
- Further context: Environmental Change Network (for site references)

## Usage notes for GIS specialists
- The dataset provides a polygonal vegetation map with a simple two-field attribute schema (VEG description and SYMBOL code) suitable for thematic mapping and symbolization by vegetation type.
- Use SYMBOL to join to a lookup table for full descriptions when creating map legends or for analysis; VEG field provides textual descriptions.
- Coordinate system is OSGB 1936 British National Grid; ensure any integration with other data uses appropriate transformation if needed.
- The 1:10560 scale indicates a relatively coarse, physiognomy-based classification; suitable for regional planning and policy visuals rather than fine-grained ecological analysis.
- Data reflects the 1960s mapping effort and generalised classification; consider data currency and potential changes if using for current analyses.

## Limitations and considerations
- Original data dates from 1960–1965; historical baseline with potential changes since.
- Mapping relied on subjective unit definitions and later consolidation into 16 units; some detail may be generalized.
- The dataset focuses on vegetation types and does not provide additional attributes beyond VEG and SYMBOL.