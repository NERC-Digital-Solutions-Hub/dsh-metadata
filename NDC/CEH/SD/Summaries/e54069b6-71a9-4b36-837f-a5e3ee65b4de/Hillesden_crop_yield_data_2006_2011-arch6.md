# Supporting information for arable crop yield data for the Hillesden Experimental Platform, UK collected between 2006 and 2011

## Overview
- Dataset from the Hillesden Experimental Platform (Hillesden Estate, Buckinghamshire, UK) collected 2005–2011.
- Purpose: examine effects of converting portions of arable land to wildlife habitat on biodiversity and crop yields, including pollinators and natural enemies of pests.
- Experimental framework: randomised block design comparing Business as Usual (BAU) with two ecological intensification treatments (ELS and ELSX).

## Study site
- Location: Hillesden Estate, central England (51.95N, 01.00W), ~900 ha.
- Soil/topography: heavy clay soils, relatively flat.
- Cropping: simple rotation—autumn-sown first wheat with break crops (oilseed rape or field beans) and back to wheat; second wheat rare.
- Field structure: large fields (10–20 ha) bordered by hedgerows; consistent management across the farm.

## Experimental design
- Period: September 2005–2011; five contiguous replicate blocks (150–180 ha) with randomised field groups (50–60 ha per treatment per block).
- Treatments:
  - BAU: production-only continuation.
  - ELS: habitat enhancement per English Entry Level Stewardship; 1% land removed from production to create field margins and a small habitat patch.
  - ELSX: expanded habitat; ~6% of land out of production; multiple patches of diverse habitat including perennial wildflower mixes and seed-bearing plants for birds and beneficial invertebrates.
- Field groups: discrete groups within blocks, each assigned to a treatment.

## Data gathering
- Crops measured: three crop types (winter wheat, oilseed rape, field beans) across 56 fields annually.
- Measurement method: onboard yield meter (Quantimeter) on CLAAS Lexion 580+; accuracy >97%.
- Timeframe: yields collected in 2005–2011.
- Yield calculations:
  - Yield/ha (cropped area): field yield divided by the area actually cropped (excluding habitat strips).
  - Yield/ha (whole field): field yield divided by the total field area.
  - Normalization: both yield metrics divided by regional average yields for winter wheat and oilseed rape (Defra SE regional averages) to yield Defra-normalized comparators; for field beans, national averages used due to lack of regional data.

## Data processing and normalization
- Data derived: total yield (tonnes) per field per year, plus area metrics.
- Normalizations:
  - Yield per cropped hectare (tonnes/ha) to reflect crop performance with habitat presence.
  - Yield per whole field hectare (tonnes/ha) to reflect total field productivity with habitat outlays.
  - Ratios to Defra regional average yields for cross-field/year comparisons.
- Regional reference data: Defra regional averages (scoped to crop type); field bean regional data not available.

## Data structure and column headings
- Year: data collection year.
- Block: replicate identifier (1–5) of the randomised block.
- Treatment: treatment label (cross-compliance, ELS, ELSX).
- Field Name: field identifier.
- Field Area: field area in hectares from farm records.
- Crop: crop type (wheat, oilseed rape, field bean).
- Quantity: total yield (tonnes) of the crop.
- Yield/ha: yield per hectare for the field (tonnes/ha) using cropped area.
- Defra SE regional average yield t/ha: published regional average yield for the crop.
- Ratio: Hillesden yield relative to the Defra regional average (comparison metric).
- Notes: additional description and derivation details for average yield data.

## Data quality and limitations
- Yield measurement quality: high accuracy (~97%+) via Quantimeter.
- Data scope: 56 fields over 7 years (2005–2011) across three crops.
- Limitations:
  - Field bean regional data not available; reliance on national averages for that crop.
  - Year-to-year variability and patchy adoption of habitat treatments may influence results.
  - Results reflect field-level management uniformity with added habitat; external factors (weather, pests) still influence outcomes.

## Potential uses
- Assessing the impact of wildlife habitat creation on arable crop yields.
- Comparing Hillesden yields to Defra regional benchmarks to identify relative performance.
- Supporting data-driven dashboards or self-serve reports for stakeholders interested in habitat–yield trade-offs.
- Informing policy discussions on ecological intensification and land-use decisions in arable systems.