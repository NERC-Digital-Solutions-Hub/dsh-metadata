Supporting information for arable crop yield data for the Hillesden Experimental Platform, UK collected between 2006 and 2011

## Overview
- Describes the study site, experimental design, data collection, and data processing used to generate arable crop yield data (2005–2011) for assessing ecological intensification and wildlife habitat effects on crop yields.

## Study site
- Location: Hillesden Estate, Buckinghamshire, central England (51.95N, 01.00W).
- Size and soils: Approximately 900 ha on heavy clay soils; relatively flat topography.
- Cropping system: Autumn-sown first wheat, with break crops (oilseed rape or field beans) in rotation; around 50% wheat and 50% break crops in most years.
- Field management: Uniform crop management with conventional inputs; hedgerows along field boundaries.

## Experimental design
- Timeframe: September 2005 – 2011; randomised block experiment.
- Objective: Compare effects of converting varying proportions of arable land to wildlife habitat on biodiversity and pollinators/natural enemies of pests.
- Treatments:
  - Business as Usual (BAU): No land removed from production.
  - ELS: Simple habitat enhancement per English Entry Level Stewardship; 1% of land removed for wildlife habitat at field edges and corners (0.25–0.30 ha margins; 0.25 ha patch for winter resources).
  - ELS extra (ELSX): Additional habitat beyond ELS; total 6% of cropped area out of production; three 0.5 ha patches with diverse wildflower/grass mixtures plus three patches for birds/beneficial invertebrates; remaining area included legume margins or tall grasses/nectar plants.
- Layout: Five contiguous replicate blocks (150–180 ha) with randomised assignment of treatments within each block to discrete field groups (50–60 ha per group).

## Data collection and measurement
- Yield data: Collected annually (2005–2011) for three crop types (in 56 fields) using the onboard Quantimeter yield meter on a CLAAS Lexion 580+ combine.
- Measurement basis: Grain volume measured in elevator to derive yield; accuracy >97%.
- Normalization:
  - Yield per cropped area (yield per field area minus habitat area) to assess effects of habitat on crop productivity per unit cropped area.
  - Whole-field yield (yield per field area including habitat strips) to assess overall field production impact.
  - Both metrics compared to Defra regional average yields for the relevant year and crop (regional averages; for beans, national averages used due to data gaps).

## Data processing and normalization
- Calculations:
  - Cropped area yield = field yield (tonnes) divided by cropped area (ha).
  - Whole field yield = field yield (tonnes) divided by total field area (ha).
  - Ratios calculated as Hillesden yield relative to Defra regional average yield (t/ha).
- Data sources: Defra regional average yields from the Defra England agricultural statistics (June summaries); national averages used for beans where regional data were unavailable.
- Yearly alignment: Data tied to year of collection, block, treatment, field, and crop.

## Data structure and variable definitions
- Year: Year of data collection (YYYY).
- Block: Randomised block identifier (1–5).
- Treatment: Cross-compliance, ELS, ELSX treatment.
- Field Name: Field identifier.
- Field Area: Total area of the field (ha) from farm records.
- Crop: Crop identifier (wheat, oilseed rape, field bean).
- Quantity: Total yield (tonnes) of the crop.
- Yield/ha: Crop yield (tonnes per hectare).
- Defra SE regional average yield t/ha: Published regional average yield for the crop and year.
- Ratio: Hillesden yield relative to Defra regional average yield.
- Notes: Details on how average crop yield data were derived.