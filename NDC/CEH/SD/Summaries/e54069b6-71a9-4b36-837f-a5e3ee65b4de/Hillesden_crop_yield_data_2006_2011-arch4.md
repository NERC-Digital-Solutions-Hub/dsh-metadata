# Supporting information for arable crop yield data for the Hillesden Experimental Platform, UK collected between 2006 and 2011

## Overview and purpose
- Data come from an experimental platform at Hillesden Estate (900 ha) in Buckinghamshire, central England.
- Objective: assess ecological intensification by converting portions of arable land to wildlife habitat and its effect on crop yields and biodiversity.
- Farm characteristics: heavy clay soils, relatively flat, simple crop rotation (autumn-sown first wheat, followed by a break crop such as oilseed rape or field beans, then back to wheat); fields bordered by hawthorn hedgerows.
- Experimental intent: compare conventional intensive agriculture (Business as Usual, BAU) with two habitat-enhancing treatments to support biodiversity, pollinators, and natural enemies of pests.

## Experimental design
- Randomised block design conducted from September 2005 to 2011.
- Five contiguous replicate blocks (150–180 ha each) with three treatments applied within each block to discrete field groups totaling 50–60 ha per group.
- Treatments:
  - BAU: continuation of intensive production with fields cropped to the edge (no land removed).
  - ELS (Entry Level Stewardship): 1% of land removed from production to create wildlife habitats at field edges and corners (0.25–0.30 ha field margins plus a 0.25 ha seed resource patch).
  - ELSX (ELS extra): additional habitats in addition to ELS, totaling about 6% of crop land out of production; included three 0.5 ha patches with diverse wildflower/grass mixes and additional patches for birds and beneficial invertebrates; remaining converted area includes legume margins or mixed tall grasses and nectar for pollinators.

## Data collection and processing
- Yield measurement: used on-board Quantimeter yield meters on a CLAAS Lexion 580+ combine; accuracy demonstrated to be >97%.
- Data captured: yield data for three crops (winter wheat, oilseed rape, field beans) in 56 fields each year (2005–2011).
- Calculation of yields:
  - Yield per field per year calculated as tonnes per cropped hectare (yield/ha) and per whole field area (tonnes per field).
  - Yields standardized against regional averages from Defra (National June Survey of Agriculture and Horticulture; Defra SE regional average yields by crop). For beans, national average data were used due to lack of regional data.
- Data normalization and outputs:
  - Yield/ha values adjusted by comparing to Defra regional averages to contextualize performance against regional benchmarks.
  - A field-level “Ratio” column provides the Hillesden yield relative to the Defra regional average.

## Data structure and key variables
- Columns and meanings:
  - Year: year of data collection (YYYY).
  - Block: replicate identifier (1–5).
  - Treatment: BAU, ELS, or ELSX (ELS extra) representing the habitat-intensification treatment.
  - Field Name: field identifier.
  - Field Area: area of the field in hectares (from farm records).
  - Crop: crop type (e.g., winter wheat, oilseed rape, field bean).
  - Quantity: total yield (tonnes) of the crop per field per year.
  - Yield/ha: yield per hectare (tonnes per hectare).
  - Defra SE regional average yield t/ha: published regional average yield for the crop and year.
  - Ratio: Hillesden yield relative to Defra regional average yield.
  - Notes: additional details on average yield derivation and methods.

## Data quality, scope, and limitations
- Coverage: 56 fields with annual yield data across 2005–2011 (despite the main document title indicating 2006–2011).
- Accuracy: onboard yield meter validated as highly accurate (>97%).
- Limitations:
  - Field bean regional data not available; national averages used for normalization.
  - Potential year-to-year variability due to weather, pests, and management factors beyond treatment effects.
- Metadata considerations:
  - Clear documentation of field-level identifiers, treatment type, field areas, and derivation of yields and ratios aids comparability and cross-study reuse.

## Use cases and relevance for data governance
- Enables evaluation of biodiversity-oriented or habitat-based interventions on traditional arable yields.
- Facilitates comparisons of yield performance under BAU, ELS, and ELSX treatments within a consistent block design.
- Provides a replicable framework for linking field-level agronomic data with regional benchmark statistics (Defra) to assess relative performance.
- Useful for researchers, policy advisors, and data managers focused on agricultural sustainability, ecological intensification, and data standardization across multi-year field experiments.

## Data management and accessibility notes
- Data are organized with explicit field identifiers, treatment designations, and year-by-year measurements, enabling traceability and reuse.
- Documentation includes explicit definitions of field-level yield calculations and the methodology for deriving ratio metrics against regional averages.
- For broader reuse, consider harmonizing field naming conventions, ensuring consistent year ranges, and preserving the linkage to Defra reference data.