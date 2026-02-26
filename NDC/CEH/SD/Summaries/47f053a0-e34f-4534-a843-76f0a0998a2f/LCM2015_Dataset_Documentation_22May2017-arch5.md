# Dataset documentation

## Overview and purpose
- Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map created by classifying satellite data into 21 classes, based on UK Broad Habitat definitions.
- Provides a range of data products to support diverse user needs; intended as a stable, archived dataset with DOIs for citation.
- Not intended for current state change mapping in its present state; differences between maps reflect real change plus classification and methodological changes.

## Data products and structure

### Vector data set
- Core vector product: polygons with attached metadata for each parcel.
- Spatial scope: Great Britain and Northern Ireland; total polygons roughly 6.7 million (GB) and 0.9 million (NI).
- Key attributes (Table 2): 
  - gid (unique polygon identifier)
  - BHAB (dominant Broad Habitat class, text)
  - Pix_dist (distribution of pixels per class within polygon; 23 numbers)
  - unc (mean per-polygon probability; 0–255 scale)
  - unc_stdev (standard deviation of uncertainty)
  - npix (number of pixels in polygon)
  - Modal_class (dominant LCM2015 class code 1–21)
  - Modal_prop (proportion of polygon in dominant class)
  - Composite (which composite image the classification used)
- Rich metadata per polygon, including dominant class, pixel-level breakdown, and uncertainty; gid should be retained for traceability.

### 25 m raster
- Two-band raster:
  - Band 1: dominant LCM2015 class per polygon
  - Band 2: mean per-polygon probability from the classifier
- Extent and metadata provided in Table 3; GB uses British National Grid (EPSG 27700); NI uses TM75 Irish Grid (EPSG 29903).

### 1 km raster (aggregate products)
- Created by summarising 25 m raster data to percent cover and dominant class at 1 km resolution.
- Available for both 21 target classes and 10 aggregated classes.
- Percentage cover products are integer values; sums may drift slightly from 100 due to rounding; coastal areas may sum to less than 100.

## Class structure and labeling

### LCM2015 classes
- 21 target classes (based on UK Broad Habitats). Some are further divided in certain products:
  - Built-up Areas and Gardens split into Suburban and Urban
  - Dwarf Shrub Heath split into Heather and Heather grassland
  - Littoral Sediment split into Littoral sediment and Saltmarsh
- Each parcel is assigned a unique gid label; metadata supports traceability and communication between users.

### Color mapping and documentation
- Appendix describes standard colour mapping for display purposes.
- Appendix 1 and 2 summarize Broad Habitat definitions used for LCM2015; Appendix 3 provides colour recipe; Appendix 4 lists composite images used.

## Methodology and differences from LCM2007

### Classification algorithm
- New: Random Forest classifier (handles multi-modal training data; no need for spectral sub-classes).
- Previous: Maximum Likelihood classifier (required spectral sub-classes).

### Training data and ancillary data
- LCM2015 uses an initial stable training set (areas classified the same in 2000 and 2007) and supplements with coastal and challenging classes.
- Ancillary data (e.g., slope, distance to rivers) are incorporated as inputs to the classifier, rather than applied post-classification.

### Spatial framework and segmentation
- LCM2015 removes segmentation-based polygons from the spatial framework, aiming for per-pixel classification and easier change mapping.
- No segmentation is used for GB; Northern Ireland largely unaffected by segmentation changes.

### Notable class and methodological changes
- Montane class removed; areas mapped as Inland Rock or upland habitats based on spectral data.
- Rough grassland class removed; grassland types now align with Broad Habitat definitions without soil data.
- Mixed woodland defined via majority per-pixel labeling rather than object-based training; may affect some mixed stands.
- Stable training areas used as a base, with supplementary areas for coastal and difficult classes.
- Overall emphasis on an objective, input-data-driven process integrated into the classifier.

## Data quality, uncertainty, and usage cautions

- Uncertainty is provided as mean per-polygon probability (via the Random Forest) and stdev for the polygon.
- Caution: differences between LCM versions and the presence of classification errors mean users should be careful when using LCM2015 for change mapping in its current state.
- Minimum mappable area: >0.5 ha; polygons smaller than 0.5 ha or lines < 20 m dissolved into surrounding landscape.
- Some classes (e.g., Montane, certain woodland classifications) have redefinitions or changes that may influence historical comparisons.

## Data access, licensing, and citation

- Access points:
  - 1 km raster: CEH Environmental Information Platform (eip.ceh.ac.uk) – openly accessible.
  - Full vector and 25 m raster: available under licence on request from CEH.
- DOIs: All LCM2015 products have DOIs for citation (GB vector, GB 25 m raster, GB 1 km products; NI vector, NI 25 m raster, NI 1 km products).
- Data citation examples provided; DOIs should be cited in publications to ensure reproducibility.

## Projections and geographic details

- Vector and raster data sets:
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: TM75 Irish Grid (EPSG 29903)
- Table 3 provides exact pixel counts, extents, and coordinate details for GB and NI products.

## Access details and contact

- Primary contact: spatialdata@ceh.ac.uk
- 1 km raster data: CEH Environmental Information Platform
- Full vector and 25 m raster: licensing on request; online application process available
- Data papers and additional information forthcoming; dataset documentation and references provided within the document.

## Citing and references

- DOIs are provided for each product to support repeatability and tracking of usage.
- References include Jackson (2000) on Broad Habitat definitions and Morton et al. (2011) for LCM2007 methodology.