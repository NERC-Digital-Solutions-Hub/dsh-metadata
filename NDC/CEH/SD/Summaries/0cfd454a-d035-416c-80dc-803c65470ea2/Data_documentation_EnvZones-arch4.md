# Countryside Survey Environmental Zones 2007

- The dataset defines Environmental Zones (EZ) for Great Britain by aggregating ITE Land Classes to report Countryside Survey results at a sub-GB level, higher than individual ITE Land Classes.
- Zones are derived from multivariate analyses of environmental data collected for each 1km square, and are labeled EZ1 through EZ9 to reflect regional groupings.

## Data structure and technical details

- Columns:
  - Envzone: Zone number (numeric)
  - Description: Zone description (text)
- Spatial characteristics:
  - Resolution: 1 km
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Extent: Great Britain

## Background and data lineage

- Countryside Survey is a nationwide environmental survey of Great Britain conducted approximately every 10 years since 1978 by CEH; zones were created to enable reporting at a sub-GB level.
- ITE Land Classes (from the ITE Merlewood Land Classification) are aggregated into Environmental Zones based on environmental characteristics through repeatable multivariate analysis.
- A mapping table (referenced in the document) shows which ITE Land Class Numbers aggregate into each Environmental Zone.

## Geographic scope and naming

- Zones cover Great Britain and are hierarchical across the nations; there are three zones in Scotland, three in England, and two in Wales. Northern Ireland is reported separately and not included in this dataset.
- Zone names are:
  - EZ1 Easterly Lowlands (England)
  - EZ2 Westerly Lowlands (England)
  - EZ3 Uplands (England)
  - EZ4 Lowlands (Scotland)
  - EZ5 Intermediate Uplands and Islands (Scotland)
  - EZ6 True Uplands (Scotland)
  - EZ7 Northern Ireland (not included here)
  - EZ8 Lowlands (Wales)
  - EZ9 Uplands (Wales)

## Associated datasets and access

- Associated datasets:
  - ITE Land Classification (2007)
  - Countryside Survey (website)
- The dataset is linked to broader Countryside Survey products and publications (careful reference to the original sources is recommended for full reproducibility).

## Metadata, documentation, and governance

- Background documentation and references include:
  - Barr (1998) and its 2011 update on Countryside Survey sampling strategy
  - Bunce et al. (1996) on ITE Land Classification
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
- The document version is 1:1-6-2013, prepared by C.M. Wood (CEH Lancaster).
- For governance and reuse, maintain alignment with the ITE Land Classification mapping and Countryside Survey metadata to ensure consistency across time and partners. The naming and aggregation logic should be documented to support interpretation and interoperability.