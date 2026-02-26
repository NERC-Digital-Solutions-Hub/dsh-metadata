# Mapping Quality Assurance Exercise

- Purpose: Evaluate and ensure high-quality, field-m collected mapping data from Countryside Survey 2007, designed to be compatible with previous datasets and suitable for rapid analysis in a geodatabase. Digital mapping reduced subjectivity and handwriting issues; QA (Quality Assurance) compared surveyor data to QA team data to assess accuracy and reliability.
- Context: Introduction of field-based mapping with Surveyor software, mandatory data fields, and an interactive wiki for early data checks. QA teams conducted visits to survey teams and used multiple digital QA approaches to validate data against 1998 baselines and across Broad Habitats (BH) and associated attributes.

## Data, Tools and Processes

- Digital mapping: Surveyors mapped in the field using Surveyor software; data uploaded to a wiki for early quality checks; QA teams used digital QA methods to compare against CS data.
- Data formats and storage: Two comparable datasets (CS surveyor data and QA data) aligned via masks; data stored in a single geodatabase; areas not surveyed or with refused access were excluded.
- QA approaches: 
  - Direct comparisons of aggregated areas/lengths/points per 1km square.
  - Raster comparisons: transform polygons to 10x10 m raster cells to assess area amounts and spatial locations.
  - 100-point grid: assess concordance of BH/PH at a finer resolution.
  - Attribute comparisons: reference ID layers to compare species attributes in matched polygons.
- Efficiency and data capture: Digital systems improved visit-status recording and species documentation; not-visited land was minimal (average ~0.4%).

## Extent and Coverage

- QA coverage: 23 one-kilometre squares, with whole squares mapped in QA to ensure depth and variety; access refusals reduced surveyed areas; analyses focused on common surveyed areas between CS and QA datasets.
- Representativeness: Squares chosen to cover different land classes and locations across Great Britain.

## Analysis Methods (Summary of Key Techniques)

- 4.1 Direct comparison: Evaluated aggregate area/length/point attributes for each square between CS and QA datasets.
- 4.2 Raster data: 1 km squares subdivided into 10,000 10x10 m cells; dominant BH assigned per cell; enabled comparison of both quantity and location.
- 4.3 100-point grid: overlaid 10x10 point grid; concordance measured for BH/PH presence.
- 4.4 Attribute analysis: generated reference ID layers to compare species attributes for matched polygons.

## Main Findings

- 6.1 Direct comparison of squares:
  - 81% of squares had BH recorded by both CS and QA.
  - Mean differences in BH proportions were generally small (mostly under 1–3.5%), though several BHs showed larger SDs indicating potential allocation differences (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban).
  - Notable habitat-definition challenges discussed (e.g., Blanket Bog, upland mosaics, land-use classifications).
- 6.2 Raster comparisons:
  - Overall raster agreement averaged around 76%, with some squares high (e.g., 364, 488) and others notably lower (e.g., 261, 773).
  - Issues linked to specific habitats (e.g., Blanket Bog, machair-related areas) and to the revised 2007 field handbook definitions.
- 6.3 100-point concordance:
  - Majority of squares showed good agreement; some squares exhibited substantial mismatches (e.g., 773, 261).
  - Habitat-specific concordance patterns documented; matrix results highlighted common BH/PH allocation disagreements.
- 6.4 Polygon species attributes:
  - 1081 QA polygons and 998 CS polygons matched; only 45% had at least one species in common.
  - Species concordance overall around 40%; higher for woodlands and Improved Grassland; lower for Bracken and upland mosaics due to complexity and dominance of multiple species.
  - Lists of commonly recorded species show substantial differences between QA and CS (e.g., Lolium perenne, Calluna vulgaris, Molinia caerulea) reflecting field identification and habitat-driven dominance.
- 7.1 Linear features:
  - Aggregate lengths per square show broad consistency; minor differences across land-use themes.
  - Some confusion between similar feature types (e.g., belts of trees vs woody linear features), but overall high consistency.
- 8.1 Point features:
  - Point counts per square show minor differences; most points aligned with CS data.
  - Habitat codes for points largely consistent; minor misclassifications (e.g., woodland vs woodland-like codes) noted.
- 9 Change recording:
  - Digital change coding allowed distinguishing Real Change, Error Change, No Change.
  - Generally high agreement on change coding; some learning curve observed as surveyors adapted to the new digital change field.

## Issues and Challenges

- Habitat definition and allocation differences:
  - Key issues with Neutral vs Improved Grassland; Broadleaf vs Coniferous Woodland; upland mosaic mapping; urban versus improved grassland classifications.
  - Blanket Bog: significant definitional and mapping difficulties; 2007 handbook updates aimed to address debates but discrepancies persisted, especially in complexes like moss/heath.
  - Machair/specialist habitats in Scotland introduced local anomalies affecting comparisons.
- Spatial variability and mosaics:
  - Upland habitats often mosaicked across multiple BHs, complicating pixel- or point-based concordance analyses.
- Training and consistency:
  - Staff with varying experience affected concordance in some squares; highlights need for ongoing training and clearer key definitions.
- Change coding complexity:
  - While overall consistent, some challenges remained in assigning accurate change codes for habitats due to overlap and interpretation.

## Conclusions

- Overall quality and compatibility: The 2007 mapping QA demonstrates substantial agreement between CS surveyors and QA assessors across habitat cover, linear and point features, and change coding, validating the digital mapping approach.
- Remaining gaps: Definitional and habitat-specific discrepancies (notably Blanket Bog, Neutral vs Improved Grassland, urban classifications, and certain upland mosaics) require further refinement and training.
- Benefits of digital QA: The digital workflow (in-field data capture, wiki checks, and geodatabase integration) improved data completeness, consistency, and the ability to perform multi-faceted QA analyses.

## Implications for Data Support Practice

- Data governance and standards:
  - Maintain clear, consistently applied habitat definitions; update field manuals as scientific understanding evolves.
  - Harmonize woodland classifications and address overlapping habitat boundaries in upland mosaics.
- QA workflows and tooling:
  - Leverage raster, 100-point, and polygon-based analyses to continuously monitor data quality.
  - Use reference-ID-based attribute comparisons to validate complex habitat attributes and species data.
- Training and knowledge transfer:
  - Provide targeted training on challenging habitats (e.g., Blanket Bog, machair) and on resolving mosaic classifications.
- Change management:
  - Continue using digital change fields to update past maps, with QA oversight to ensure accurate application of Real/Error/No Change codes.
- Data reuse and sharing:
  - The integrated geodatabase and QA outputs facilitate cross-dataset analyses and faster, more reliable exploration of CS data alongside other national spatial datasets.