# ITE Land Classification of Great Britain (1998)

- Overview
  - A shapefile dataset providing 1 km resolution land classifications for Great Britain.
  - Contains 40 land class areas, each defined by environmental characteristics (climate, altitude, slope) and mapped across GB.
  - Based on Countryside Survey data; data are credited to NERC – Centre for Ecology & Hydrology (CEH).

- Data content and structure
  - Format: Shapefile.
  - Spatial coverage: Great Britain (England, Wales, Scotland).
  - Resolution: 1 km.
  - Attributes:
    - LC1998: ITE Land Class Number (1998).
    - LC1998_COD: ITE Land Class Code (1998).
  - Spatial reference: British National Grid (OSGB36), Projection: Transverse Mercator.

- Spatial organization and class details
  - The dataset comprises 40 land classes, used to stratify GB by prevailing landform and environmental conditions.
  - England/Wales portion includes classes 1–24 (various landforms such as flood plains, flat plains, coastal plains, upland valleys, etc.) with codes like 1e, 2e, up to 24e.
  - Scotland portion comprises classes 25–40, detailing coastal/plains and upland/mountain landforms (e.g., coastal plains, upland valleys, round mountains, high summits, etc.).
  - Class descriptors cover a range of landform categories from low-lying floodplains to high mountain terrains.

- Use cases for GIS specialists
  - Map-based visualization of landscape types across GB for policy analysis, planning, conservation, or public-facing products.
  - Integration with other spatial datasets by joining on LC1998 or LC1998_COD to analyze landscape context, habitat suitability, or risk assessments.
  - Comparative analyses across regions (England/Wales vs Scotland) to examine landform distributions at the 1 km grid.

- Metadata and documentation
  - Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
  - Further reading and related documentation provided, including sampling strategies and classification validity:
    - Barr (1998); Wood (2011) on Countryside Survey sampling strategies.
    - Earlier and subsequent works on ITE land classification and applications in ecological survey contexts.

- Considerations and caveats
  - Data date: 1998; may require update or revalidation for current applications.
  - Data quality and standards: potential inconsistencies; substantial data cleaning/transforming may be needed for integration with other datasets.
  - Volume and complexity: 40 classes across GB; large datasets may need careful packaging for downstream use.