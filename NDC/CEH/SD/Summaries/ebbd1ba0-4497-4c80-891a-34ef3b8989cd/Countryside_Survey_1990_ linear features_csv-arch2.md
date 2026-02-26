# Dataset Documentation

## Purpose and scope
- Provides national estimates of landscape linear feature stock for 1990 using the 2007 ITE Land Classification.
- Outputs are total lengths by feature type and Land Class, expressed in 000s km, with lower/mean/upper 95% confidence estimates.
- Includes Land Class areas (00s ha) and the related reporting framework that avoids double counting.

## Data structure and fields
- Key fields:
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class (text)
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI for feature length (000s km)
  - MEAN_ESTIMATE: Mean feature length (000s km)
  - UPPER_ESTIMATE: Upper 95% CI for feature length (000s km)
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)
- Note: MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as zero.

## Linear feature codes and definitions
- _1 Hedge: Managed line of woody vegetation; hedges may accompany other features and have reporting precedence.
- _3 Wall: Built stone/manufactured wall; may include associated fences or streams but reports separately from hedges.
- _4 Line of trees/shrubs/relict hedge/fence: Line of trees/shrubs (natural shape or former hedges with fences).
- _5 Line of trees/shrubs/relict hedge: Line of trees/shrubs; may include avenues; can include banks/grass strips.
- _6 Bank/grass strip: Bank or grass strip with/without a fence.
- _7 Fence: Permanent post/rail/board fence with or without adjacent grass strip, ditch, or stream.
- TOTAL: Total length of linear features.
- Important reporting rule: Features are reported hierarchically with no double counting; hedges take precedence when co-occurring with walls or fences.

## Reporting methodology and data provenance
- Based on field survey data recorded as a set of detailed codes, enabling flexible reporting by code combinations.
- Six major feature types are reported, with careful separation to avoid overlap.
- Reporting framework prioritizes ecological relevance of hedges.

## Use limitations and acknowledgement
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement and copyright notice: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Use in publications, presentations, and data portals should include the above statements.

## Access, documentation, and references
- Countryside Survey Website provides project overview, methodologies, and links to documents.
  - http://www.countrysidesurvey.org.uk/
- Key references include:
  - Carey et al. 2008: Countryside Survey UK Results from 2007
  - Barr et al. 1993: Countryside Survey 1990 main report
  - Scott 2007: CS Technical Report No.4/07 Statistical Report
  - Bunce et al. 1996/2007: ITE Land Classification publications
- Data provenance notes: explains how national estimates are generated from 1 km survey squares and the ITE Land Classification framework.

## Implications for environment monitoring
- Useful for monitoring changes in landscape linear features over time by standardised units and classifications.
- Facilitates cross-dataset analyses by providing standardized feature codes and accompanying land-class context.
- Aligns with the Analysts Monitoring the Environment approach through:
  - Data verification, quality assurance, cleaning, and transformation steps (implied by structured fields and CI estimates).
  - Standardised outputs (tables, codes, and classifications) suitable for reporting, mapping, and portal uploads.
  - Emphasis on data accessibility and enabling downstream use of underlying data beyond final outputs.