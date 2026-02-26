# Countryside Survey Environmental Zones 2007

## Overview
- Purpose: Provide a sub-GB level reporting framework for Countryside Survey results, aggregating environmental data into zones higher than individual ITE Land Classes.
- Context: Countryside Survey is a nationwide environmental survey of Great Britain conducted by the CEH, repeated about every 10 years since 1978, based on 1km squares.
- Focus: Zones are derived from combinations of environmental characteristics via multivariate analysis of ITE Land Classes.

## Data Content and Structure
- File scope: Contains 8 Environmental Zones for Great Britain, created by aggregating ITE Land Classes (2007) to enable reporting at a finer scale than ITE classes but broader than individual classes.
- Dataset linkages: Associated with ITE Land Classification (2007) and Countryside Survey data.
- Core columns:
  - Envzone: Zone number (numeric)
  - Description: Zone description (text)
- Scale and extent:
  - Resolution: 1 km
  - Coordinate system: British National Grid (OSGB36)
  - Projection: Transverse Mercator
  - Extent: Great Britain

## Methodology
- Zones are aggregations of ITE Land Classes, which themselves come from repeatable multivariate analyses of environmental data collected for each 1km square.
- The Consolidation into zones is based on environmental characteristics, rather than single parameters (e.g., altitude alone).

## Zone Naming and Coverage
- The dataset presents nine GB Environmental Zones (named to reflect averaged environmental characteristics) with hierarchical national context:
  - EZ1 Easterly Lowlands, England
  - EZ2 Westerly Lowlands, England
  - EZ3 Uplands, England
  - EZ4 Lowlands, Scotland
  - EZ5 Intermediate Uplands and Islands, Scotland
  - EZ6 True Uplands, Scotland
  - EZ7 Northern Ireland (reported separately, not included in this dataset)
  - EZ8 Lowlands, Wales
  - EZ9 Uplands, Wales

## Data Sources and References
- ITE Land Classification (2007)
- Countryside Survey ( GB results, Carey et al., 2008)
- Background and methodological references detailing the sampling strategy and ITE classifications (Barr 1998; Bunce et al. 1996; Barr et al. 1998; CEH references)

## Usage, Access, and Practical Considerations
- Purpose-driven use: Facilitates reporting of Countryside Survey results at sub-GB scales and supports cross-zone comparisons for environmental health and policy assessments.
- Data stewardship: Zone definitions and outputs are stored and uploaded to appropriate data portals; underlying ITE Land Classifications and Countryside Survey datasets are associated for deeper analysis.
- Key challenges for analysts: 
  - Increase the value of datasets by combining zones with other relevant data.
  - Enable access to underlying data used to create the final zone outputs.