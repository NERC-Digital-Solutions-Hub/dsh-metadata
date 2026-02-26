# Cumbria_Land_Classification file details

- This document describes a GIS-ready land classification dataset for Cumbria, Great Britain, organized into 16 Land Classes that represent environmental and land-use patterns across the county.
- Data product is provided as an ESRI Shapefile with a 1 km resolution, using the British National Grid (OSGB1936) projection (Transverse Mercator).

## Data format, scope, and spatial reference

- Format: ESRI Shapefile
- Resolution: 1 km
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain (dataset focuses on Cumbria’s 16 land areas)
- Data coverage: Cumbria, with a methodology described for classifying grid squares and extending to classify remaining squares via a dichotomous key

## Attributes and data content

- Dataset includes a large set of map-derived characteristics captured from one-inch Ordnance Survey maps. The attributes cover a wide range of features including roads, waterways, terrain forms, soils, vegetation, land use, and man-made features.
- The characteristic list is extensive (Table 1 in the document), comprising both natural and infrastructural features used to define the land classes.

## Methodology and analysis

- Sample design:
  - A county-wide grid was created by selecting the central square from 3 x 3 km blocks, resulting in roughly 11% sampling for analysis.
  - Attributes recorded from the maps informed the classification process.
- Data analysis:
  - Indicator Species Analysis (ISA) used to identify features that discriminate between classes.
  - Reciprocal Averaging (RA) used to assess relationships among sample squares.
  - The combination of ISA and RA defines the Land Classification hierarchy (Figure 2) and a dichotomous key (Figure 3) to classify the remaining squares.
- Objectives:
  - Identify distinctive land classes by combining environmental, topographic, soil, and vegetation characteristics.
  - Demonstrate the dominant role of altitude in dividing upland vs lowland and show geological influences on class differences.

## The Land Classes (16 classes)

- General organization:
  - Major division is between upland and lowland, with altitude as a dominant factor.
  - Geological associations help separate classes within the same altitude band (e.g., limestone vs sandstone regions).
  - Coastal classes (7 and 8) are distinguished from inland classes; higher elevation classes (9–16) cover uplands, fells, and summits.
- Lowland classes (1–6):
  - 1 and 2: Predominantly lowland map characteristics; Solway Plain and Eden Valley areas; medium to good quality agricultural land; varied soils (brown earths).
  - 3: Slightly higher elevation; western Eden Valley; limestone-laden undulating terrain; mixed pasture and arable use.
  - 4: Mixed with upland features; margins of central fells; variable agricultural quality; presence of moorland and well-drained soils.
  - 5: Alluvial plains; intensive farming; hedgerows; deep brown soils.
  - 6: Associated with human artefacts and communications; mainly lowland, intensively farmed grassland.
- Coastal classes (7–8):
  - 7: Coastal estuarine sand and mud.
  - 8: Coastal with substantial bare sand/mud; livestock-friendly, with hedges and improved pastures; deep, nutrient-rich soils.
- Upland and high-elevation classes (9–16):
  - 9–10: Upper fells and valleys; coniferous dominance in some areas; poor quality moorland and upland grazing.
  - 11–12: Complex middle fells; broadleaved woods or conifer plantations; variable soils; predominately upland grazing.
  - 13–14: Pennine/Skiddaw margins; steep, mostly treeless slopes; poor to intermediate soils; open-range sheep grazing.
  - 15–16: Upper slopes and summits of central Lake District fells; very rugged, largely treeless; peat and peaty soils; open range grazing.

- Distribution and patterns:
  - Nearly two-thirds of Cumbria classified as lowland.
  - Some land classes occur in large blocks (e.g., 1 and 2), while others occur in small groups (e.g., 4 and 11).
  - Upland classes tend to form cohesive blocks due to valley-disrupted geographies; lowland classes form broader extents and blocks.
- Summary descriptors and frequency:
  - The document provides summary frequencies (Table 2) and association patterns among land classes (Table 3), illustrating how classes relate and cluster across the county.

## Uses, interpretation, and outputs

- The 16-class hierarchy serves as a map-based classification to support landscape interpretation, planning, and policy analysis within GIS environments.
- The classification emphasizes altitude-driven upland vs lowland differentiation plus geological influences, enabling users to relate land-class types to geomorphology, land use, and vegetation.
- The dataset provides a basis for deriving thematic maps, landscape components, and spatial analyses that consider both natural and human-influenced features.

## Further reading and references

- Bunce, R. G. H., Morrell, S. K., & Stelf, H. E. (1975) on multivariate analysis in regional surveys.
- Hill, M. O. (1973) on reciprocal averaging (ordination).
- Hill, M. O., Bunce, R. G. H., & Shaw, M. W. (1975) on indicator species analysis and its application to the Cumbria study.

## Limitations and considerations

- Temporal scope: Based on historical map data (primarily mid-1970s); archival methodology and classifications reflect that period’s mapping conventions.
- Scope: While extent mentions Great Britain, the land-classification work and descriptions focus on Cumbria; users should be mindful of county-specific interpretations.
- Data structure: The attribute table is extensive; users should refer to Table 1 in the document for the complete list of map characteristics and codes.