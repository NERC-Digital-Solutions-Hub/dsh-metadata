# Mapping Quality Assurance Exercise

- Overview and purpose
  - 2007 Countryside Survey produced high-quality habitat/landscape data intended to be compatible with previous methods and easily analyzable alongside other national datasets in a geodatabase.
  - Transitioned to digital mapping in the field (Surveyor software) to reduce errors from post-survey digitisation and handwriting issues.
  - Digital QA workflow: data uploaded to an interactive wiki for early data checks; QA teams conducted protocol adherence checks; emphasis on data accuracy, metadata completeness, and traceability.

- Data, systems and workflow
  - Field data capture using Surveyor software with mandatory fields, prompts, and visit-status layers to flag unvisited features.
  - Early data checks via an interactive wiki; QA teams performed on-site protocol verification.
  - Post-collection workflow: data uploaded to a geodatabase; unsurveyed or access-refused areas excluded from analysis; two datasets aligned for comparability.

- QA methodologies employed
  - 4.1 Direct comparison of aggregate areas/lengths/points for each 1 km square.
  - 4.2 Raster data comparisons: convert polygons to 10 x 10 m raster cells; compare absolute Broad Habitat extents and locations.
  - 4.3 100-point grid analysis: evaluate concordance of Broad Habitats at ~100 points per square; identify concordant vs discordant areas.
  - 4.4 Attribute comparison for areas/lines/points using reference ID layers to align QA and surveyor data.

- Key findings: habitat mapping (Broad/Priority Habitats)
  - General agreement: in 81% of squares, a Broad Habitat (BH) was recorded by both CS and QA for a given square.
  - Differences: mean differences between QA and CS BH extents mostly under 1–3.5% across most BHs; some habitats showed larger SDs indicating potential differential allocation (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and certain upland habitats).
  - Notable issues:
    - Blanket Bog: significant discrepancies tied to evolving definitions and field interpretation; in particular, moss/heather-dominated mosaics (e.g., Dwarf Shrub Heath vs Blanket Bog) caused misclassifications in some squares (notably 773, 991, 1034).
    - Grasslands and woodlands: overlaps/definitions between Broadleaf and Coniferous woodland present; urban vs grassland labeling ambiguities observed.
    - Upland mosaics: mosaicked landscapes in which precise BH allocation is challenging; small-scale mosaics can inflate mismatches.
    - Machair/special habitats on Scottish dunes affected some squares, illustrating the challenge of local habitat peculiarities.
  - 6.2 Raster data comparisons: average agreement across squares ~76%, with some squares high (e.g., 364, 488) and others low (e.g., 261, 773).
  - 6.3 100-point concordance: overall good agreement for many squares but notable mismatches in some (e.g., 773: 19%, 261: 41% concordance).
  - 6.4 Polygon-level species attributes: 45% of QA polygons matched with CS polygons for at least one listed species; 77% of matched polygons also had a matching BH. Species concordance overall around 40%; commonly recorded species show higher concordance for certain habitat types (woodlands, Improved Grassland). Lolium perenne showed notable agreement (66% in common species).
  - 6.5 Species lists: broader species concordance lower than BH concordance, reflecting greater variability in species composition and the influence of dominant species on BH classification.

- Key findings: linear, point features and change recording
  - 7.1 Linear features: lengths across squares show only minor differences; high consistency in land-use theme assignments (e.g., fences vs walls, forestry belts); some confusion between specific forestry-related codes (FO vs WNS/WUS) but overall robust alignment.
  - 8.1 Points: similar overall agreement in point-feature counts by land-use theme; veteran trees showed the greatest discrepancy between CS and QA due to field instructions (limit of two trees per species).
  - 9. Change recording: digital change field allowed more detailed coding (Real change, Error change, No change); some early surveyor confusion with the change field, but overall agreement between CS and QA on change coding improved as the system matured. Change records could be used to update prior maps, addressing historical inaccuracies.

- Data governance and stewardship implications
  - Digital field workflow demonstrates strong data provenance, with explicit capture of change and metadata, enabling better traceability and auditability.
  - Definitions and classification schemes (e.g., Blanket Bog, coniferous vs broadleaved woodland) require ongoing refinement to improve cross-survey consistency; need for clear, up-to-date field manuals and training.
  - Mosaic and small-scale habitat boundaries highlight challenges in operational definitions; may necessitate refinement of hedges between BH categories and consideration of mosaic mapping practices.
  - Emphasizes the necessity of robust metadata, versioning, and change-tracking workflows to maintain data integrity as datasets are updated over time.
  - Findings support the publishing/data-sharing goal: datasets are more readily discoverable and interoperable when standardized, with explicit QA results guiding data consumers about reliability and known limitations.

- Endnotes and overall conclusion
  - The 2007 mapping QA exercise demonstrates a high degree of consistency between CS surveyors and QA teams across a broad range of habitats and features, validating the digital mapping and QA approach.
  - Remaining discrepancies, especially around Blanket Bog definitions, upland mosaic mapping, and certain grassland/woodland delineations, point to targeted areas for definitional refinement, training, and potential methodological tweaks.
  - Overall, the digital QA framework enhances data quality, provides richer metadata and change-tracking, and supports improved data governance, stewardship, and interoperability for national-scale ecological datasets.