# Mapping Quality Assurance Exercise

- Context and purpose
  - Countryside Survey 2007 produced high-quality habitat and landscape data designed to be compatible with previous approaches and suitable for rapid analysis in a geodatabase.
  - Digital mapping was introduced to reduce subjective interpretation and post-survey transcription errors, with field mapping via the Surveyor software and mandatory data fields.
  - Early QA was integrated through a wiki portal and supervisory QA visits to ensure protocols were followed.

- Data collection, systems and governance
  - Surveyors used Surveyor with mandatory prompts and visit-status tracking; data uploaded to a wiki for immediate post-field checks.
  - QA teams conducted in-field and office-based checks to ensure adherence to protocols.
  - Data management included masking unsurveyed or access-denied areas prior to comparative analysis; results were stored in a single geodatabase for consistency.

- QA approaches and methodologies
  - Mapping QA coverage: 23 one-kilometre squares, selected to represent land-class variety; emphasis on different mapping squares to reduce owner-related bias.
  - Direct comparisons: aggregate area/length/point metrics exported to SAS for Square-by-Square comparisons (CS vs QA).
  - Raster comparisons: each 1 km square subdivided into 10,000 cells (10x10 m) to compare dominant Broad Habitat across datasets; resolution-based sampling for attribute analysis.
  - 100-point grid analysis: overlaid points to assess spatial concordance of Broad Habitats between CS and QA datasets; both positive concordances and discrepancies documented.
  - Feature-level analyses: reference ID layers created to compare species attributes within matched polygons (areas, lines, points).
  - Change recording: new digital change field capturing Real change, Error change, No change; alignment between QA and CS on change codes analyzed.

- Findings: habitat and attribute concordance
  - Overall, high agreement for many Broad Habitats between CS and QA, with most squares showing close alignment in habitat proportions.
  - Notable discrepancies observed in several habitats:
    - Neutral vs Improved Grassland
    - Broadleaf vs Coniferous woodland
    - Upland habitats (Acid Grassland; Fen, Marsh, Swamp)
    - Urban areas vs grassland classifications
    - Sand Dune/machair habitats and Blanket Bog versus Dwarf Shrub Heath
  - Blanket Bog: major source of misclassification, driven by evolving definitions and field handbook revisions; cross-square issues (notably square 773) linked to experience differences and habitat overlap (wet heath over blanket bog).
  - Mosaic upland habitats: mosaics and subsequent disaggregation led to mismatches when comparing “like” Broad Habitats within mosaics.
  - Machair in Scottish dunes: localized, overlapping with Neutral/Improved Grassland classifications, highlighting landscape/location effects on habitat coding.

- Raster and 100-point concordance
  - Raster-level agreement: average around 76% across squares, with some squares achieving high concordance (e.g., 364, 488) and others showing poor agreement (e.g., 261, 773).
  - 100-point concordance: majority of squares showed good concordance, but some important outliers exhibited substantial mismatches (e.g., squares 773 and 261 with low concordance percentages).
  - Differences by Broad Habitat: generally good matches for many habitat types; some discrepancies concentrated in Neutral/Improved Grassland, Urban areas, and certain woodland classifications.
  - Summary: most habitat agreements are solid, but certain habitat definitions and mosaic mapping challenges reduce concordance in specific squares or habitat types.

- Species attributes and polygon analyses
  - Polygon-level species data: 1,081 QA polygons and 998 CS polygons; around 45% of QA polygons matched at least one species in the corresponding CS polygon.
  - Species concordance varied by Broad Habitat; woodland and Improved Grassland showed relatively higher species concordance, while other habitats showed lower alignment.
  - Species lists within matched polygons indicated that common species (e.g., Lolium perenne) often showed higher agreement, while many others varied between QA and CS lists.

- Change recording outcomes
  - Introduction of detailed change coding (Real, Error, No change) supported more nuanced data updates and historical data correction.
  - Overall alignment between QA and CS change coding was strong across most Broad Habitats and linear features; some habitat-level changes remained challenging to assess due to complexity of habitat definitions in certain contexts.

- Data governance implications and recommendations
  - Definitions and harmonization: continue refining habitat definitions (notably Blanket Bog; Broadleaf vs Coniferous woodland) to reduce cross-squad interpretive differences.
  - Training and expertise: enhance field and QA training to handle upland mosaics and localized habitats; improve consistency across survey teams with standardized guidelines.
  - Metadata and lineage: document detailed metadata for data provenance, QA methods used, and change-coding conventions; ensure traceable data lineage from field collection to publication.
  - Versioning and update workflows: establish robust update procedures to reflect approved changes (change field usage) and maintain versioned datasets across habitats, linears, and points.
  - Interoperability and discoverability: maintain standardized data models (BH/PH codes, geodatabase schema) to facilitate integration with national datasets and external portals; provide clear documentation for data users.
  - Continuous improvement: use QA findings to inform future survey design, including handling of mosaics, urban-rural interfaces, and dune/machair contexts; consider targeted recalibration where discrepancies were most pronounced.

- Bottom-line for data stewards
  - The 2007 Mapping Quality Assurance Exercise demonstrates strong overall data quality and usable interoperability between field-collected data and QA assessments, but also highlights critical areas for governance: clear, up-to-date habitat definitions; thorough metadata and change-tracking; training to reduce interpretation variance; and documented, auditable data update paths to maintain dataset reliability and discoverability for downstream users.