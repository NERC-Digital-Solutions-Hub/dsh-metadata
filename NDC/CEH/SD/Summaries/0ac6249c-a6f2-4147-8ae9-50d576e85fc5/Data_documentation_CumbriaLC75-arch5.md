# Cumbria_Land_Classification file details

## Overview
- Dataset documenting the Cumbria land classification system, defining 16 land classes (1–16) across the county.
- Derived from environmental characteristics (e.g., climate, altitude, slope) and later interpreted with geology and land use.
- Aims to enable governance, planning, and landscape understanding by providing a standardized classification and descriptive summaries.

## Data format and extent
- Format: ESRI Shapefile
- Resolution: 1 km
- Coordinate system: British National Grid (OSGB36), Projection: Transverse Mercator
- Extent: Great Britain
- Metadata/version: Dataset Documentation, Version 1, 20-11-2015
- Source and reading: Based on ecological surveys and map-based analyses (references cited in document)

## Data content and structure
- 16 land classes (1–16) organized in a hierarchical classification key (Figure 2) used to classify remaining grid squares (Figure 3).
- Attributes recorded from one-inch scale Ordnance Survey maps, including human artefacts (roads, buildings) and natural features.
- Class descriptions blend geomorphology, altitude, geology, and land use characteristics.
- A classification key and association patterns describe how classes relate to each other and to geographical zones (upland vs. lowland).

## Methods and analysis
- Sampling approach: approx. 11% of Cumbria sampled by grid squares (central square from 3x3 km blocks).
- Analytical methods: Indicator Species Analysis (ISA) and Reciprocal Averaging (RA) to define and validate classes.
- Data collection and processing: Compilation of map characteristics; data analysis workflow illustrated (Figure 1).
- Geological approach: Use of geology attributes to differentiate classes; some attributes (drift) were excluded due to map limitations.

## Land class descriptions (high-level)
- Land Class 1–2: Predominantly lowland with flat to undulating terrain, mixed farmland, and nutrient-rich brown soils.
- Land Class 3: Lowland-influenced with limestone geology; undulating land and mixed soils.
- Land Class 4: Mixed upland-lowland features near central fells; variable soils.
- Land Class 5–6: Lowland alluvial plains; intensive farming; significant human artefacts and communications influence.
- Land Class 7–8: Coastal sands/mud; livestock-focused farming; coastal/open shore characteristics.
- Land Class 9–12: Upland foothills and fells; conifer plantations; peat and acidic soils; variable vegetation and drainage.
- Land Class 13–16: Pennine/Lake District margins to summits; steep slopes to high elevations; extensive open range sheep grazing; peat soils dominating.

## Distribution and frequencies
- Nearly two-thirds of Cumbria categorized as lowland (classes 1–6, with overlap into adjacent classes).
- Coastal and upland classes occur less frequently.
- Spatial patterns: some classes (1–2) occur in large blocks; others (4, 11) in smaller clusters.
- Upland squares tend to form cohesive patterns; lowland classes appear in larger, more widespread blocks.
- Tables (Table 2: frequencies; Table 3: associations) summarize the distribution and inter-class relationships (noting that the association patterns are described but specific numeric values are in the tables).

## Data quality, provenance, and limitations
- Based on historic map-derived attributes with a sampling-based approach; drift excluded due to map limitations.
- The hierarchy is not strictly numerical; altitude is the major initial division, with geology shaping subsequent splits.
- Differences between sample and full enumeration are small, but some regional heterogeneity remains.
- Class descriptions rely on subsequent field surveys and literature, not solely map features.

## Metadata, governance, and usage
- Documentation accompanies the dataset, with bibliographic references to supporting ecological and multivariate methodologies.
- Primary governance considerations include ensuring alignment with data user needs, maintaining metadata quality, and documenting any updates or reclassifications.
- Intended use includes landscape understanding, regional planning, and environmental analysis; potential need for modernization or interoperability with contemporary GIS standards.

## References (methodology and context)
- Bunce, R. G. H., Morrell, S. K. & Stel, H. E. 1975. The application of multivariate analysis to regional survey.
- Hill, M. O. 1973. Reciprocal Averaging: an eigenvector method of ordination.
- Hill, M. O., Bunce, R. G. H. & Shaw, M. W. 1975. Indicator species analysis, a divisive polythetic method of classification.