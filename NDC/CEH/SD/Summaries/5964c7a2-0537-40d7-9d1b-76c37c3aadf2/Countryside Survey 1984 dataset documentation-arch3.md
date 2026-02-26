# Broad Habitat Area Estimates by Land Class for Great Britain 1984

## Overview
- Countryside Survey 1984 estimates of Broad Habitat areas in Great Britain, providing national stock (Habitats 1–17) for 1984.
- Calculations use the 1998 ITE Land Classification; results reported as total area in thousands of hectares per Broad Habitat and Land Class, including 95% confidence intervals (lower and upper estimates).
- Two data products accompany the estimates: a CSV stock file and a 1 km pixel TIFF raster with per-pixel mean habitat percentages.

## Data Files and Structure
- CS1984_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha).
- cs1984_stock.tif (1 km resolution)
  - Each 1 km pixel contains a mean percentage estimate of habitat presence for a given Broad Habitat class.
  - Band-to-Habitat mapping clarifies which band corresponds to which Broad Habitat (e.g., Band 2 = Broad Habitat 2 under certain Land Class combinations; detailed mappings provided).

## Spatial Dimensions and Classification
- Spatial reference: British National Grid (OSGB36), Transverse Mercator projection.
- Spatial resolution: 1 km pixels (1000 m).
- Extent: Great Britain.
- Land Classification: ITE Merlewood Land Classification (used to derive the Broad Habitat categories).
- Broad Habitats covered: 1–17, with descriptive names tied to the 2000s biodiversity framework (as referenced).

## How to Use for Monitoring Frameworks
- Provides a 1984 baseline of Broad Habitat areas by Land Class for trend analyses and monitoring policy outcomes.
- Enables aggregation of habitat areas across Land Classes or per Broad Habitat for UK-wide or GB-wide monitoring.
- The raster product supports spatial analyses at 1 km scale, including habitat distribution mapping and change detection when combined with future datasets.
- Confidence intervals (lower/upper estimates) support uncertainty assessment in monitoring results.

## Data Quality, Metadata, and Governance
- Data are tied to established Countryside Survey methodologies and publications; metadata and methodological references are provided.
- Potential data quality considerations for monitoring:
  - The 1984 baseline is based on the 1998 Land Classification scheme, which may affect comparability with later datasets.
  - The raster relies on sampling within Land Class strata; pixel-level estimates are band-specific.
- Acknowledgement and use restrictions:
  - Countryside Survey data must be acknowledged; data are © NERC–CEH; all rights reserved.

## Access, Licensing and Acknowledgement
- Data usage requires acknowledgement: Countryside Survey data owned by NERC - CEH.
- Publication and presentations should include the specified acknowledgement.

## References and Context
- Key publications and methodological references linked to the dataset (e.g., Scott 2007; Bunce et al. 1998; Jackson 2000) provide the background for the Land Classification and habitat interpretations.
- Links and citations are provided for further methodological detail and context on the Countryside Survey framework and its 2007 UK results.

## Practical Considerations for Monitoring Framework Authors
- Use as an 1984 GB baseline for broad habitat area across Land Classes to support long-term environmental health monitoring.
- Combine with subsequent surveys to evaluate habitat change over time; be mindful of changes in classification schemes when linking across years.
- Leverage the CSV for tabular area estimates and the TIFF raster for spatially explicit analyses and visualization.
- Ensure proper governance, metadata alignment, and open data practices when integrating into monitoring reports or dashboards.