# Dataset documentation

- LCM1990 is a parcel-based UK land cover map produced from Landsat-5 imagery (30 m) to support monitoring and decision-making. It classifies into 21 Broad Habitat-based classes and is aligned with the LCM2015 spatial framework to enable long-term change analysis. The vector and raster products are provided in multiple resolutions to support a range of monitoring applications. Each product has a Digital Object Identifier (DOI) for citation, and data access is via CEH’s Environmental Information Platform with potential licensing fees.

## Data products and structure

- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland
  - Each polygon carries rich attributes: dominant class, source image, per-polygon class breakdown, mean classification probability, and geometry identifier (gid)
- 25 m raster
  - 3-band raster: band 1 dominant LCM1990 class per polygon, band 2 mean per-polygon classifier confidence, band 3 percentage of polygon area covered by the modal class
- 1 km rasters
  - Dominant cover at 1 km for both Target (21) and Aggregate (10) classes
  - Percentage cover at 1 km for Target (21 bands) and Aggregate (10 bands)
  - Note: percentage values are integer and may not sum exactly to 100 due to rounding; coastal areas may sum to less than 100
- Spatial framework and comparability
  - Core framework follows LCM2015 methods to maximise compatibility and enable 25-year land cover change products (1990–2015)
- Data formats and access
  - Core vector product; 25 m raster; 1 km rasters
  - Access via CEH Environmental Information Platform (eip.ceh.ac.uk); full vector dataset available on request; licensing fees may apply

## Class definitions and mapping

- 21 LCM1990 classes
  - Based on UK Biodiversity Action Plan Broad Habitats (Jackson, 2000)
  - Some classes subdivided for spectral distinctions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment)
- Relationship to Broad Habitats
  - Each class corresponds to a Broad Habitat category with defined characteristics and notes on spectral interpretation
- Distinctions between land cover and land use
  - LCM1990 maps land cover; some classes may not uniquely indicate land use (e.g., arable land may be used for multiple purposes)

## Spatial and data quality details

- Minimum mapping unit and dissolution
  - Minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding areas
- Unique identifiers and metadata
  - Each parcel has a unique geometry identifier (gid); metadata includes dominant class, pixel counts per class, and per-polygon classification confidence
- Uncertainty information
  - Random Forest per-pixel probability is provided as mean per-polygon value (vector) and in the 25 m raster’s band 2
- Projections
  - Great Britain data: British National Grid (EPSG 27700)
  - Northern Ireland data: Irish National Grid (TM75 / EPSG 29903)
- Data access and licensing
  - 25 m and 1 km rasters available via CEH eIP
  - Full vector product on request; licences may apply for some uses

## Citing and use in publications

- All LCM1990 products have DOIs; citations should include author and date, with the DOI in references
- Example citation format provided for GB and NI products (vector, 25 m raster, 1 km target, 1 km dominant, and aggregate classes)

## Quality assurance and validation

- Data produced with defined methods and code; QA checks cover projections, spatial completeness, modal class presence in polygons, metadata consistency, value ranges (0–100 for rasters), and pixel sizes
- A full validation exercise has been conducted against reference datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately
- The parcel-based framework traces back to the 2007 OS MasterMap-derived base, with field-boundary changes considered minor for overall accuracy

## Access, licensing, and further information

- Access points
  - CEH Environmental Information Platform for raster products
  - Full vector product available on request from CEH
- Licensing
  - Some users/applications may require licences; fees may apply
- Additional information
  - LCM1990 documentation, dataset-specific DOIs, and contact details are available via CEH’s LCM data pages
  - Journal paper and additional information are in preparation or forthcoming

## Appendix highlights (context for interpretation)

- Appendix 2 provides summaries of Broad Habitat definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Grasslands types, Wetlands, and Coastal/marine habitats)
- Appendix 3 and 4 provide technical details for colour mapping and composite images used in LCM1990