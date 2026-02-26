# Mapping Quality Assurance Exercise

## Overview
- Evaluation of Countryside Survey 2007 data quality to produce high-quality, interoperable habitat and landscape maps.
- Shift to digital field mapping (Surveyor software) to reduce interpretation error and enable rapid in-field QA via a wiki and office QA checks.
- Comparison between surveyors' data and QA datasets across multiple scales and methods to assess accuracy, consistency, and data usability.

## Data Governance and Metadata Considerations (Data Steward perspective)
- Use of controlled vocabularies and structured attributes (e.g., Broad Habitat BH codes, primary vs secondary attributes, dominant species).
- Documentation of data lineage, methodology, and versioning (e.g., updates to habitat definitions, such as Blanket Bog; field handbook revisions).
- Provenance and transparency: data flowed from field collection to geodatabase, then QA analyses, with explicit change-tracking (Real change, Error Change, No change) to support historical revision.
- Metadata needs highlighted by the exercise:
  - Data collection methods and software prompts
  - Mandatory fields and visit status indicators
  - Details of QA methods and analysis workflows (direct comparison, raster, 100-point grid)
  - Handling of refused access and partial coverage (masks and common surveyed areas)
- Data interoperability: alignment with previous CS data (1998) to enable temporal comparisons; explicit notes on mosaic mapping and cross-scale compatibility.

## Data Collection, Storage, and Sharing (Data Stewardship implications)
- Data capture: field mapping in 2007 using Surveyor tablets; immediate upload to an interactive wiki enabling early data checking.
- Data storage: centralized geodatabase for analysis; MS Excel-like tables for summary stats and QA outputs.
- Data sharing: QA and CS datasets accessible for analysis; documentation supports reuse and cross-dataset analyses.
- Update mechanisms: explicit procedures to exclude unsurveyed or refused areas; emphasis on update-ready datasets with visit status and dominant-species fields.

## QA Approaches and Methods (Key points for governance)
- 6.1 Direct comparison of aggregate areas: CS vs QA proportions of Broad Habitats (BHs) per square; findings show most BHs similar, with some notable discrepancies and scale-dependence.
- 6.2 Raster data comparisons: 1 km squares divided into 10,000 10x10 m cells; assessment of absolute BH amounts and spatial locations; average raster agreement around 76%, with some squares much higher or lower.
- 6.3 100-point grid analysis: concordance between CS and QA BH mapping at 100-point resolution; reported concordance varies by square; highlights where mis-matches occur and the effect of mosaic upland habitats.
- 6.4 Polygon species attributes: comparison of 2–3 dominant species per polygon; about 45% of QA polygons matched a corresponding CS species; 77% of polygons with species match also had matching BH; species concordance generally lower than habitat concordance due to identification and composition complexity.
- 6.5 Species lists: comparison of commonly recorded species within matched polygons; indicates broader differences in species lists than in habitat coding.
- 7–8: Linear features and points: high consistency in land-use themes for linears; point feature habitat codes also largely consistent after buffering and matching.
- 9: Change recording: implementation of Real Change, Error Change, No Change fields; general agreement on change coding, though some habitat-specific ambiguities persist, especially where habitat definitions overlap or where prior data differ (e.g., Blanket Bog vs Dwarf Shrub Heath).

## Key Findings and Quality Insights (Data Quality and Governance)
- Overall agreement between CS surveyors and QA teams is high across many habitats and feature types, illustrating the value of digital data capture and structured QA.
- Some persistent issues:
  - Blanket Bog vs Dwarf Shrub Heath disagreements, influenced by evolving definitions and field-key revisions.
  - Urban vs Improved Grassland classification ambiguities, and overlaps between Neutral and Improved Grassland.
  - Upland mosaic mapping challenges where fine-scale mosaics are difficult to partition accurately.
  - Machair-type sand dunes presenting unique classification questions due to local ecology.
- Mosaic and scale challenges underscore the need for explicit handling of transitional habitats and for robust versioned definitions to support consistency.
- Change coding, while generally reliable, can be complex for habitat-level changes and benefits from continuous training and clear guidelines.
- The exercise demonstrates substantial data quality improvements through digital workflows, but also highlights the necessity of ongoing governance aspects (definitions, training, metadata) to maintain interoperability over time.

## Implications for Data Stewards (Actionable Recommendations)
- Establish and maintain a strict data dictionary and controlled vocabularies for habitat and feature codes with version control to track definition changes (and to support historical comparisons).
- Implement formal data lineage and provenance metadata, including:
  - Original field collection methods and tools
  - QA procedures and analysis methods (direct, raster, 100-point)
  - Change-tracking history with clear definitions of Real Change, Error Change, and No Change
- Version habitat definitions and provide migration/mapping guides when definitions are updated (e.g., Blanket Bog revisions) to minimize cross-year inconsistencies.
- Maintain comprehensive metadata on mosaics and mosaic handling, especially in upland or transitional habitats, to aid reproducibility and interpretation.
- Ensure data quality metrics are standardized and auditable:
  - Routine reporting of agreement rates (Raster, 100-point, polygon) by habitat and square
  - Documentation of outliers and their causes (e.g., specific squares like 261, 773)
- Provide clear data products with different granularity:
  - Field-level data and final habitat maps
  - Ancillary datasets (dominant species per polygon, change codes)
  - Processed rasters and 100-point grids for interoperability with other national datasets
- Strengthen training and QA alignment across data creators and sharers to reduce inter-team variance, especially for complex habitats and urban classifications.
- Plan for data integration with legacy datasets and future updates, ensuring consistent schema and accessible change logs for researchers reusing the data.

## Risks, Limitations, and Considerations for Future Work
- Access limitations (refused areas) create gaps and require masking; governance should document handling rules and impacts on analyses.
- Differences in definitions between field handbook versions and QA interpretations necessitate ongoing calibration and potentially reconciliation rounds.
- The high level of detail in this exercise increases complexity; governance should balance granularity with usability for data users.

## Conclusion (Data Steward Takeaways)
- The Mapping Quality Assurance Exercise demonstrates that a digital, well-documented QA workflow enhances data quality and interoperability for large-scale habitat mapping.
- Key governance imperatives include versioned definitions, robust metadata and provenance, standardized QA metrics, and ongoing training to align surveyors and QA teams.
- By codifying these practices, Data Stewards can ensure that habitat datasets remain reliable, citable, updatable, and readily discoverable for downstream analysis and sharing across organizations.