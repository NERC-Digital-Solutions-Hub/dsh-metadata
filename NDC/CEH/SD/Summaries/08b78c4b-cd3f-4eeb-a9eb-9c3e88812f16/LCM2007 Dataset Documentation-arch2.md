# Land Cover Map 2007 Dataset documentation

## Overview
- UK-wide parcel-based land cover classification (LCM2007) using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Derived from summer–winter satellite composites at 20–30 m resolution; upgrades from LCM2000 with OSMM-based spatial framework.
- Distinguishes land cover (not strictly land use); minimum mapping unit is >0.5 ha; parcels under 0.5 ha or linear features <20 m are dissolved.
- Some Broad Habitats are subdivided for more detail (e.g., Built-up Areas and Gardens into Suburban/Urban).

## Key features and considerations
- Rich metadata and provenance for polygons; unique Parcel_ID for each parcel, linking to source imagery.
- Classes are validated at the 23-class level; Broad Habitat sub-classes (BHSub) are included but may require independent validation for sub-class use.
- Knowledge-based enhancements (KBE) applied during classification; ProbList provides top 5 spectral-class probabilities for each polygon.
- Validation against ground reference data (9127 polygons) yields an average accuracy of about 83%, with regional variations possible.

## Data products

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class number 1–23), KBE, ProbList, CorePixels, Construct, TotPixels.
  - BHSub and FieldCode offer additional detail but are not QA-validated for accuracy; users should validate before applying sub-class information.
  - Includes a comprehensive construction history and metadata per polygon (e.g., source image, segmentation method).

- Raster Data Sets
  - 25 m and 1 km raster products derived from the vector dataset.
  - 25 m: 23 LCM2007 classes; pixel values correspond to class numbers.
  - 1 km: derived by summarising 25 m data to produce:
    - Dominant cover at 1 km for LCM2007 classes
    - Dominant cover at 1 km for Aggregate classes
    - Percentage cover at 1 km for LCM2007 classes
    - Percentage cover at 1 km for Aggregate classes
  - GB and NI datasets provided separately due to different projections.

- File size and projections
  - Vector (GB 100 km × 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster 25 m (GB): ~1.36 GB; NI ~46 MB.
  - 1 km rasters: smaller sizes (dominant/percentage products).
  - Projections: GB National Grid (OSGB 1936) for GB; Irish National Grid for NI (with NI moving toward ITM in some products).

## Data access and licensing
- 1 km raster data available via CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; licence fees may apply.
- Application process via CEH website or contact spatialdata@ceh.ac.uk.

## Data structure and usage guidance
- LCM2007 maps land cover (not land use); interpretation should consider potential ambiguities (e.g., grass used for recreation vs. grazing).
- Use the 23-class resolution for detailed analyses; 1 km rasters provide aggregated views suitable for national-scale modelling or integration with other national datasets.
- The standard colour mapping (Appendix 3) is provided for visualization; the Appendix 2 relationships help connect Broad Habitats to LCM2007 classes and sub-classes.
- Northern Ireland grids may require reprojection for some GIS workflows; NI data are transitioning toward ITM.

## Appendix highlights

- Appendix 1: LCM2007 Classes
  - Provides concise definitions and examples for each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral/Calcareous/Acid Grassland, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Saltwater, Freshwater, Supra-littoral/Rock/Sediment, Littoral Rock/Sediment, Saltmarsh, Built-up Areas and Gardens split into Urban/Suburban).
  - Notes on cross-class ambiguities and practical considerations for classification (e.g., grassland subtypes, bog vs. heath, Montane vs. other habitats).

- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Maps Broad Habitat groupings to LCM2007 class numbers and sub-classes (e.g., Broadleaved woodland → Broadleaved woodland; Arable and Horticulture; Rough Grassland → Neutral/Calcareous/Acid Grassland via KBE; Heather vs Heather grassland; Saltmarsh sub-classes; Urban vs Suburban).
  - Helps users understand how LCM2007 classes align with broader habitat concepts.

- Appendix 3: Colour mapping
  - Provides the RGB color codes used for each LCM2007 class (for visualisation in maps and reports).

## Further information
- Morton et al. 2011: Final Report for LCM2007 – The New UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
- Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification (for cross-walking classifications and understanding Broad Habitats).

## Guidance for Analysts
- Use LCM2007 for consistent, standards-based environmental monitoring and policy performance over time.
- Leverage vector data for detailed, attribute-rich analyses, and raster data for scalable national or regional analyses.
- Validate Broad Habitat sub-classes when applying them in analyses requiring high accuracy.
- Consider data licensing and access procedures when planning large-scale or recurrent analyses.