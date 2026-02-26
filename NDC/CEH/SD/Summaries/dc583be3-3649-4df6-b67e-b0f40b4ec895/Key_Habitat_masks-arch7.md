# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

- Overview
  - National GIS-derived masks for calcareous grassland, coastal landscapes, upland and lowland heath habitats in England (1992-93 survey, published 2017).
  - Created to identify existing or potential habitat areas and to define the population from which 1 km sampling sites were drawn for ecological surveys.
  - Masks were validated against other information; some mis-matches exist but overall fit is acceptable for project purposes.
  - Coastal heathlands are acknowledged but reported separately; coastal mask is included as part of the dataset.

- Spatial scope and data granularity
  - Geography: England
  - Resolution: 1 km squares (vector polygons)
  - Dataset structure: each square is a polygon with indicators for applicable masks and landscape types
  - Masks included (and how they relate): calcareous, coastal, lowland heath, upland

- Mask definitions and methodology
  - Calcareous grassland mask
    - Based on 1 km squares containing existing or potential calcareous grassland
    - Derived by GIS layering of geology and drift deposits
    - Criteria include coverage of potential areas and exclusion of squares >75% urban
    - Potential areas identified to allow future habitat restoration or expansion
    - Validation: compared with other data; overall acceptable fit
    - Coverage: 26,555 1 km squares in England
  - Coastal mask
    - Defined as land within 500 m inland from high water mark plus contiguous saltmarsh, dunes, and coastal bare land
    - Coastline delineation used Land Cover Map 1990 and a 25 m Landsat-based classification
    - Inland coastal buffer created by extending coastline inland; borders aligned with Bartholomew 1:250,000 boundaries
    - Final database: 8,870 1 km squares (after exclusions, 7,341 remain)
    - Note on data sources and limitations due to inland maritime misclassifications
  - Lowland heath mask
    - Based on soils likely to support heathland at landscape scale
    - Built from Soil Survey and Land Research Centre soils data; peat soils included
    - Distinguishes lowland from upland via ITE Land Classification 1990; excludes upland-dominated areas
    - Coastal heathlands partially captured; reported separately due to limitations of soil-based differentiation
    - Coverage: 8,538 1 km squares in lowland England
  - Upland mask
    - Derived from ITE Land Classification 1990; uses 32 land classes categorized as upland or lowland
    - Excludes predominantly urban squares (>75% urban)
    - Coverage: 15,616 1 km squares in England

- Dataset structure and attributes
  - Format: vector dataset of 1 km square polygons
  - Presence indicators (one per mask):
    - DOMGEOL: calcareous mask sub-types (e.g., 2 = Oolitic limestone, 7 = Chalk, 8 = Massive limestone, 0 = Other)
    - COAST: coastal mask indicator (1 = coastal)
    - CALC: calcareous mask indicator (1 = calcareous)
    - LOHEATH: lowland heath mask indicator (1 = yes)
    - UPHEATH: upland mask indicator (1 = yes)
  - STRATA: Coast type descriptor (H = hard coast, S = soft coast, E = estuarine)

- Data provenance and references
  - Origin: Countryside Survey data (Institute of Terrestrial Ecology/Centre for Ecology & Hydrology) 1992-1993
  - Mask derivation and validation led by Barr, Bunce, Cummins, Hallam, Hornung, Wood, and colleagues
  - Key related publications and datasets include Barr et al. (2017) Habitat and vegetation data; Bunce et al. (1990) ITE Land Classification; Fuller et al. (1993) Land Cover Map 1990
  - NERC Environmental Information Data Centre references provided for dataset access

- Practical considerations for GIS use
  - Masks may overlap; note that some squares can belong to more than one habitat mask
  - Coastal heathlands are partially captured; users should consult the separate coastal heathland reporting for complete coverage
  - Data are historically anchored to 1992-1993 field surveys but are provided as a national mask layer suitable for current GIS analyses and as a basis for sampling design or habitat planning
  - Suitable for integrating with other GIS layers (geology, soil, land cover) to support habitat assessment, restoration planning, or policy analysis