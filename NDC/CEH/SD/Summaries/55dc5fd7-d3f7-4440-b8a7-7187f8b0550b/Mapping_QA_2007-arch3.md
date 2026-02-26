# Mapping Quality Assurance Exercise

- Purpose: Report on the 2007 Countryside Survey (CS) mapping QA to ensure high-quality, comparable habitat and feature data suitable for national-scale analysis and integration with other spatial datasets.

- Context: Transition from post-survey digitisation of paper maps to field-based digital mapping using Surveyor software; early field- and office-based QA via a wiki; aim to reduce subjectivity and improve data clarity and accessibility.

- Scope: QA exercise covering 23 one-kilometre squares, conducted in parallel with CS data collection; designed to test mapping accuracy, attribute coding, and data governance against CS standards.

- Governance and data practices:
  - Use of geodatabase for centralized data management; data uploaded to an interactive wiki for early checks.
  - Mandatory data fields for features to improve field-level data integrity.
  - Discussion of data sharing and metadata quality as ongoing considerations.

- What was compared and how (Methods):
  - Direct aggregate comparisons of square-level extents and attributes for habitat, linear, and point features.
  - Raster-based comparisons by converting polygons to a 10x10 m grid within each square and sampling with a resolution grid.
  - 100-point grid analysis to assess concordance of Broad Habitats between CS and QA at a consistent, prior QA resolution.
  - Attribute-level comparisons using reference IDs to align QA and CS data for areas, lines, and points.
  - Separate analyses for surveyor efficiency, linears, points, and change coding.

- Data and sampling details:
  - QA covered 23 squares; access refusals and landowner concerns influenced surveying and representativeness.
  - Data processing included masking unsurveyed areas and aligning CS and QA datasets for common surveyed areas.

- Key findings: overall agreement and where discrepancies occurred
  - Broad Habitat (BH) presence: 81% of squares showed BH presence recorded by both CS and QA; most BH proportions differed by less than 1–2% on average, with some habitats showing larger differences.
  - 6.1 Direct comparison of aggregate areas: most BHs exhibited small mean differences; notable variability for Improved grassland, Neutral grassland, Dwarf Shrub Heath, Bog, Urban, and Blanket Bog; upland mosaics and recent key definitions contributed to mismatches.
  - 6.2 Raster data comparisons: average raster agreement across squares ≈ 76%; high concordance in several squares (e.g., 364 ≈ 98%), but substantial discordance in others (e.g., squares 261 ≈ 49%, 773 ≈ 23%).
  - 6.3 100-point concordance: overall concordance around 77% for BHs; some squares showed lower concordance (e.g., 773 at 19–41%), while others showed strong agreement (e.g., 364 at ~95–98%).
  - 6.4 Polygon species attributes: 45% of QA polygons matched at least one species with the corresponding CS polygon; 77% of those had matching BH. Species concordance across polygons was around 40%, with common species showing higher agreement for certain habitat types (woodlands, Improved Grassland). Post-hoc issues linked to habitat allocation decisions.
  - 7.1 Linear features: generally high consistency in land-use theme classifications; limited cases where QA recorded a feature that CS did not; some ambiguity between belts of trees (FO) and woody linear forms (WNS/WUS).
  - 8.1 Points: habitat codes for buffered point features showed high consistency; occasional confusion between woodland codes; overall strong cross-check results.
  - 9 Change recording: digital change-coding (Real change, Error change, No change) largely aligned between CS and QA; some complexity led to occasional disagreements, but the digital workflow helped clarify changes and update prior maps.

- Notable issues and interpretations
  - Blanket Bog: major source of disagreement; evolving definitions and field-key revisions in 2007 created mis-matches with Dwarf Shrub Heath; highlighted need for refined, consistent definitions and training.
  - Urban vs Grassland: inconsistencies in classifying Urban areas as Improved Grassland; calls for clearer guidance in field handbook.
  - Mosaic upland habitats: mosaics mapped as multiple BHs caused potential mis-matches when disaggregated for comparison; reflects the difficulty of mapping continuous habitat gradients at small scales.
  - Machair on Scottish sands: localized anomaly where machair vegetation aligned with Neutral/Improved Grassland in classifications—present but limited impact on overall results.
  - Species-level concordance: 45% polygon match for listed species; higher concordance for conspicuous, dominant species (e.g., Lolium perenne); overall species-level agreement influenced by habitat type and dominance patterns.

- Practical implications and recommendations
  - Digital QA is effective for improving data integrity and enabling in-field verification, but requires ongoing refinement of habitat definitions and user guidance.
  - Training and field handbook updates are essential to reduce misclassifications in challenging habitats (notably Blanket Bog, Bog/Dwarf Shrub Heath, urban grassland distinctions).
  - Metadata quality and data provenance remain critical; attention to data standardization and interoperability with other national datasets is important.
  - Further analyses are warranted to understand how species composition influences habitat allocation and to refine BH definitions for future surveys.
  - Acknowledgment that mosaics and continuum habitats pose inherent challenges for precise pixel- or polygon-level validation and require nuanced interpretation and possibly adaptive mapping approaches.

- Conclusion
  - The 2007 Mapping Quality Assurance Exercise demonstrates a robust, largely consistent alignment between CS surveyors and QA assessments across most habitat types, linears, and points, supported by a strong digital data framework.
  - While overall concordance is high, certain upland and peatland habitats (especially Blanket Bog) and urban/grassland distinctions require definitional clarity and targeted training to maximize future data quality and comparability.
  - The exercise affirms the value of integrated QA in monitoring framework development, data governance, and informing future survey design and data sharing practices.