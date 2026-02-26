# ITE Land Classification of Great Britain (2007)

## Overview
- A shapefile-based dataset defining 45 land classes across Great Britain, stratified by environmental characteristics (climate, altitude, slope).
- Used in broader Countryside Survey work and related ecological analyses.

## Dataset Details
- Format: Shapefile
- Extent: Great Britain
- Resolution: 1 km
- Coordinate system / Projection: British National Grid (OSGB36), Transverse Mercator
- Included fields:
  - LC2007: ITE Land Class Number (2007)
  - LC2007_COD: ITE Land Class Code (2007)

## Content and Classification
- Contains 45 land class areas, each with a descriptive code and description.
- Summary names cover England, Scotland, and Wales with region-specific coding (e.g., England, Scotland “s” codes, and Wales codes).
- The 45 classes map to diverse landform and habitat types across the country, with a detailed legend linking codes to descriptive names.

## Documentation and Provenance
- Supporting literature and methodological references accompany the dataset, including:
  - Barr (1998) and revised strategies by Wood (2011)
  - Several Bunce et al. papers (1991, 1996a, 1996b)
  - Howard, Barr, Scott (1998), Clarke et al. (2006)
- Extensive bibliographic references provide context for sampling strategies and validation within Countryside Survey.
- Supplied as part of broader ecological and land classification research.

## Considerations for Data Leaders
- Data governance and usability:
  - Ensure metadata captures the 1 km resolution, GB extent, OSGB36 projection, and shapefile format for discoverability.
  - Maintain versioning awareness: this is the 2007 version with its associated methodology and legend.
- Interoperability:
  - Align with other GB geospatial datasets by using the same projection and resolution where possible.
  - Use LC2007 and LC2007_COD fields to integrate with analytical workflows and downstream products.
- Usage and gaps:
  - Useful for landscape-scale analyses, land cover classification, and ecological planning.
  - Consider cross-referencing with updated or supplementary land classification schemes if newer data are required.