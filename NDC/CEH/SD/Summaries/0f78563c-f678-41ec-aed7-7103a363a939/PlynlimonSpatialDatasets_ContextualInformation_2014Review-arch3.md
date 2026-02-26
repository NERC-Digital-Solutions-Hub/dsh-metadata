# INTRODUCTION

- The Plynlimon experimental/research catchments were established in the late 1960s by the Institute of Hydrology (IH), later part of CEH, to study how land use affects catchment water availability, flooding, and low flows. They lie at the headwaters of the River Severn and River Wye in mid-Wales and represent the two main upland land uses: coniferous forestry and sheep-grazed grassland, chosen to be as similar as possible in other environmental aspects.
- The sites were intensively instrumented, providing long-term climatic, streamflow, and soil moisture records, along with surveys of physical characteristics and land use. The project produced a range of thematic maps and datasets.

- Datasets and outputs include a comprehensive set of spatial layers and a hydrologically corrected elevation grid, designed to support hydrological and environmental analyses. The initial aim included high-quality long-term measurements and the production of data suitable for use in modelling and decision-making.

- References to related work and data sources are provided, with further information available on CEH’s website and linked publications.

## Key spatial datasets and layers

- Catchment and subcatchment boundaries
- River network
- Spot heights
- Wye catchment contour lines
- Severn catchment contour lines
- Soil Parental Materials
- Vegetation map (updated 2013)

- Plynlimon hydrologically corrected elevation grid (DTM/DEM)
  - File: Plyn_DEM (GRID, 15 m cells, British National Grid, hydrologically corrected)
- Additional outputs include shapefiles describing catchments, river networks, spot heights, contour lines, soils, and vegetation classes with appropriate attributes

## Data provenance and history

- Topographic and hydrography data originated from a large-scale Hunting Survey aerial photography program (1967-68). Later, these data were digitised in the late 1990s to create GIS-ready layers.
- Field surveys in the early years mapped soils, geology, vegetation, and land use. Some datasets are missing or held by other organisations; a key soil map (Bell 1969) was digitised and updated by CEH in 2005.
- The Vegetation map (2013) was produced by updating the CEH Land Cover Map 2000 (LCM2000) to better reflect heath, bracken, and improved grassland, using 2009 aerial photography and 2013 field truthing. A special variant column allows using coniferous plantations as either woodland or plantation status.

## Data formats, structure, and processing

- Digitisation and GIS: CEH digitised most shapefiles using ArcInfo; Severn contour lines were digitised separately by Edinburgh University. Ground control points were used to align features during digitisation.
- Hydrologically corrected DEM: Derived from 1:5,000 contour maps, spot heights, river maps, and catchment boundaries. A TIN was built and used to generate the hydrologically corrected grid (Plyn_DEM) with 15 m resolution.
- Dataset specifics and attributes:
  - Catchment shapefile: Catchment, Subcatch, boundaries
  - River network shapefile: FNODE_TNODE, LENGTH, Catchment, Type (natural or artificial)
  - Spot heights shapefile: HEIGHTS (elevation)
  - Wye and Severn contour shapefiles: HEIGHTS (contour elevations)
  - Soil Parental Materials shapefile: SOIL (code), Descript (description)
  - Vegetation map: id, VegClass, Variants (subclass) with a 2013 update aligned to LCM2000 classes
- A 2014 vegetation update integrates results from the SoilTrEC project and soil carbon surveys (top 30 cm, 2012).

## Data accessibility, standards, and governance

- Some datasets are not freely available due to ownership or data-sharing restrictions, representing a barrier to immediate reuse.
- Metadata adequacy is variable, requiring careful verification for suitability in new analyses.
- Data formats (Shapefiles, GRID/DTM) and coordinate systems (British National Grid) are specified to facilitate interoperability.
- Data governance considerations include the need to publicize underlying data while respecting IP and sharing constraints; the CEH site provides access to related publications and data products.

## Appendices and contextual notes

- Appendix A describes the Hunting Survey aerial photography campaign (1967) and notes on the archival status of film negatives, with digitised frame footprints.
- The document references foundational studies (e.g., Bell 1969; Brandt et al. 2004) and provides avenues for accessing additional information (CEH website and publications).