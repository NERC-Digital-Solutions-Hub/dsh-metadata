# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Data generation and sources
- Compared Landsat 7 SLC-off imagery (15 m resolution) with Landsat 2005 imagery and the Change in Natural Forest Cover (1990–2005) dataset.
- Imagery sources:
  - USGS Global Visualization Viewer (Glovis).
  - Years by scene: p158r73 (2006–2010) and p158r72 (2006, 2007, 2009, 2010).
- Preprocessing:
  - Landsat 7 gap-free composites produced with ENVI 4.7.
  - Landsat 8 imagery preprocessed through Google Earth Engine.

## Attribute data and schema
- Attribute fields defined for describing imagery and change:
  - Scene, Baseline, Year, Area_ha, X_utm, Y_utm, Zone, Code
- Field details:
  - Scene: Landsat imagery used; Description and Type string.
  - Baseline: Imagery used for comparison; Type string.
  - Year: Year of change (e.g., 2006 = 2005–2006); Type long.
  - Area_ha: Area in hectares; Type double.
  - X_utm / Y_utm: UTM coordinates; Type long.
  - Zone: Protected-area delineation (priority for conservation, sustainable use, controlled settlements); Type string.
  - Code: Unique identifier; Type long.

## Processing and analytical approach
- Change detection through visual interpretation and manual digitization using Esri software.
- Observations documented in the attribute table; identification criteria were expert-judgment-based and subjective.
- Characteristics used to distinguish true clearings from natural phenology changes include shape, color, texture, and proximity to other clearings/settlements.
- Output comprised 5,954 polygons; approximately 75% of clearings were ≥ 1 ha; minimum recorded area ~5 pixels.

## Data structure and format
- Data structure: shapefile.
- Key attributes (8 relevant columns): scene, baseline, year, area_ha, x_utm, y_utm, zone, code.

## Usage and citation
- Purpose: Evaluate the effectiveness of conservation investments in reducing deforestation and fires in the Ankeniheny-Zahemena Corridor, Madagascar.
- Citation: Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.