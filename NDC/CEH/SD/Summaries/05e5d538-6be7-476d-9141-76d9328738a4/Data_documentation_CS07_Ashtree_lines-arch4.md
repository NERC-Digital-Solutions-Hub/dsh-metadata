# Countryside Survey: Ash tree distribution in woody linear features 2007

## Overview
- Dataset details ash tree estimates for Great Britain within woody linear features, based on Countryside Survey 2007 data.
- File: CS07_Ashtree_Linears (document version: 1:19-8-2013).
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology; prepared by CEH Lancaster.

## Data contents and structure
- Columns (Land Class related):
  - LC2007 (Land Class, numeric)
  - LC2007_COD (Land Class, text)
  - LC_2007 (Land Class with no code where no hedges occur)
  - Area of Land Class (m2; may differ from default Area)
  - Size_of_LC
- Woody Linear Feature (WLF) measurements:
  - WNS_km: Natural shape ash length in km within land class
  - WUS_km: Unnatural shape ash length in km within land class
  - Belt_km: Belts of trees ash length in km within land class
  - All_WLF_km: Total of above three components (in land class)
  - Mean_km_km: Mean length of all linear features in km per km2
- Resolution: 1 km
- Spatial reference: British National Grid (OSGB1936), Projection: Transverse Mercator
- Extent: Great Britain

## How estimates were produced
- Countryside Survey uses a stratified random sample of 1 km squares across GB, based on land classes representing major ecological gradients.
- Landscape features: woody linear features include hedgerows, walls, fences; minimum length 20 m with gaps up to 20 m; features categorized as Natural Shape (e.g., lines/belts of trees) or Unnatural shape (hedgerows).
- Ash proportion: For natural-shape lines, ash proportion is distributed across bands (<10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%, Individual Tree) and midpoints of bands (e.g., 5%, 17.5%, 37.5%, 62.5%, 85%, 97.5%, 100%) are used to compute mean ash length per 1 km square.
- Scaling to national estimates: 1 km square means per sampling stratum are multiplied by Land Class area to yield country totals; the same method applies to belts of trees (and belts of scrub) using corresponding data.
- For Unnatural-shape hedges, ash proportion is inferred from adjacent D plots (vegetation diversity plots) with percent cover per species, aggregated to obtain mean ash length per stratum; results are scaled by hedge length and land class area.
- Models combine stratum means and land class areas to produce national estimates for ash in lines of trees and belts.

## Data quality and considerations
- Natural vs. Unnatural shapes are treated with slightly different data collection and estimation methods (e.g., species composition handling in hedges).
- Data are aggregated by land class, acknowledging variation in ecological gradients and landscape structure.
- Proportions are based on band midpoints and adjacent vegetation plots to estimate ash presence in hedges.

## Associated datasets and references
- ITE Land Classification (2007): http://dx.doi.org/10.5285/5f0605e4-aa2a-48ab-b47cbf5510823e8f
- Countryside Survey main site: http://www.countrysidesurvey.org.uk
- Further reading and methods:
  - Distribution of Ash trees in Countryside Survey data (2013) – Maskell et al.
  - Countryside Survey: UK Results from 2007 (Carey et al.)
  - LCM2007 – Final report: Land cover map for Great Britain
  - Sampling Strategy references (Barr et al., Bunce et al., etc.)
  - Additional project reports and PDFs listed in the document

## Usage and access notes
- Data are produced under Countryside Survey copyright: © NERC - CEH.
- Primary usage is to quantify ash distribution within woody linear features across Great Britain, enabling ecological and policy analyses at national scales.
- For methodological details, consult the listed further reading and linked resources on the Countryside Survey site.