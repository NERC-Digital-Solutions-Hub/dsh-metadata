# Supporting information for arable crop yield data for the Hillesden Experimental Platform, UK collected between 2006 and 2011

## Study site
- Location: Hillesden Estate, Buckinghamshire, central England (900 ha; 51.95N, 01.00W).
- Soils: heavy clay with flat topography.
- Cropping system: large fields (10–20 ha) in simple rotation—autumn-sown wheat followed by break crops (oilseed rape or field beans), then back to wheat; second wheat crops rare (≈5% of fields).
- Farm management: uniform inputs of fertilisers/pesticides; hedgerows along field boundaries.

## Experimental design
- Period: September 2005–2011; randomized block experiment with five contiguous blocks (150–180 ha) across farm fields.
- Treatments: three within-block treatments applied to field groups (50–60 ha per group)
  - Business as Usual (BAU): continuation of intensive production to field edges.
  - ELS: 1% of land out of production for wildlife habitat at field edges/corners.
  - ELS extra (ELSX): additional habitat, totaling 6% of land out of production, including diverse patches and margins.
- Purpose: compare ecological intensification against BAU to support biodiversity, pollinators, and natural enemies of crop pests.

## Data gathering and measurement
- Yield data: collected for three crops (n=56 fields) yearly from 2005–2011 using onboard CLAAS Lexion 580+ yield meter; accuracy >97%.
- Calculation of yields:
  - Yield per field per year in tonnes.
  - Two yield metrics: cropped area yield (tonnes per harvest area) and whole-field yield (tonnes per field area).
  - Normalization: yield per hectare compared to regional Defra averages.
    - For wheat and oilseed rape: Defra regional average yields (t/ha) used.
    - For field beans: national average yield data used due to lack of regional data.
- Field and crop identifiers: Year, Block, Treatment, Field Name, Field Area, Crop, Quantity, Yield/ha, Defra SE regional average yield t/ha, Ratio, Notes.

## Data structure and metadata
- Column definitions:
  - Year: data collection year.
  - Block: replicate identifier (1–5).
  - Treatment: cross-compliance, ELS, or ELSX.
  - Field Name: field identifier.
  - Field Area: field area in hectares from farm records.
  - Crop: crop identifier.
  - Quantity: total yield (tonnes) per crop.
  - Yield/ha: yield per hectare.
  - Defra SE regional average yield t/ha: published regional average.
  - Ratio: Hillesden yield relative to Defra regional average.
  - Notes: additional description of derivation.
- Data provenance: direct measurements from field operations, with subsequent normalization to regional averages.

## Data processing and quality control
- QA reflects high accuracy of yield meter measurement (>97%).
- Calculations standardized to enable cross-field and cross-year comparisons: per-area and per-field yield, plus ratio to regional benchmarks.
- Clear documentation of data derivation, including handling of missing regional data (beans) via national averages.

## Data governance and reuse considerations
- Metadata and column definitions provide clear data semantics for reuse in biodiversity, pollinator, and crop-yield research.
- Versioning and updates implied by ongoing data collection across multiple years and treatments.
- Data sharing considerations include alignment with Defra data sources and transparency about data provenance and normalization procedures.

## Limitations and considerations for users
- Field beans rely on national rather than regional averages due to data gaps.
- Temporal scope limited to 2005–2011 (yield data collected within this period; document notes 2006–2011 for collection).
- Treatments and block design are specific to this site; caution needed when generalizing to other contexts.