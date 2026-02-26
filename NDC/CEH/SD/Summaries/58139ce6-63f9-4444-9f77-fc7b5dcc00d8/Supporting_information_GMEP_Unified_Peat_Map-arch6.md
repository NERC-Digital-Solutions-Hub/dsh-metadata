# The Glastir Monitoring and Evaluation Programme (GMEP)

## Purpose and scope
- Welsh Government monitoring programme (initiated in 2013) to assess the effects of Glastir agri-environment schemes on climate, biodiversity, soil, water quality, and woodland expansion.
- Aims to quantify environmental status and trends and to identify how drivers of change (land use, climate, pollution) interact with Glastir interventions.
- Outputs support evidence-based assessment of scheme effectiveness and broader environmental monitoring.

## Unified peat map overview
- Aims to map peat extent and condition in Wales to support the GMEP monitoring framework.
- Commissioned by Welsh Government; developed by UK Centre for Ecology and Hydrology (with British Geological Survey and Natural Resources Wales).
- Provides a detailed, up-to-date view of peat distribution, including deep peat in uplands and substantial peat in lowland areas, with implications for biodiversity and greenhouse gas emissions.
- Represents a significant advancement over previous peat mapping efforts in Wales.

## Generation methods (data sources and integration)
- Datasets combined to form the unified peat map (peat > 45 cm):
  - Areas mapped as peat in the British Geological Survey (BGS) superficial geology map (1:50,000).
  - Soil mapping derived from Forestry Commission Wales soil survey records (codes 8a–14w indicating >45 cm peat depth).
  - Boundaries of deep peat from the Lowland Peatland Survey of Wales ground-based survey.
  - Habitat polygons indicative of deep peat presence from Habitat Survey of Wales (Phase I), excluding E2.
- Data layers were joined sequentially using the UNION function in ArcMap to create a final multipart polygon shapefile (GMEP_Unified_Peat_Map.shp).

## Quality control and limitations
- Data quality depends on the input datasets from national agencies; reliability varies by source.
- In uplands, boundaries may be less precise due to mosaics of mire and non-mire vegetation; lowland peat boundaries are generally more reliable.
- The combined product reflects multiple data sources and methodologies, with acknowledged uncertainties.

## Data product and metadata
- Product: GMEP_Unified_Peat_Map.shp (multipart polygon shapefile) showing peat soil outlines in Wales.
- Key attributes include:
  - FID: Unique polygon identifier.
  - SHAPE_AREA: Area of polygon (square metres).
  - SHAPE_LEN: Perimeter (metres).
  - DESC_: Description of polygons (e.g., 'Peat').
- Associated metadata and lineage are documented in the referenced source materials.

## How outputs are used and dissemination
- Supports monitoring of environmental outcomes and drivers within GMEP.
- Aids policy analysis and reporting to Welsh Government; informs understanding of peat-related greenhouse gas emissions and biodiversity.
- Outputs may be promoted, shared, and iteratively improved; potential to extend use to other data products and self-serve analyses.

## Attribution and licensing
- Any product derived from or incorporating the Data must acknowledge the source:
  - '© Hawlfraith y Goron: Llywodraeth Cymru' or '© Crown copyright: Welsh Government'
  - Contains Natural Resources Wales information © NRW
  - All rights reserved
  - Contains data from British Geological Survey: 'Derived in part from British Geological Survey geology data 1:50,000 scale. BGS © UKRI.'

## References and context
- Key supporting documents and datasets include: Evans et al. (2015) on the peat map; Lawley (2009); Pyatt (1982); Kennedy (2002); Jones et al. (2011); Bosanquet et al. (2013); Blackstock et al. (2010); ECOSSE (2007); Emmett et al. (2014–2017) on the GMEP program; and related Welsh Government reports.