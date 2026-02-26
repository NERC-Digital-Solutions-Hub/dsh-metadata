# Mapping Quality Assurance Exercise

- Purpose: Evaluate the quality and comparability of digital mapping from Countryside Survey 2007, ensuring data are high-quality, compatible with previous approaches, and stored for use with national spatial datasets in a geodatabase.
- Context: Transition to field-based digital mapping (Surveyor software) to reduce interpretation error and speed data analysis; early data checks via an interactive wiki; QA teams and CS survey teams used multiple QA approaches to assess data quality.

## Data, scope and workflow

- Data collection and QA setup
  - Field mapping with mandatory fields and visit-status prompts; data uploaded to a wiki for early office checks.
  - QA mapping covered 23 1km squares, selected to represent land classes and locations across GB; areas with access refusals excluded from analysis.
- Quality assurance approaches
  - Direct comparison of aggregate areas/lengths/points between surveyors and QA.
  - Raster-based comparisons: convert polygons to 10x10 m raster cells; compare dominant Broad Habitats per 1 km square; sample with a resolution grid.
  - 100-point sample grid: overlay 10x10 grid, compare Broad Habitat matches; assess concordance and SD across habitats.
  - Attribute-level analysis: compare species attributes within matched polygons via a reference ID framework.
- Data processing and transparency
  - Data stored in a single geodatabase; unsurveyed and refused areas excluded prior to analysis; alignment of CS and QA datasets for common surveyed areas.
  - Use of SAS for aggregate analysis; wide set of habitat-and feature-type comparisons.

## Key findings by analysis type

- 6.1 Direct comparison of aggregate data
  - 81% of squares had the Broad Habitat (BH) presence recorded by both CS and QA; mean BH proportion differences generally under 1–3.5% depending on habitat.
  - Some habitats showed larger variability (e.g., Improved and Acid Grasslands, Dwarf Shrub Heath, Bog, Urban).
  - Notable issues in Blanket Bog due to definitional updates; mosaics in upland areas contributed to matching challenges.
- 6.2 Raster data comparisons
  - Overall raster agreement across squares averaged around 76%, with some squares showing high concordance (e.g., 364, 488) and others lower (e.g., 261, 773).
  - Agreement by BH per square varied, with several squares achieving >80% and some much lower (e.g., 773 with only about 23%).
- 6.3 100-point analysis
  - Concordance generally high across many squares, but notable mismatches in a few (e.g., 773 at 19%, 261 at 41%).
  - Table-based matrix indicates good matches for many BH/PH codes, with some cross-check issues in complex or localized habitats (e.g., sand dunes, machair-related neutral/grassland distinctions).
  - Overall, 76–78% concordance across primary BH/PH codes for many squares; some 100-point results showed substantial mismatches.
- 6.4 Polygon analysis of species attributes
  - 1081 QA polygons and 998 CS polygons matched spatially; about 45% contained at least one species common to both matched polygons.
  - Species concordance varied by Broad Habitat; Improved Grassland and woodland showed higher species-match rates, while upland mosaics and Bracken had lower concordance.
  - Common species list (e.g., Lolium perenne, Calluna vulgaris, Molinia caerulea) showed mixed agreement between QA and CS surveyors; CS data tended to record more species per polygon.
- 7.1 Linear features
  - Lengths of linear features showed high consistency between QA and CS across most squares; where differences existed, they reflected expected cross-field variability (e.g., fence vs wall distinctions).
  - Land-use theme analysis indicated strong agreement for most themes; some confusion between specific forestry/woody features (FO vs WNS/WUS) but overall low mismatch.
- 8.1 Points
  - Point feature counts per land-use theme were largely consistent; most differences were minor and expected given feature definitions.
  - Habitat codes for point features were generally aligned between QA and CS datasets.
- 9 Change recording
  - Change coding used more detailed digital fields (Real change, Error change, No change) to update or correct previous maps.
  - High overall agreement on change codes between CS and QA, though some habitat-related discrepancies remained (e.g., divergence in blanket bog vs dwarf shrub heath in uplands).
  - Change recording benefited from in-field verification, though it added complexity for surveyors and QA.

## Implications for environmental data monitoring

- Overall quality and interoperability
  - Digital mapping with standardized fields and in-field QA enhances data clarity, reduces subjectivity, and supports integration with national datasets.
  - The QA exercise demonstrates generally strong agreement between surveyors and QA across many habitat types, supporting reliability for policy monitoring and trend analysis.
- Habitat-definition and data interpretation
  - Identified habitat-definition challenges (notably Blanket Bog, Neutral vs Improved Grassland, urban classifications, and machair-related issues) that require ongoing refinement and training.
  - Mosaic and upland habitat complexities highlight limitations of exact cross-square matching and the need for nuanced interpretation in continuum habitats.
- Data accessibility and reuse
  - The QA process emphasized making underlying data accessible and comparable, aligning with the aim to increase the value and reuse of monitoring datasets beyond single-use outputs.

## Challenges and recommendations for future work

- Habitat definitions and training
  - Provide targeted training on problematic habitats ( Blanket Bog, urban grassland distinctions, Dwarf Shrub Heath vs Blanket Bog in uplands) and update field handbooks accordingly.
- Handling mosaics and upland continua
  - Develop clearer guidance for disaggregating mosaics and resolving cross-habitat boundaries in high-heterogeneity areas to improve cross-method concordance.
- Machair and region-specific anomalies
  - Acknowledge local habitat peculiarities (machair) and assess whether special-case rules should apply or if reclassification is needed.
- Data integration and QA design
  - Consider more synchronized QA planning to balance field-time efficiency with the depth of QA coverage, given the complexity of multi-table comparisons and multiple analysis layers.

## Conclusion

- The 2007 mapping QA exercise demonstrates a high level of consistency between field surveyors and QA assessments across most habitat types and data products, with some habitat-specific discrepancies identified for refinement.
- The shift to digital data collection and in-field change verification substantially improved data quality, transparency, and the potential for cross-dataset analyses.
- The findings support the use of such QA-driven, standardized datasets for ongoing environmental monitoring and policy performance assessment, while also pointing to areas where habitat definitions and field guidance can be strengthened to further enhance data reliability and accessibility.