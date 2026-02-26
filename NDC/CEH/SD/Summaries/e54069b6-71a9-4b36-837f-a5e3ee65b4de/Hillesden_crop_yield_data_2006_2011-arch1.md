# Supporting information for arable crop yield data for the Hillesden Experimental Platform, UK collected between 2006 and 2011

## Overview
- Documents the dataset and methods for arable crop yield data from the Hillesden Experimental Platform (2005–2011, with title indicating 2006–2011).
- Aims to assess effects of converting portions of arable land to wildlife habitat on crop yields and biodiversity-related outcomes.
- Compares three treatments: Business as Usual (BAU), ELS (Entry Level Stewardship habitat enhancement), and ELS extra (ELSX) against BAU.
- Data are field-level yield measurements across multiple crops, standardized against Defra regional average yields to enable cross-year comparisons.

## Study site
- Location: Hillesden Estate, Buckinghamshire, central England (51.95N, 01.00W).
- Size and land: ~900 ha on heavy clay soils with relatively flat topography; fields of 10–20 ha, bordered by 2–3 m hedgerows.
- Cropping system: simple rotation with autumn-sown first wheat usually followed by break crops (oilseed rape or field beans), then back to wheat; second wheat crops rare (~5% of fields).
- Management: consistent across farm with conventional inputs; annual variations due to weather/pest outbreaks.

## Experimental design
- Period: September 2005–2011; randomized block design with five blocks (1–5), totaling 150–180 ha per block.
- Treatments within blocks: three treatment groups distributed randomly across discrete field groups (50–60 ha per group).
  - BAU: continuation of intensive production to field edges.
  - ELS: habitat creation removing ~1% of land from production (0.25–0.30 ha 6 m field margins plus a 0.25 ha patch supplying winter resources).
  - ELS extra (ELSX): broader habitat provision with ~6% of land removed, including three 0.5 ha patches with diverse perennial wildflowers and grasses, three additional 0.5 ha patches with seed-bearing plants for birds/invertebrates, and 0.6 ha margins sown with legumes or tall grasses with nectar resources.

## Data gathering and processing
- Yield measurements: annual field-level yields for three crop types (n = 56 fields) using the onboard Quantimeter yield meter on a CLAAS Lexion 580+ combine.
- Accuracy: field tests show >97% accuracy.
- Yield calculations:
  - Yield per cropped area (tonnes per hectare): crop yield divided by cropped area (excluding habitat-for-production).
  - Yield per whole field area (tonnes per hectare): crop yield divided by total field area (including habitat).
  - Normalization: each yield figure divided by Defra regional average yield per hectare for the corresponding year and crop. For field beans, national average yield data were used due to lack of regional data.
- Coverage: data span 2005–2011 (field-level yields in 56 fields across the five blocks).

## Data columns and definitions
- Year: year of data collection (YYYY)
- Block: replicate identifier (1–5)
- Treatment: treatment identifier (cross-compliance, ELS, ELSX)
- Field Name: field identifier
- Field Area: area of field (ha)
- Crop: crop type
- Quantity: total yield (tonnes) of crop
- Yield/ha: yield per hectare of crop
- Defra SE regional average yield t/ha: published regional average yield for the crop and year
- Ratio: Hillesden yield relative to the Defra regional average
- Notes: description of how average crop yield data were derived

## Key considerations for analysis
- The design isolates effects of habitat conversion (ELS/ELSX) on yields relative to BAU, using randomized blocks to control for spatial variation.
- Two yield measures (cropped-area yield and whole-field yield) allow assessment of both efficiency of cropped area and overall field productivity losses due to land conversion.
- Normalization to Defra regional averages enables year-by-year comparability across crops with differing national/regional baselines.
- Field beans rely on national averages due to unavailable regional data, which may introduce cross-year comparability considerations for that crop.
- The dataset supports analyses of biodiversity-friendly practices versus conventional farming and their trade-offs with yield, as well as potential correlations with landscape-scale factors (pending additional data).