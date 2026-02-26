# Mapping Quality Assurance Exercise

- Purpose: Assess quality and consistency of habitat, landscape feature mapping from Countryside Survey 2007 when digital field mapping and a wiki-based QA process were introduced to improve accuracy, speed, and data integration with national spatial datasets.

- Context for data leaders: Highlights governance, standards, metadata, cross-team collaboration, and data-system implications for building an effective data strategy.

## Data, Tools and Workflow

- Digital mapping in the field using Surveyor software with mandatory fields and prompts; reduced handwriting/labeling errors; visit status tracking.
- Data uploaded to an interactive wiki for early QA and guidance; QA teams conducted in-field checks with survey teams.
- Quality Assurance (QA) compared surveyors’ mapped data (CS) with QA-produced data across multiple scales and data types.
- Focus on interoperability: aim to compare CS data with CS QA data using a common 1km square framework and to align with prior 1998 datasets where feasible.

## QA Coverage and Approach

- Spatial extent: QA covered 23 one-kilometre squares, selected to reflect land-class variety and geographic distribution; access refusals affected some areas.
- Field operations: QA teams mapped near survey teams; both datasets combined in a single geodatabase; unsurveyed/refused areas excluded prior to analysis; analysis performed on common surveyed areas.

## Analysis Methods

- 4.1 Direct comparison of aggregate areas/lengths/points for whole squares (CS vs QA).
- 4.2 Raster data comparisons: convert polygons to 10 x 10 m rasters; compare dominant Broad Habitat (BH) per 1 km square; sampling via grid points.
- 4.3 100-point grid: overlay and compare BH agreement at 100 points per square; identify concordant/motentially discrepant squares.
- 4.4 Attribute analysis: match reference IDs to compare species attributes within polygon-level matches.
- 7.1–8.1 Additional analyses for linear features and points; 9.1–9.3 Change recording assessment.

## Key Findings

- Broad Habitat (BH) agreement
  - 81% of squares recorded BH by both CS and QA as present; mean BH proportion differences mostly under 3.5% across many BH types.
  - Some BHs showed potential issues (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban) with notable standard deviations indicating differential allocation.
- Raster data comparisons
  - Overall raster agreement across squares averaged around 76%, with some squares very high (364, 488) and others poor (261, 773).
- 100-point analysis
  - General concordance good for many squares, but several squares exhibited substantial mismatches (e.g., 773 at 19% concordance; 261 at 41%).
  - When aggregated by BH/PH codes, most agreements were strong, but notable discrepancies existed in complex mosaics and upland/or machair-type habitats.
- Species attributes in polygons
  - 45% of QA polygons matched a CS polygon by location with at least one shared species.
  - Species concordance varied by habitat type; woodlands and Improved Grassland showed higher likelihoods of matched species; Bracken and upland mosaic habitats showed lower concordance.
  - 77% of polygons with species matches also had a matched BH, suggesting species data often aligned with habitat classification when polygons were spatially matched.
- Linear features and points
  - Linear features: high consistency in land-use-theme assignments between QA and CS; very few cases where QA flagged a feature not in CS, and minor confusions mainly between related feature types (e.g., belts of trees vs. woody linear features).
  - Points: overall good agreement on point habitat codes; some confusion between woodland/forest coding likely due to legacy coding practices.
- Change recording
  - Change coding largely aligned between CS and QA; digital changes supported clearer differentiation among Real Change, Error Change, No Change.
  - Some surveyors faced initial challenges with change-field usage; QA exercise helped clarify issues and improve consistency.

## Notable Issues and Interpretations

- Habitat definitions and updates
  - Blanket Bog definitions were revised for 2007, affecting coding in upland squares (e.g., squares 773, 991, 1034); highlights the importance of up-to-date, authoritative field keys and training.
- Habitat mosaics and small-scale variability
  - Mosaics in upland areas caused mismatches when disaggregating into component BHs; precise small-scale delineation remains challenging.
- Machair and Sand Dune habitats
  - Localized, distinctive habitats (machair) contributed to anomalies; underscores need for region-specific definitions and training.
- Woodlands classification
  - Some inconsistencies stemmed from definitions of Broadleaf vs Coniferous woodland; legacy field practices (allocation via matrices) complicated direct comparisons.
- Data integration and provenance
  - The exercise demonstrates the value of digital field data, but also the complexity of reconciling new digital mappings with legacy datasets and across partners.

## Change Recording and Species Analysis Insights

- Change coding consistency was strong for many habitat types and feature types, but some habitat-specific changes required careful interpretation, especially where habitat boundaries are ambiguous.
- Species-level concordance is lower than habitat-level concordance due to ecological complexity and dominance variances; improved standardization of dominant-species selection could raise cross-team agreement.

## Implications for Data Governance and Strategy (Data Leaders’ Perspective)

- Benefits of digital mapping and wiki-based QA: enhanced data quality, faster feedback loops, and clearer traceability of changes.
- Need for robust data standards
  - Harmonize habitat definitions, especially for contentious or mosaic habitats (e.g., Blanket Bog, urban grassland classifications, coniferous vs broadleaf woodland) to improve cross-team consistency.
  - Maintain and publish clear, versioned field keys and metadata; document any revisions (as done with Blanket Bog) and ensure training materials accompany changes.
- Training and capacity-building
  - Invest in targeted training for staff on updated habitat keys, mosaic interpretation, and change coding to reduce inter-operator variability.
- Data quality metrics and governance
  - Use multi-faceted QA metrics (BH agreement, raster concordance, 100-point concordance, species concordance, change coding alignment) to monitor data quality across cycles.
  - Maintain provenance trails: link QA outcomes to field teams, datasets, and versioned field handbook revisions to support auditability.
- Interoperability and future-proofing
  - Strengthen interoperability with prior datasets (1998, other national datasets) and ensure consistent alignment of geodatabases and metadata schemas.
  - Consider refining BH/PH mapping schemes to reduce cross-wab between similar habitats and to support scalable analysis across networks.
- Resource planning
  - Allocate QA coverage to capture representative land classes and mitigate access/refusal biases; plan for cross-square temporal consistency to account for vegetation changes.
- Community and collaboration
  - Continue cross-team collaboration to refine habitat definitions, share best practices, and align with wider data communities to support a more effective data ecosystem.

## Takeaways for Strategic Action

- Maintain digital-first data capture with rigorous, defined metadata and versioned field keys.
- Prioritize standardization and training around contentious habitats and mosaic classifications.
- Expand and optimize QA coverage to ensure representative spatial types and address areas with historically higher disagreement.
- Leverage multi-scale QA metrics to drive continuous improvement in data quality, interoperability, and governance.