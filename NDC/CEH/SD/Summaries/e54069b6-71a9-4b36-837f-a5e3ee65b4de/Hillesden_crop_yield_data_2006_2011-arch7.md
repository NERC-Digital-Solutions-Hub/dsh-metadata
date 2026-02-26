# Supporting information for arable crop yield data for the Hillesden Experimental Platform, UK collected between 2006 and 2011

## Overview
- Purpose: Assess effects of converting arable land to wildlife habitat on biodiversity and crop yields (pollinators and natural enemies of crop pests).
- Study period: Experimental design 2005–2011; yield data collected 2005–2011 (document notes some year ranges); dataset refers to 2006–2011 in title.
- Dataset focus: Per-field crop yields (three crops) with treatment and area information, standardized against regional average yields.

## Study site
- Location: Hillesden Estate, Buckinghamshire, central England (900 ha; 51.95N, 01.00W).
- Field characteristics: Heavy clay soils, flat topography; large 10–20 ha fields; simple crop rotation (autumn-sown first wheat, then break crops—oilseed rape or field beans—then back to wheat; second wheat crops rare).
- Landscape features: Hedgerows along field boundaries (2–3 m high, dominated by hawthorn).

## Experimental design (spatial layout)
- Design: Randomised block experiment with five replicate blocks (150–180 ha each) to compare three treatments.
- Treatments:
  - BAU: No land removed from production; fields cropped to the edges.
  - ELS: 1% of land removed for wildlife habitat at field edges/corners (0.25–0.30 ha field margins + 0.25 ha seed patch).
  - ELSX: Expanded habitat effort (6% of land removed) with three 0.5 ha patches of diverse wildflower/grass mixes plus additional patches for birds/invertebrates and 0.6 ha margins with legumes or nectar-rich grasses/forbs.
- Field assignment: Fields grouped into treatment-specific sets within each block (total ~50–60 ha per treatment per block).

## Data gathering (yield measurement and processing)
- Yield measurement: In-field yields of three crop types (n=56 fields) measured yearly (2005–2011) using Quantimeter on CLAAS Lexion 580+ combines; accuracy >97%.
- Calculations:
  - Yield/area metrics:
    - Yield per cropped area (tonnes per hectare) — area actually cropped (excluding habitat patches).
    - Yield per whole field area (tonnes per hectare) — entire field area including habitat patches.
  - Standardization: Yields divided by regional Defra average yields (t/ha) for the relevant year; field beans use national averages where regional data unavailable.
- Field data scope: Data captured for each field, year, and crop.

## Data fields and column definitions
- Year: Year of data collection (YYYY).
- Block: Replicate identifier (1–5) of the randomised block.
- Treatment: Experimental treatment identifier (BAU, ELS, ELSX).
- Field Name: Field identifier.
- Field Area: Field area in hectares from farm records.
- Crop: Crop identifier (wheat, oilseed rape, field beans).
- Quantity: Total yield (tonnes) of the crop.
- Yield/ha: Crop yield per hectare (tonnes/ha) for the field.
- Defra SE regional average yield t/ha: Published regional average yield for the crop (Defra data).
- Ratio: Hillesden crop yield expressed as a ratio to the Defra regional average yield.
- Notes: Additional description of how average crop yield data were derived.

## GIS relevance and potential uses
- Spatially explicit dataset: Per-field, per-year yield data aligned with field boundaries and treatment areas.
- Enables mapping and analysis of yield responses to habitat creation and management treatments.
- Facilitates integration with habitat patches, hedgerows, and landscape features to study biodiversity and ecosystem service outcomes.

## Quality, limitations and assumptions
- Consistent farm-wide management and inputs across treatments, with variations due to weather/pest outbreaks.
- Accuracy of yield measurements is high (>97%).
- Regional averaging (Defra) used for standardization; field beans rely on national averages where regional data are lacking.
- Data aggregation considers both cropped-area and whole-field yield perspectives, which can inform trade-offs between habitat conservation and production.