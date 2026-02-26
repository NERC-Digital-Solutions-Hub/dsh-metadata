# Broad Habitat Area Estimates by Land Class for Great Britain 1984 Version: 1: 22-11-2013 C.M. Wood, CEH Lancaster.

## Overview
- Countryside Survey 1984 estimates of Broad Habitat areas in Great Britain.
- National stock estimates (Habitats 1–17) for 1984 calculated using the 1998 ITE Land Classification.
- Outputs include total area by Broad Habitat per Land Class (in 000s ha) with lower and upper 95% confidence intervals.
- Datasets support monitoring of environmental health and policy performance over time.

## Data Files and Structure
- CS1984_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - Content: Mean area of Broad Habitat by Land Class, with lower and upper 95% confidence intervals; units are 000s ha.
- cs1984_stock.tif
  - A 1 km pixel raster where each band represents a Broad Habitat class; each pixel contains the mean percentage estimate of that habitat within the 1 km square.
  - Mapping details: Each band corresponds to a Broad Habitat in combination with Land Class (e.g., Broad Habitat 2 with Broad Habitat 1 mapped to Band 2; Broad Habitat 3 with Broad Habitat 1 mapped to Band 3; and so on through Band 17).
  - Pixel size: 1 km; Spatial reference: British National Grid (OSGB36), Transverse Mercator; extent: Great Britain.

## Spatial Reference and Usage Details
- Pixel size: 1,000 m; Coordinate system: British National Grid OSGB1936; Projection: Transverse Mercator.
- Data capture and interpretation are based on the 1 km survey squares sampled within each Land Class strata.
- The raster enables location-based visualization (maps) of habitat distribution and proportions across Great Britain.

## How to Use
- Use for national-scale habitat stock estimation and monitoring against standards or targets.
- Combine with other habitat datasets for broader environmental health assessments.
- Outputs suitable for reports, maps, and charts to illustrate habitat distribution and confidence intervals.
- Dataset use requires acknowledgement of Countryside Survey data owned by NERC-CEH; copyright restrictions apply.

## Relevance to Monitoring Aims
- Provides standardized, verifiable habitat area estimates across GB for 1984.
- Demonstrates environmental condition using a consistent Land Classification framework (ITE 1998).
- Supports time-series analysis by offering structured outputs (areas by habitat, per Land Class, with uncertainty).

## Practical Considerations for Analysts
- Value enhancement: integrate CS1984 habitat stock with other datasets (e.g., later Countryside Survey rounds) to assess trends and policy impact.
- Data accessibility: ensure underlying raster and tabular data are stored in appropriate data portals with proper metadata.
- Data quality: rely on defined confidence intervals and established methodologies (Bunce et al., 1996; 1998; Scott, 2007) for interpretation and QA.

## Acknowledgement and References
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data use must include copyright notice.
- Key references and context: Countryside Survey methodology and results papers (e.g., Carey et al. 2008; Scott 2007), ITE Land Classification literature (Bunce et al. 1996, 1998; Bunce et al. 1981), and related habitat guidance (Jackson 2000). Links and DOIs provided in the original dataset documentation.