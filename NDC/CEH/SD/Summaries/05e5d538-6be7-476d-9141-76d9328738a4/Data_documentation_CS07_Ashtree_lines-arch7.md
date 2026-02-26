# Countryside Survey: Ash tree distribution in woody linear features 2007

## Overview
- GB estimates of ash trees within woody linear features, derived from Countryside Survey 2007 data.
- File: CS07_Ashtree_Linears; data support map-based analysis of ash distribution in hedgerows and related linear features.

## Data content and structure
- Columns:
  - LC2007 (Land Class numeric)
  - LC2007_COD (Land Class text)
  - LC_2007 (Land Class name without code for LCs with no hedges)
  - Size_of_LC (Area of Land Class in m2)
  - WNS_km (Ash length in natural-shaped woody linear features, km)
  - WUS_km (Ash length in unnatural-shaped woody linear features, km)
  - Belt_km (Ash length in belts of trees, km)
  - All_WLF_km (Total ash length across WLF categories, km)
  - Mean_km_km (Mean length of all linear features per km2)
- Resolution: 1 km
- Coordinate system / Projection: British National Grid (OSGB36), Transverse Mercator
- Extent: Great Britain

## Spatial scope and feature types
- Woody linear features: landscape elements <5 m wide; minimum length 20 m; gaps up to 20 m.
- Two feature shapes:
  - Natural Shape: lines of trees or belts of trees
  - Unnatural Shape: hedgerows
- For Natural Shape, ash proportions recorded in bands (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%, Individual Tree).
- For Belts, method mirrors lines; for Unnatural Shape, ash composition inferred through separate survey data.

## Methodology for estimating ash length
- Sampling design: Countryside Survey samples 1 km2 squares across GB, stratified by Land Class (ecological gradients).
- Natural Shape (lines of trees):
  - Use band midpoints (e.g., 5%, 17.5%, 37.5%, 62.5%, 85%, 97.5%, 100%) to estimate ash length per 1 km2 per stratum.
  - Compute 1 km mean ash length per sampling strata, multiply by Land Class area, and sum across strata for national totals.
- Belts of trees:
  - Apply the same methodology as lines of trees.
- Unnatural Shape (hedgerows):
  - Species composition not tied to ash length in rings; data from D plots used.
  - Estimate ash proportion from mean percent cover adjacent to hedges, multiply by total hedge length, scale by Land Class area, and sum nationally.
- Data sources and methods are detailed in associated Countryside Survey documentation and literature.

## Associated datasets and references
- ITE Land Classification (2007)
- Countryside Survey (official website)
- Related methods papers and technical reports (e.g., CS UK results 2007; LCM2007, sampling strategies)

## Usage considerations for GIS specialists
- Suitable for map-based visualisations of ash distribution in hedgerows, belts, and woody linear features across GB.
- Ensure alignment with the Land Classification data and the 1 km resolution when combining with other spatial products.
- Be aware of methodological differences between Natural Shape and Unnatural Shape estimates (e.g., how ash in hedges is derived from D plots).
- Useful for national-scale trend analyses and for informing biodiversity and ash-health related risk assessments.

## Access and references
- Countryside Survey outputs and methods: www.countrysidesurvey.org.uk
- Related publications and technical reports cited within the dataset documentation.