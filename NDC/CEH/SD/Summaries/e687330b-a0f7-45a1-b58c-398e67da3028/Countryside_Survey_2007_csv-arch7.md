# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology National estimates of landscape linear feature stock (as listed below) for 2007 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007).   Estimates are given as total lengths in '000s km for each linear feature type per Land Class including lower and upper confidence limit estimates.

## Overview
- Provides national estimates (for 2007) of landscape linear features using the 2007 ITE Land Classification.
- Estimates are presented as total lengths by Land Class, with 95% confidence intervals (lower, mean, upper).
- Units: lengths in thousands of kilometers ('000s km) per feature type and Land Class; Land Class Area given in hundreds of hectares (00s ha).

## Data fields
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class (text)
- FEATURENO: Linear feature code (text)
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% CI of feature length (000s km)
- MEAN_ESTIMATE: Mean length estimate (000s km)
- UPPER_ESTIMATE: Upper 95% CI of feature length (000s km)
- LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)

Notes:
- MEAN_ESTIMATE may contain negative values due to the statistical model; treat negative values as zero.

## Linear feature codes
During field survey, information about Linear Landscape Features was recorded as codes. Reporting uses a hierarchical system of classes. No double counting occurs for multi-element features.

- _1 = Hedges: A line of woody vegetation managed so trees no longer take natural shape; hedges may be present with other features below (also known as "managed" hedgerows).
- _3 = Wall: Built structure of natural stone or blocks; may include walls with fences or banks/grass strips and/or lines of trees/shrubs.
- _4 = Line of trees/shrubs/relict hedge/fence: Trees/shrubs in natural shape; may include banks/grass strips; may include hedges originally planted with a fence.
- _5 = Line of trees/shrubs/relict hedge: Trees/shrubs in natural shape; includes avenues of trees; may include banks/grass strips.
- _6 = Bank/grass strip: Earth or stone-faced bank or grass strip with or without a fence.
- _7 = Fence: Permanent post-and-wire/rail structure; may include grass strip, ditch or stream; fences can be of various materials.
- TOTAL: Total length of all linear features.

## Reporting and data integrity
- Features are reported in a six major-type hierarchy with no double counting of multi-element features.
- When hedges are present with walls or fences, hedge lengths are reported separately; wall/fence lengths do not include portions found with hedges.
- Hedges are given reporting precedence due to ecological/policy relevance.

## Use limitations and acknowledgement
- All use of Countryside Survey (CS) data must be acknowledged.
- Required acknowledgement text: "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" along with copyright notice.
- Data are © Countryside Survey; all rights reserved.

## Data provenance and references
- Countryside Survey Website: General overview and methodologies (http://www.countrysidesurvey.org.uk/)
- Carey et al. (2008): Countryside Survey: UK Results from 2007
- Scott (2007): CS Technical Report No.4/07 Statistical Report (how national estimates are derived from 1 km survey squares)
- Bunce et al. (1996, 2007): ITE Land Classification of Great Britain; ITE Land Classification 2007 vector dataset
- CS Technical Report No.1/07: Field Mapping Handbook (Habitat Mapping Methodology)

## GIS usage considerations
- Data designed for map-based visualization of landscape features; suitable for integration with other spatial datasets at the national scale.
- Use the 2007 ITE Land Classification framework to align with other CS products.
- Be mindful of potential negative mean estimates; apply a zero floor where appropriate.
- Units are in 000s km for feature lengths and 00s ha for land-class area; ensure consistent unit handling when combining with other datasets.
- Consider data provenance and citation requirements when publishing or presenting map products.