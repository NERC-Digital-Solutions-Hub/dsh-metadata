# Land Cover Map 2007 Dataset documentation

## Overview and purpose
- Parcel-based classification of UK land cover using 23 classes based on Broad Habitats.
- Data provided as a range of products (vector and raster) at multiple resolutions to support diverse applications.
- Focus is on land cover (not land use); 0.5 ha minimum mapping unit; some classes subdivided for spectral or habitat reasons.
- Consult the Final Report for comprehensive methodology and limitations (Morton et al., 2011).

## Data content and structure

- Vector Data Set
  - 8.6 million polygons for Great Britain, 0.9 million for Northern Ireland.
  - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class, 1-23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID for unambiguous communication; retain Parcel_ID in derived datasets.
  - Subclasses (BHSub) accompany class codes but may be less reliable than main LCM2007 classes; recommended validation if used for fine-grained analysis.

- Raster Data Sets
  - 25 m and 1 km products derived from the vector dataset.
  - Great Britain and Northern Ireland provided separately with appropriate projections.
  - 25 m: 23 LCM2007 classes (full thematic resolution).
  - 1 km: Aggregate classes; Dominant cover and Percentage cover products for both LCM2007 classes and Aggregates.

## Quality, validation, and limitations

- Validation
  - Ground reference data used to validate against spatial and thematic resolution; average accuracy ~83%; regional variations may occur.
- Spatial and thematic considerations
  - 0.5 ha minimum unit; smaller parcels dissolved.
  - LCM2007 maps land cover, not always directly inferable land use.
  - Broad Habitat subclasses provided (BHSub) primarily for information and ProbList; not guaranteed to meet QA standards; use with caution and validate as needed.
- Classification and knowledge-based enhancements
  - Some grassland, moorland, and montane classes have known mis-classifications; Neutral/Calcareous/Acid Grassland distinctions can be challenging.
  - Montane mappings rely on altitude in addition to spectral data; potential validity trade-offs.
- Data accuracy and limitations
  - Local discrepancies possible; global accuracy is an average across the dataset.

## Metadata, provenance, and documentation

- Rich metadata accompanies the vector product (processing history, polygon construction details, spectral classification, KBE history).
- Includes a ProbList showing top spectral variants per polygon and the CorePixels used for maximum likelihood classification.
- Appendix materials provide detailed mappings:
  - Appendix 1: LCM2007 classes (definitions and criteria).
  - Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode).
  - Appendix 3: Standard LCM2007 colour mapping (for visualization).

## Access, licensing, and usage

- Data access:
  - 1 km raster data via the CEH Information Gateway.
  - Full vector product and 25 m raster product available on request from CEH.
- Licensing and fees:
  - Licences may apply; contact CEH (spatialdata@ceh.ac.uk) or apply online.
- Reuse and attribution:
  - Acknowledgement to CEH/NERC and project partners; data derived from multiple sources (Landsat, SPOT, AWIFS, etc.) with appropriate permissions.

## Technical details

- Coordinate systems and projections
  - Great Britain: British National Grid (OSGB 1936) with Transverse Mercator projection.
  - Northern Ireland: Irish National Grid (with ongoing transition toward ITM).
- File sizes (guidance)
  - Vector shapefile (GB 100 km x 100 km sample): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: 21 MB to 49 KB depending on product.
- Data scale and complexity
  - ~10 attributes per vector polygon; large dataset requiring careful data handling.

## Data access and further information

- Primary references:
  - Morton et al., 2011. Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
  - Jackson, 2000. Guidance on interpretation of the Broad Habitat Classification.
- Additional information and contact:
  - CEH data portal and Information Gateway; licensing details via CEH.
  - For more, see the Countryside Survey website: www.countrysidesurvey.org.uk

## Appendices (summary)

- Appendix 1: LCM2007 Classes — detailed definitions and Broad Habitat associations (e.g., Broadleaved woodland, Coniferous woodland, Arable, Grasslands, Wetlands, Coastal/Built-up, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings, class numbers).
- Appendix 3: Standard LCM2007 colour mapping (RGB values per class) for visualization.