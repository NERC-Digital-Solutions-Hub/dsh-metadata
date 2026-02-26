# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- National estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification.
- Estimates given as total lengths (metres) for each linear feature type per 1 km square per Land Class.
- Note: negative values may appear in LC2007 due to the statistical model; treat these as zero.
- Data includes geometry (Shape) and a set of attribute fields describing land class, year, and feature lengths.

## Data structure and key fields
- FID: Object ID; Feature ID (autonumber).
- Shape: Geometry; Shape_Length and Shape_Area provide geometric metrics.
- LC2007: Double; ITE Land Class (numeric).
- LC2007_COD: Text; ITE Land Class code (text code).
- CSYEAR: Number; Year of survey.
- LCAREA: Number; Total area of relevant Land Class (00s ha).
- LF_1: Number; Hedges; Length per 1 km square in metres.
- LF_3: Number; Wall; Length per 1 km square in metres.
- LF_4: Number; Line of trees/shrubs/relict hedge/fence; Length per 1 km square in metres.
- LF_5: Number; Line of trees/shrubs/relict hedge; Length per 1 km square in metres.
- LF_6: Number; Bank/grass strip; Length per 1 km square in metres.
- LF_7: Number; Fence; Length per 1 km square in metres.
- LFTOTAL: Number; Total length of all linear features (metres per 1 km square per land class).
- Shape_Length, Shape_Area: Geometry attributes describing the feature.

## Feature types and reporting rules
- Six major feature types are reported.
- No double counting: multi-element features are not double-counted; hedges have reporting precedence when alongside other features.
  - Hedges (LF_1) may accompany walls or fences, but lengths of walls/fences found with a hedge are not included in the hedge totals.
- The dataset provides hierarchical grouping and codes to enable reporting in different aggregations.

## Use and processing guidance for GIS
- Suitable for map-based visualization and spatial analysis by GIS professionals.
- Join with Land Classification (LC2007) and 1 km square data to contextualize by land class.
- Use CSYEAR to confirm the survey year and ensure alignment with other datasets.
- Handle LC2007 negative values by treating them as zero during analysis or visualization.
- When combining datasets, maintain the reporting hierarchy to avoid double counting.

## Limitations and data quality considerations
- Data corresponds to 1990 estimates derived from the 2007 ITE Land Classification; spatial resolution tied to 1 km square reporting.
- Data quality may be affected by:
  - Data compiled from multiple sources with potential inconsistencies or gaps.
  - The necessity to clean and transform data during integration.
  - Large or complex datasets requiring packaging into manageable chunks.
- Use limitations require appropriate acknowledgement in all outputs.

## Acknowledgement and licensing
- Use of Countryside Survey data must be acknowledged:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Include acknowledgement in all copies, publications, presentations, and data products.

## References and additional resources
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- Carey et al., 2008: Countryside Survey: UK Results from 2007.
- Scott, W.A. (2007): CS Technical Report No.4/07 Statistical Report.
- Bunce et al. (various): ITE Land Classification references and methodology.
- Related field handbooks and background reports available through NERC/CEH and associated repositories.