# Geological map of the Moor House National Nature Reserve (1963)

## Overview
- Shapefile MH_Geology.shp containing polygons of rock types mapped in the 1950s/1960s.
- Originally published as part of The Geology of Moor House, a National Nature Reserve (1963).
- Digitized in the 1990s by the Institute of Terrestrial Ecology (now the Centre for Ecology & Hydrology).

## Dataset Details
- Format: Shapefile
- Content: Polygons representing rock types mapped in the 1950s/1960s; linked to a rock-type taxonomy and geological era.
- Columns:
  - GEOLOGY_ID: numeric, arbitrary unique code per polygon
  - GEOLOGY: text, description of rock type
  - ERA: text, geological era
- Spatial reference: British National Grid (OSGB1936)
- Projection: Transverse Mercator
- Extent: Great Britain
- Original map scale/resolution: 3 minutes to a mile

## Mapped Rock Types
- ROCK-TYPE CATEGORIES (examples):
  - ALLUVIAL FAN
  - FRESHWATER ALLUVIUM
  - LIMESTONE UPPER / LIMESTONE MIDDLE / LIMESTONE LOWER / LIMESTONE
  - BASEMENT GROUP
  - SKIDDAW SLATE SERIES
  - SANDSTONE
  - QUARTZ DOLERITE (Great Whin Sill)
  - WATER
- Each type is accompanied by a descriptive entry and, where applicable, an ERA descriptor.

## Provenance and History
- Moor House National Nature Reserve established in 1951.
- Detailed geological work and re-survey conducted starting 1954; results published in 1963 (Johnson & Dunham).
- Digitization conducted in the 1990s by the Institute of Terrestrial Ecology (now CEH).

## Geological Context
- Exposes almost the complete Carboniferous stratigraphic succession of the northern Pennines within the Reserve.
- Key features include:
  - Continuous upper Carboniferous sequence on Great Dun Fell
  - Western escarpment outcrops and east-dipping benches
  - Lower Palaeozoic basement rocks (Cross Fell Inlier) nearby
  - Great Whin Sill (quartz-dolerite) exposures within the Reserve
  - Mineral veins (lead, zinc, fluorite, barytes) visible in the Reserve
  - Glacial deposits (boulder clay, morainic gravel) and peat deposits throughout

## Data Quality and Metadata Considerations for Monitoring Frameworks
- Metadata scope is limited to field codes and descriptions; explicit data quality indicators (accuracy, precision, date of capture, QA procedures) are not provided.
- Data lineage is documented (original map from 1963; digitized in the 1990s), but there is no explicit metadata detailing digitization methods or transformation steps.
- Scale/Resolution is historical (3' to a mile), which may affect current applicability for fine-grained monitoring.
- Access and sharing considerations are not detailed; dataset is provided as a shapefile with georeferencing in OSGB36.

## Uses for Monitoring and Management
- Informing geological and soil contexts within Moor House NNR for environmental health assessments.
- Supporting habitat, erosion, and land-use planning with historical lithology context.
- Providing a baseline for historical geologic conditions to compare against newer surveys.
- Useful for data governance planning: highlights need for explicit QA, metadata enrichment, data provenance, and openness when reused for monitoring decisions.

## References and Further Reading
- The Geology of Moor House, a National Nature Reserve in north-east Westmorland (Johnson & Dunham, 1963), Monographs of the Nature Conservancy No.2
- Environmental Change Network (contextual reference): http://data.ecn.ac.uk/sites/ecnsites.asp?site=T04