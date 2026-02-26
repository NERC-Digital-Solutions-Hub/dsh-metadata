# Countryside Survey: Ash tree distribution in woody linear features 2007

## Overview
- Estimates of ash trees in Great Britain within woody linear features, derived from Countryside Survey 2007 data.
- Output designed for national-scale monitoring of environmental health and policy performance.
- Data prepared for use with standardised monitoring workflows and integration with other environmental datasets.

## Data Contents and Structure
- Dataset name: CS07_Ashtree_Linears; linked to associated datasets (ITE Land Classification 2007; Countryside Survey).
- Columns (key fields):
  - LC2007 (Land Class, numeric)
  - LC2007_COD (Land Class, text)
  - LC_2007 (Land Class as above, no code where no hedges occur)
  - Area_of_Land_Class (m2, from land classification file)
  - Size_of_LC
  - WNS_km (wooden linear features, natural shape, length of ash in km)
  - WUS_km (wooden linear features, unnatural shape, length of ash in km)
  - Belt_km (belts of trees, length of ash in km)
  - All_WLF_km (total of the above three)
  - Mean_km_km (mean length of all linear features per km2)
- Resolution: 1 km
- Coordinate system/Projection: British National Grid (OSGB1936), Transverse Mercator
- Extent: Great Britain

## Methodology and Calculations
- Sampling framework: Countryside Survey uses stratified random sampling across GB based on land classes representing major ecological gradients.
- Features measured: woody linear features (lines of trees/hedgerows) and belts of trees; minimum 20 m length with gaps up to 20 m.
- Shape types: Natural Shape (lines/belts) and Unnatural Shape (hedgerows); species proportions recorded for natural shapes as bands (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%, or Individual Tree).
- Ash estimation approach:
  - For lines of trees: ash length calculated per 1 km square within each proportion band using midpoints (e.g., 5%, 17.5%, 37.5%, 62.5%, 85%, 97.5%, 100%).
  - 1 km means of ash length per sampling strata multiplied by Land Class area to obtain country totals.
  - For belts of trees: same methodology applied; belts of scrub included.
- Special case: Unnatural shapes
  - Species composition not tied to length directly; data from vegetation 'D plots' adjacent to hedges used to estimate ash proportions.
  - D plots provide total percentage cover per species; mean ash proportion across plots per strata multiplied by total hedge length to estimate ash.
- Aggregation: mean ash lengths per 1 km square scaled by Land Class area, then summed to produce national estimates.
- Reference methods and further reading: detailed in accompanying CS outputs and linked technical reports.

## Data Use and Outputs
- Provides standardized, comparable estimates of ash presence in woody linear features for national monitoring and trend analysis.
- Enables combination with other Countryside Survey outputs and external environmental datasets for broader analyses.
- Outputs support assessment of ash distribution patterns across ecological gradients and landscape features.

## Quality, Access, and Limitations
- Methods are standardised to ensure consistency over time and across datasets; QA processes implied (verification, cleaning, transformation).
- Datasets are intended to be stored and uploaded to appropriate portals for accessibility by analysts and stakeholders.
- Hedgerow-specific methodology differences (natural vs unnatural shapes) require careful interpretation when comparing with other datasets or time points.

## Related Resources
- Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (2013) – Maskell et al., CEH
- Countryside Survey outputs and UK Results from 2007
- Sampling Strategy and Land Classification documentation and related CEH/NERC reports
- Links to Countryside Survey outputs: www.countrysidesurvey.org.uk