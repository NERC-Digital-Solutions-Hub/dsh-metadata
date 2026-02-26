# Countryside Survey Environmental Zones 2007

## Overview
- A GB-wide dataset of Environmental Zones (EZ) created by aggregating ITE Land Classes to report Countryside Survey results at a sub-GB level, above individual ITE classes.
- Zones are defined by combinations of environmental characteristics rather than a single parameter.
- Botswana: Northern Ireland is reported separately and not included in this GB dataset.

## Data details
- Columns: Envzone (zone number, numeric), Description (zone description, text)
- Resolution: 1 km
- Coordinate system / Projection: British National Grid (OSGB36), Transverse Mercator
- Extent: Great Britain
- Associated datasets: ITE Land Classification (2007); Countryside Survey (CS) dataset

## Content and zone structure
- The dataset represents 8 GB zones (EZ1–EZ6 and EZ8–EZ9); EZ7 corresponds to Northern Ireland and is not included in this GB dataset.
- Zone names reflect average environmental characteristics and hierarchical geographic splits across Scotland, England, and Wales:
  - EZ1 Easterly Lowlands (England)
  - EZ2 Westerly Lowlands (England)
  - EZ3 Uplands (England)
  - EZ4 Lowlands (Scotland)
  - EZ5 Intermediate Uplands and Islands (Scotland)
  - EZ6 True Uplands (Scotland)
  - EZ8 Lowlands (Wales)
  - EZ9 Uplands (Wales)
- Each zone is an aggregation of multiple ITE Land Classes (the specific class-to-zone mappings are provided in a supplementary table referenced in the document).

## Background and purpose
- Created to report Countryside Survey UK results (Carey et al., 2008) at a sub-GB level, enabling analysis beyond individual ITE Land Classes.
- Countryside Survey is a nationwide environmental survey of Great Britain, conducted at roughly 10-year intervals since 1978, based on a 1 km square sampling framework.

## Use in GIS and data integration
- Designed for map-based data visualisations to show spatial environmental patterns across GB at 1 km resolution.
- Useful for presenting survey results at a finer spatial scale than ITE classes but at a scale that remains aggregated by environmental characteristics.
- Requires alignment with ITE Land Classification data for full interpretation and mapping.

## Provenance and references
- Core background and method described in:
  - Barr (1998); Bunce et al. (1996)
  - Carey et al. (2008): Countryside Survey UK Results from 2007
  - Wood (2011): The Sampling Strategy for Countryside Survey (up to 2007)
- Document details:
  - Countryside Survey Environmental Zones 2007
  - Document version: 1:1-6-2013
  - Data held by CEH (Centre for Ecology & Hydrology) and attributed to NERC

## Additional notes
- The document references a table detailing which ITE Land Classes aggregate into each Environmental Zone, but the full mapping table is not included in the text provided.
- Northern Ireland data (EZ7) is reported separately and not included within this GB dataset.