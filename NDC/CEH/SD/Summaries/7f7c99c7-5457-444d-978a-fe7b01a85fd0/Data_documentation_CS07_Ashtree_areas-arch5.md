# Countryside Survey: Ash tree distribution in areas <5ha, 2007

## Overview
- Dataset CS07_ashtree_areas provides estimates of ash trees in Great Britain specifically within broadleaved woodland areas smaller than 5 hectares.
- Based on Countryside Survey 2007 data; represents ash presence in 2007.

## Data content and structure
- Columns:
  - Gridcode: Code for band interval relating to the hectares of ash per km square (values 1-7).
  - Ha_per_km: Estimate of the number of hectares of ash per km square, for seven bands: 0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5 (text format for bands).
- Resolution: 1 km.
- Extent: Great Britain.
- Coordinate system/Projection: British National Grid (OSGB1936), Transverse Mercator.

## Methods and provenance
- Countryside Survey samples 1 km squares across GB using stratified random sampling based on major ecological gradients.
- In each 1 km square, habitats are mapped; dominant species recorded by percentage cover categories.
- This dataset focuses on areas where ash is present in 2007 and excludes larger woodlands (>0.5 ha) to avoid duplication with Forestry Commission data.
- National estimates are derived by:
  - Calculating mean ash woodland area within each 1 km square by land class.
  - Multiplying by land class area and summing across land classes.
  - Weighting means by the proportion of Broadleaved Woodland in each 1 km square using Land Cover Map 2007 (LCM2007).
- Land classification used: 1990 ITE Land Classification with 32 classes.
- More methodological details available at the Countryside Survey website.
- Related literature and sources listed for context (e.g., Maskell et al. 2013; Barr 1998; Morton et al. 2011).

## Associated datasets and links
- ITE Land Classification (1990) [associated dataset]
- Land Cover Map 2007 (1 km raster) [associated dataset]
- Countryside Survey main site: www.countrysidesurvey.org.uk

## Metadata and governance
- Data rights: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Document version: 1:19-8-2013; prepared by C.M. Wood, L.C. Maskell, P.A. Henrys (CEH Lancaster).

## Data quality, limitations, and considerations
- Based on a sample-based national estimation approach; includes uncertainty inherent in upscaling from 1 km squares.
- Focused on areas <5 ha to avoid duplication with larger-scale Forestry Commission data; not a complete inventory of all ash in GB.
- Uses mid-point representations for percentage cover within bands, which introduces approximate estimation.
- Outputs are suitable for broad-scale assessment of ash presence in small broadleaved woodland patches and for integration with related land classification and land cover datasets.

## Practical considerations for Data Stewards
- Ensure availability and discoverability via relevant portals; maintain provenance links to CS methods and LC Map 2007.
- Align metadata with associated datasets (ITE Land Classification and LCM2007) for interoperability.
- Monitor for updates or revised analyses that may alter national estimates; record versioning and methodological changes.
- Provide clear citation guidance and references for end users (including the listed further readings).