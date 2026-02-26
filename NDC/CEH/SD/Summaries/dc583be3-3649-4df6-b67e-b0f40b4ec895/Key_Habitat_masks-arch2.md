# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

- Purpose and scope
  - Provides GIS-based spatial masks (1 km squares) for four key English habitats to support the Countryside Survey monitoring program (Key Habitats 1992-93).
  - Masks cover calcareous landscapes, coastal landscapes, upland landscapes, and lowland heath; coastal heathlands are reported separately.
  - Masks define populations from which 1 km sampling sites were selected, supplementing Countryside Survey 1990 data.

- What the dataset contains
  - Vector dataset of 1 km square polygons across England, with presence flags for each mask.
  - Distinguishes calcareous mask by limestone types; includes a coastal mask with inland extent up to 500 m from the high water mark.
  - Masks included: Calcareous, Coastal, Lowland Heath, Upland.
  - Summary coverage (approximate): 26,555 calcareous squares; 8,870 coastal squares (with exclusions leaving 7,341 coastal squares); 8,538 lowland heath squares; 15,616 upland squares.

- How the masks were created (methodology)
  - GIS-based derivation using national Geology and drift data to identify suitable areas at 1 km resolution.
  - Calcareous mask: identify current and potential calcareous grassland by combining solid geology, drift deposits, and exclusion of >75% urban land; expanded to escarpments as needed.
  - Coastal mask: define 500 m inland buffer from a coastline derived from Land Cover Map 1990; used Landsat-based coastline derivation with smoothing and validation against HWM data where available.
  - Lowland heath mask: built from soils and altitude data to identify areas with potential for heath, using ITE Land Classification 1990 to separate upland areas; acknowledges subjectivity in distinguishing upland vs. lowland heath.
  - Upland mask: based on ITE Land Classification 1990 classes; excludes predominant urban squares; final mask covers 15,616 squares.
  - Validation: masks were compared with other information; overall fit deemed acceptable, though some mismatches exist.

- Dataset structure and fields
  - Format: vector dataset; each 1 km square polygon contains flags for the four masks.
  - Key columns:
    - DOMGEOL, Type/Description: calcareous mask subtypes (e.g., 1 = calcareous mask; 2 = Oolitic limestone; 7 = Chalk; 8 = Massive limestone; 0 = Other).
    - COAST, Type/Description: coastal mask indicator (1 = coastal mask).
    - CALC, Type/Description: calcareous mask indicator (1 = calcareous mask).
    - LOHEATH, Type/Description: lowland heath mask indicator (1 = lowland heath mask).
    - UPHEATH, Type/Description: upland mask indicator (1 = upland mask).
    - STRATA, Description: coastal mask strata (H = hard coast, S = soft coast, E = estuarine).

- Data provenance and usage notes
  - Origin and management: developed under the Countryside Survey program (Institute of Terrestrial Ecology/Centre for Ecology & Hydrology); masks validated and managed by project teams, with data management by CEH.
  - Related publications and data records: Barr, Barr et al. (2017) Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993; NERC EIDC record.
  - Access and references: dataset referenced via DOI in the NERC Environmental Information Data Centre; foundational methods described in Bunce & Shaw (1973) and related Barr et al. reports.

- Practical considerations for analysts
  - Standardised, reproducible masks suitable for selecting monitoring locations and for cross-dataset analyses.
  - Strengths: consistent 1 km grid, explicit criteria for each habitat type, clear documentation of data sources and validation.
  - Limitations: coastal heathlands are not fully captured within the main masks and are reported separately; potential misclassifications exist due to overlaps and regional variation; exact thresholds differ regionally (e.g., upland vs. lowland delineation).
  - Opportunities: increase dataset value by integrating with other environmental layers (e.g., habitat status, biodiversity indicators) and by providing access to underlying spatial data sources for broader reuse.

- Related materials and access
  - Core dataset: Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993 (Barr et al., 2017), NERC EIDC.
  - Supplementary and foundational sources: Countryside Survey 1990 materials; ITE Land Classification of Great Britain 1990; GIS and remote sensing methods cited in the accompanying documentation.