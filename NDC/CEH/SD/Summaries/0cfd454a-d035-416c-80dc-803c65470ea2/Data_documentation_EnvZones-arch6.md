# Countryside Survey Environmental Zones 2007

## Overview
- Eight Environmental Zones (EZs) across Great Britain created by aggregating ITE Land Classes for Countryside Survey reporting at a sub-GB level higher than individual ITE classes.
- Zones are based on combinations of environmental characteristics and are used to report survey results at a finer scale than the ITE classes.

## Data and Structure
- Dataset columns: Envzone (zone number, numeric) and Description (zone description, text).
- Spatial resolution: 1 km.
- Extent: Great Britain.
- Spatial reference: British National Grid (OSGB36), Projection: Transverse Mercator.

## Background and Methodology
- Countryside Survey is a nationwide environmental survey of GB, repeated about every 10 years since 1978, using a 1 km square sampling framework.
- Environmental Zones were created to enable reporting at a sub-GB level beyond the 45 ITE Land Classes.
- ITE Land Classes are derived from multivariate analysis of environmental data for each 1 km square; zones represent aggregations of these classes.
- The document references a table detailing which ITE Land Classes map to each Environmental Zone.

## Zone Naming and Structure
- Zone names are derived from analysis of average environmental characteristics and are not tied to a single parameter.
- Hierarchical structure spans Scotland, England, and Wales, with EZs as follows:
  - EZ1 Easterly Lowlands (England)
  - EZ2 Westerly Lowlands (England)
  - EZ3 Uplands (England)
  - EZ4 Lowlands (Scotland)
  - EZ5 Intermediate Uplands and Islands (Scotland)
  - EZ6 True Uplands (Scotland)
  - EZ7 Northern Ireland (not included in this dataset)
  - EZ8 Lowlands (Wales)
  - EZ9 Uplands (Wales)

## Practical Use and Considerations for Data Support
- Designed to enable sub-GB reporting and cross-walks with ITE classifications; suitable for dashboards, pivot analyses, and self-serve data exploration.
- Zone definitions depend on environmental characteristics and may require referencing the ITE-to-Zone aggregation table for reproducibility.
- Ensure spatial alignment with other GB datasets using OSGB36 coordinates.
- Documentation version: 1:1-6-2013; dataset prepared by CEH Lancaster.
- Associated datasets: ITE Land Classification (2007); Countryside Survey dataset (main portal).

## Associated Data and References
- ITE Land Classification (2007) (associated dataset)
- Countryside Survey (UK results from 2007)
- Key references for background and methodology:
  - Carey et al. (2008)
  - Barr (1998)
  - Bunce et al. (1996)
  - Sampling strategy documentation (Barr 1998; Wood 2011)