# ITE Land Classification of Great Britain (1990)

## Overview
- A shapefile dataset covering Great Britain, partitioned into 32 Land Classes (LAND CLASS: ONE to LAND CLASS: THIRTY-TWO).
- Each area is defined by broad environmental characteristics used to classify land into distinct classes.
- The dataset is derived from Countryside Survey data (ITE/NERC) and includes a single attribute LC1990 that stores the Land Class Number (1990).
- Extent: Great Britain; Resolution: 1 km; Coordinate system: British National Grid; Projection: Transverse Mercator (OSGB36).

## Data Content and Structure
- Format: Shapefile.
- Extent and coverage: 32 land-class areas across Great Britain, including regions such as Southern England, Wales, Northern England, Scotland, and coastal zones.
- Attribute schema: LC1990 – ITE Land Class Number (1990).
- Descriptive content: Each Land Class (ONE to THIRTY-TWO) comes with a detailed description covering:
  - Geography
  - Land form
  - Topography
  - Landscape
  - Land use
  - Soils
  - Vegetation
- Geographic scope encompasses a wide range of environments from lowland cereals and pasture to upland moorlands, fens, downlands, coasts, and urban-influenced landscapes.
- The document provides extensive narrative descriptions for all 32 Land Classes (e.g., lowland mixed landscapes, downland, fenland, coastal margins, upland moorlands, and arable-dominated regions).

## Land Class Descriptions (Key Characteristics)
- 32 classes span the full gradient from lowland agricultural plains to high-altitude uplands and remote coasts.
- Class narratives include variations in:
  - Regions (e.g., Southern England, Wales, East Anglia, Northern Scotland)
  - Land forms (e.g., alluvial plains, downs, fens, upland plateaux, coastal cliffs)
  - Topography (altitude ranges and slope characteristics)
  - Landscape features (hedgerows, forests, urban influence, moorland)
  - Land use (arable crops, cereals, pasture, good grassland, urban)
  - Soils (gley soils, brown earths, gleys, peats, podsols)
  - Vegetation (ranging from limited vegetation to bracken, moorland, rough grassland, and peatland)
- Examples (illustrative, not exhaustive):
  - Land Class One: southern lowland with cereals and grassland.
  - Land Class Seven: variable coastal morphology with pasture and some arable.
  - Land Class Nineteen, Twenty, Twenty-Two: upland rough grazing and moorland types.
  - Land Class Thirty-One and Thirty-Two: windswept coastal and upland moorland environments.

## Provenance and References
- Based on Countryside Survey data (ITE – Institute of Terrestrial Ecology; Countryside Survey)
- Supporting documentation and literature cited include:
  - Barr (1998) on sampling strategy
  - Bunce et al. (1991, 1996) on land classification and ecological surveys
  - Howard, Barr, and Scott (1998) on sampling validity
  - Clarke, Howard, and Scott (2006) on Wales-only reporting
- These references provide methodology, validation, and contextual grounding for the Land Classification scheme.

## Potential GIS Applications
- Map-based visualization of land classification across Great Britain for policy, planning, and public communication.
- Landscape and ecological analyses by overlaying LC1990 with other spatial layers (habitat, soils, vegetation, climate, urban areas).
- Historical or comparative studies using the 1990 classification to assess changes over time when combined with newer datasets.
- Support for regional planning, biodiversity assessments, and environmental reporting.

## Practical Considerations and Challenges
- Temporal relevance: classification reflects conditions circa 1990; may not reflect current land-use or landscape changes.
- Data integration: one dataset with 32 classes; harmonization needed when integrating with other land-cover or GIS layers.
- Resolution: 1 km squares; suitable for broad-scale analysis but not fine-grained mapping.
- Data standards: alignment with other datasets requires attention to coordinate systems and attribute schemas.
- Data access and provenance: explicitly tied to Countryside Survey products and related methodological literature.

## How to Use in GIS
- Access as a shapefile with LC1990 as the primary attribute indicating the Land Class.
- Use the LC1990 field to symbolise or colour-code GB-wide polygons by land class.
- Refer to the accompanying Land Class narratives for domain knowledge when interpreting classifications.
- Combine with ancillary layers ( soils, vegetation, topography, urban areas) to produce informative map products for policy, clients, or the public.