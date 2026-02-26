# Mapping Quality Assurance Exercise

## Overview
- Reports on the 2007 Countryside Survey digital mapping QA exercise.
- Aim: ensure high-quality, analysable data in a geodatabase and enable fast analysis alongside national datasets.
- Shift from post-survey digitisation of paper maps to field mapping with a dedicated Surveyor software (mandatory fields, prompts, visit status) and early wiki-based data checks.
- Quality assurance involved cross-checks between surveyors and QA teams across multiple scales and data types.

## Dataflow and QA Framework
- Field data collected digitally with Surveyor; uploaded to an interactive wiki for early QA.
- QA teams conducted field visits to survey squares and used separate mapping tasks to validate data.
- Analyses used: direct aggregate comparisons, raster-based habitat comparisons, 100-point grid comparisons, and polygon-level attribute checks.
- Common surveyed areas created via masking to ensure comparability when access was refused or areas were not surveyed.

## QA Approaches and Metrics
- 4.1 Direct comparison: aggregate areas/lengths/points per 1 km square by habitat types.
- 4.2 Raster comparison: convert polygons to 10x10 m rasters; compare habitat extents and locations; sampling with a resolution grid.
- 4.3 100-point grid: evaluate concordance of Broad Habitats (BH) and Priority Habitats (PH) at 100 points per square.
- 4.4 Attribute comparisons: reference IDs used to compare species and other attributes between CS and QA datasets.
- 6.2 Raster data: overall raster agreement varied by square (average around mid-70s percent; some squares much higher, others much lower).
- 6.3 100-point concordance: majority of squares showed good concordance; notable exceptions included squares 773 and 261.
- 6.4 Polygon species analysis: 45% of QA polygons had at least one matching listed species in the CS polygon; 77% of those also had matching BH.
- 7–8: Linear features and point features: generally strong agreement in total lengths and point counts; most linears and points aligned in land-use themes and habitat codes.
- 9 Change recording: new digital change field allowed detailed categorisation (Real change, Error change, No change); overall good agreement on change coding, though habitat-specific change can be complex.

## Key Findings and Insights
- Overall data quality improvement: digital collection and wiki-based QA enhanced data integrity, with mandatory fields and visit status layers improving completeness.
- Broad Habitat (BH) agreement: substantial alignment between CS and QA for many BHs; some discrepancies observed, notably with Neutral vs Improved Grassland, and with Broadleaf vs Coniferous woodland.
- Upland and mosaic habitats: greater mismatches in upland areas and mosaics, where habitat boundaries are diffuse and definitions can be contested.
- Blanket Bog: significant definitional challenges; revisions to field handbook and habitat keys in 2007 contributed to mismatches, especially in squares with complex peatland mosaics.
- Scotland-specific issues: machair habitats on sand dunes introduced localised anomalies affecting comparisons with BH categories.
- Woodland definitions: some confusion around woodland classification due to previous guidelines; most allocations balanced between Broadleaf and Coniferous timber classifications.
- Species concordance: species-level matching between QA and CS polygons lower (about 40%), influenced by the dominance and identification of species; Better concordance for woodlands and Improved Grassland.
- Change coding: high consistency for change flags across most landscape features, though habitat-level change interpretation remains nuanced.

## Habitat- and Data-Specific Observations
- Some squares show high raster concordance (e.g., 364, 488); others show notable disagreement (e.g., 261, 773).
- 100-point concordance highlights specific problem squares (261, 773) and generally strong performance elsewhere.
- Urban and grassland classifications presented particular challenges in certain squares; ongoing refinement of urban vs. grassland delineation noted.

## Implications for Data Strategy and Governance
- The digital QA framework demonstrates robust mechanisms for data quality control, versioning, and traceability across scales (from polygons to rasters to points).
- Clear, consistent habitat definitions and training are critical to reduce upland and mosaicked habitat mismatches.
- Continuous refinement of habitat keys (e.g., Blanket Bog, Neutral vs Improved Grassland) is needed to improve cross-team consistency.
- Data stewardship should emphasise metadata clarity, standardized classifications, and ongoing QA feedback loops to support cross-network data use.

## Recommendations and Next Steps
- Finalise and harmonise habitat definitions, with targeted training for field teams to reduce misclassifications in complex habitats (especially Blanket Bog and upland mosaics).
- Further refine woodland classification criteria and ensure alignment with field handbook terminology.
- Expand targeted QA on problematic squares and habitat types to iteratively improve key definitions and mapping protocols.
- Maintain digital change recording workflows and provide ongoing guidance to users on interpreting and applying change codes.
- Consider additional harmonisation efforts for urban vs grassland delineation and for sand-dune habitats with localised variants (e.g., machair).

## Endnotes
- The exercise covered 23 1-km QA squares with some access refusals; data were aligned with CS survey data for comparability.
- The combination of raster, 100-point, and polygon assessments provides a comprehensive picture of data quality and informs ongoing data governance and strategy for landscape-scale data products.