# Dataset Documentation

- National estimates of landscape linear feature stock for 1984 calculated using the 2007 ITE Land Classification.
- Estimates reported as total lengths in thousands of kilometers (000s km) per Land Class, including lower and upper 95% confidence limits.
- Data type fields include YEAR, LAND_CLASS, FEATURENO, FEATURE, LOWER_ESTIMATE, MEAN_ESTIMATE, UPPER_ESTIMATE, and LAND_CLASS_AREA (area in hundreds of hectares).

## Content and Data Structure

- YEAR: Year of Survey (1984 for this dataset).
- LAND_CLASS: ITE Land Class (as per Bunce et al., 2007; Bunce et al., 1996).
- FEATURENO: Linear feature code (codes listed below).
- FEATURE: Description of the linear feature.
- LOWER_ESTIMATE: Lower 95% confidence interval for feature length (000s km).
- MEAN_ESTIMATE: Mean estimated length for the feature (000s km).
- UPPER_ESTIMATE: Upper 95% confidence interval for feature length (000s km).
- LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha).

## Linear Feature Codes and Reporting

- _1 = Hedge: A line of woody vegetation managed to alter natural shape; hedges may accompany other features.
- _3 = Wall: Built structure of stone or blocks; may include walls with fences or banks/grass strips.
- _4 = Line of trees/shrubs/relict hedge/fence: Trees/shrubs in natural shape; may include banks/grass strips.
- _5 = Line of trees/shrubs/relict hedge: Line of trees/shrubs; may include avenues and banks/grass strips.
- _6 = Bank/grass strip: Earth or stone-faced bank or grass strip with or without a fence.
- _7 = Fence: Permanent post-and-wire/rail structure; may be alongside grass strips, ditches, or streams.
- TOTAL: Total length of linear features.
- Reporting framework avoids double counting for multi-element features; hedges take precedence in reporting when found with other features.
- Six major feature types are reported; reporting is hierarchical with careful handling of overlaps.

## Data Quality, Use, and Limitations

- Use of CS data requires acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Copyright and rights: Countryside Survey © NERC-CEH; all rights reserved.
- Note: Negative values may appear in the MEAN_ESTIMATE column due to the statistical model; treat negatives as zero.
- Year 1984 estimates are derived using the 2007 ITE Land Classification methodology.
- Data may be accessed alongside accompanying Documentation and methodologies via the Countryside Survey Website and related published reports.

## Access, Attribution, and References

- Countryside Survey Website: general overview and links to relevant documents and methodologies.
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007.
  - Scott, W.A. (2007) CS Technical Report No.4/07 Statistical Report.
  - Bunce et al. (1996, 2007) ITE Land Classification publications.
- Related datasets: ITE Land Classification 2007 vector dataset; historical methodological handbooks and reports.

## Practical Considerations for Data Leaders

- Assess data availability and gaps for landscape linear features, especially at required granularity.
- Leverage metadata and classification schemes (ITE Land Classification) to contextualize analyses.
- Plan for data governance: ensure proper acknowledgment, metadata discoverability, and clarity on units and confidence intervals.
- Be mindful of potential data access barriers (paywalls, licensing) and coordinate with data stewards for broader sharing within permissible terms. 
- Consider user needs (policy colleagues, researchers) and support co-ownership and iterative use of data products.