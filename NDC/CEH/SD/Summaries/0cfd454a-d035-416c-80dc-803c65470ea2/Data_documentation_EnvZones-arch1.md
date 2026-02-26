# Countryside Survey Environmental Zones 2007

## Overview
- A GB-wide spatial dataset of Environmental Zones (EZ) created by aggregating ITE Land Classes to enable reporting at a sub-GB level above individual ITE classes.
- Based on 1 km square environmental data from the Countryside Survey (repeated ~10-year intervals since 1978 by CEH).
- NI is reported separately; the GB dataset comprises eight Environmental Zones.

## Data Content and Structure
- Columns:
  - Envzone: Zone number (numeric)
  - Description: Zone description (text)
- Associated datasets:
  - ITE Land Classification (2007)
  - Countryside Survey (main dataset and results for 2007)
- Spatial resolution: 1 km
- Extent: Great Britain (GB)
- Coordinate system / Projection: British National Grid (OSGB36), Transverse Mercator
- File scope: Eight GB Environmental Zones (NI EZ7 excluded; NI reported separately)
- Zones included (GB): EZ1, EZ2, EZ3, EZ4, EZ5, EZ6, EZ8, EZ9
  - EZ1 Easterly Lowlands (England)
  - EZ2 Westerly Lowlands (England)
  - EZ3 Uplands (England)
  - EZ4 Lowlands (Scotland)
  - EZ5 Intermediate Uplands and Islands (Scotland)
  - EZ6 True Uplands (Scotland)
  - EZ8 Lowlands (Wales)
  - EZ9 Uplands (Wales)

## Background and Construction
- Environmental Zones were created to report Countryside Survey results at a sub-GB level, above the 45 ITE Land Classes.
- ITE Land Classes are derived from repeatable multivariate analysis of environmental data for each 1 km square; zones are aggregations of these classes.
- The naming of zones is not tied to a single parameter; zones are hierarchical across Scotland, England, and Wales, with names derived from analysis of average environmental characteristics.
- Details of aggregations and the mapping from ITE Land Classes to Environmental Zones are provided in accompanying tables (not reproduced in this document).

## How to Use for Analysis
- Use Envzone (numeric) as a key to join with Countryside Survey results and other environmental attributes at the zone level.
- Compare environmental and ecological indicators across zones (e.g., habitat types, land cover, biodiversity metrics) at 1 km resolution.
- Consider cross-border comparisons (England, Scotland, Wales) within the eight GB zones, noting that NI is outside this dataset.
- Leverage associated ITE Land Classification data for deeper disaggregation or repeated analyses across time.

## Data Quality and Limitations
- Zones are aggregates of ITE Land Classes, so intra-zone variation exists and there is a loss of fine-grained detail.
- Data reflect the 2007 Countryside Survey period; temporal comparisons require caution or additional time-series data.
- Access to the full zone-to-ITE mappings and table details is referenced but not included here; users should consult the associated datasets for exact class-to-zone mappings.

## Documentation and References
- Related sources:
  - Barr (1998) The Sampling Strategy for Countryside Survey
  - Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
- Datasets:
  - ITE Land Classification (2007)
  - Countryside Survey (website: www.countrysidesurvey.org.uk)

## Practical Considerations for Analysts
- Ensure alignment of coordinate systems when joining with other spatial data (OSGB36 vs. other projections).
- Be mindful of the 1 km resolution when aggregating to finer scales or interpreting zone-level summaries.
- Use zone descriptions to interpret ecological or environmental context and tailor analyses to zone-specific characteristics.