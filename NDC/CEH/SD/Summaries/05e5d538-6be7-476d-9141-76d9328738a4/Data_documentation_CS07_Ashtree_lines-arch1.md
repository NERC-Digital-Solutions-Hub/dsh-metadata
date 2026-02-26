# Countryside Survey: Ash tree distribution in woody linear features 2007

## Overview
- Provides estimates of ash trees in Great Britain within woody linear features, derived from Countryside Survey 2007 data.
- Aims to enable national-scale estimation by scaling sampled data from 1 km squares using land classifications that reflect major ecological gradients.
- Distinguishes between natural-shaped woody features (e.g., belts) and hedgerows (unnatural shapes) to estimate ash distribution.

## What the dataset contains
- Estimates of ash within woody linear features (WLFs) across Great Britain, derived from CS07 data.
- Columns describing land class and ash coverage/length within different feature types (hedgerows, belts, etc.).
- Resolution: 1 km; Extent: Great Britain; Coordinate system: British National Grid; Projection: Transverse Mercator.

## Data columns (key fields)
- LC2007: Land Class (numeric)
- LC2007_COD: Land Class (text)
- LC_2007: Land Class with no code for LCs where no hedges occur
- Size_of_LC: Area of Land Class (m2)
- WNS_km: Ash length in natural-shaped lines of trees (km) within land class
- WUS_km: Ash length in hedges/unnatural shapes (km) within land class
- Belt_km: Ash length in belts of trees (km) within land class
- All_WLF_km: Total ash length across WLF types (km)
- Mean_km_km: Mean length of all linear features per km2
- Extension: Dataset covers Great Britain with 1 km resolution

## Methodology and estimation approach
- Countryside Survey samples 1 km squares using stratified random sampling based on land classes (ecological gradients such as soils, geology, climate).
- Linear features include hedgerows, walls, and fences; minimum feature length is 20 m with up to 20 m gaps.
- Two Woody Linear Feature types:
  - Natural Shape: lines/belts of trees; ash proportion recorded in bands (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%, Individual Tree).
  - Unnatural Shape: hedgerows; ash proportion inferred for some cases via mixed-species categories.
- For lines of trees (natural shape), ash length per 1 km square is calculated using the band midpoints (e.g., 5%, 17.5%, 37.5%, 62.5%, 85%, 97.5%, 100%).
- For belts and hedges, the same approach is used; however, belts are treated as a separate feature type.
- For hedges with unnatural composition, ash estimation uses D plots (vegetation plots adjacent to hedges) that record total species cover; ash proportions are inferred by multiplying mean ash cover by the total hedge length in each strata.
- National ash estimates are obtained by multiplying 1 km square means by the area of each Land Class and summing across all classes.

## Scaling and geography
- National estimates are produced by:
  - Calculating 1 km square means within each Land Class stratum.
  - Multiplying these means by the Land Class area (m2) to scale to country total.
  - Summing across all Land Classes to produce GB-wide estimates.

## Associated datasets and references
- ITE Land Classification (2007): link provided for context and classification framework.
- Countryside Survey (main site): provides broader CS outputs and metadata.
- Key related publications and reports for methodology and results, including:
  - Distribution of Ash trees in Countryside Survey data (2013)
  - CS Sampling Strategy documents and related methodological papers
  - LCM2007 (UK land cover map) Final Report

## Practical notes for analysts
- Data enable correlations between ash distribution in woody linear features and ecological gradients captured by land classes.
- The approach accounts for different feature types (natural lines/belts vs hedgerows) and adapts ash estimation accordingly, which is important when analyzing the impact of management actions on ash distribution.
- Uncertainty arises from band-based proportions, use of adjacent vegetation plots (D plots) for hedges, and the assumption that 1 km square means are representative of Land Class areas.
- Data are designed to be discoverable and reusable, with metadata and links to source datasets.

## Usage guidance and cautions
- Suitable for estimating national-scale ash distribution in WLFs and exploring relationships with land-class variables.
- When linking to other datasets, ensure consistent spatial resolution (1 km) and the GB-wide geographic scope.
- Consider potential biases due to sampling design (stratified by land class) and the treatment of mixtures in hedgerows.