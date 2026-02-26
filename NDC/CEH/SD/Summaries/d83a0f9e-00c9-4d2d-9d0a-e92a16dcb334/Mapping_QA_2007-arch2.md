# Mapping Quality Assurance Exercise

- Purpose and context
  - Evaluates the quality of digital habitat and landscape mapping from the 2007 Countryside Survey (CS) to ensure compatibility with previous methods and with national spatial datasets.
  - Introduced field-based mapping with a dedicated software package (Surveyor) to reduce interpretation errors and improve data clarity.
  - Used an interactive wiki for early data checks and QA teams to monitor protocol adherence; QA visits ensured consistent data collection.

- Data and process framework
  - Digital mapping in the field with mandatory fields and prompts; visit status layers helped identify unmapped features.
  - Data uploaded to a wiki for early office-based checks; QA teams conducted independent verification in multiple squares.
  - QA focused on three parallel approaches to assess data quality:
    - Direct comparison of aggregate areas/lengths/points by 1 km squares.
    - Raster data comparisons by converting polygons to 10 m x 10 m raster cells.
    - 100-point grid analysis to assess spatial concordance of Broad Habitats (BH) at a standard resolution.

- Coverage and scope
  - QA mapping covered 23 1 km squares; some areas inaccessible or refused access reduced sample size.
  - Analyses aligned QA and CS data to common surveyed areas using masks to ensure comparability.

- Analysis methods and metrics
  - 4.1 Direct comparison: assessed BH and feature extents per square (areas, lines, points).
  - 4.2 Raster data: compared dominant BH per 10x10 m cell; evaluated absolute amounts and locations.
  - 4.3 100-point grid: overlaid 100 points per square to gauge concordance of BH between QA and CS at specified resolution.
  - 4.4 Attribute comparison: used reference IDs to align attributes across QA and CS for areas, lines, and points.

- Surveyor efficiency and data quality improvements
  - Digital system and wiki-based checks improved efficiency and data integrity.
  - Notably low not-visited land area (average around 0.4%), with most squares fully covered when access allowed.
  - Mandatory data fields increased the number of species recorded per area.

- Key results by analysis approach
  - 6.1 Direct comparison of aggregate areas
    - BH agreement across squares: 81% of cases had BH recorded by both CS and QA.
    - Mean differences between CS and QA generally small: under 1% for many BH; up to 2–3.5% for others.
    - Some BH-specific discrepancies: Improved grassland, Neutral grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral sediment showed potential issues.
    - Blanket Bog: significant definitional challenges; debates and field handbook revisions in 2007 highlighted; ongoing refinement planned.
  - 6.2 Raster data comparisons
    - Overall raster agreement across squares averaged around 76%, with some squares showing high concordance (e.g., 364, 488) and others low (e.g., 261, 773).
    - Tabled BH-specific agreement revealed areas of stronger/weaker concordance and highlighted problematic habitats in particular squares.
  - 6.3 100-point grid
    - Concordance varied by square; several squares showed good concordance (e.g., 364, 359) while others lagged (e.g., 773, 261).
    - Most BHs achieved reasonable agreement; some issues dominated by mosaics, upland variability, or rare habitats (e.g., machair on Scottish dunes).
    - Matrix analyses showed common mismatches between broad and priority habitats, reflecting definitional and contextual differences.
  - 6.4 Polygon analysis of species attributes
    - About 45% of QA polygons had at least one shared species with the CS polygon at matching locations.
    - Species concordance across matched polygons was around 40%, with higher concordance for woody habitats and Improved Grassland.
    - Dominant species lists varied; Lolium perenne frequently matched, while others showed varying levels of agreement.
  - 7.1 Linear features
    - Lengths of linear features per square were broadly consistent; buffering QA lines to CS data (5 m) allowed robust comparison of land-use themes.
    - High consistency in land-use theme allocation; few mismatches when comparing similar feature types (e.g., fences vs walls).
  - 8.1 Points
    - Point feature habitat codes showed strong consistency across QA and CS datasets; some confusion around woody/woodland classifications noted.
    - Buffering and matching approaches provided reliable cross-checks for point-based habitats.
  - 9 Change recording
    - Transition to digital change recording allowed more detailed change coding (Real change, Error change, No change).
    - Overall agreement on change coding was strong for many habitats and feature types, though habitat-specific challenges remained (e.g., blanket bog and mosaic habitats).
    - Some surveyors initially struggled with change coding; QC exercises and training aided interpretation.

- Habitat-specific and methodological considerations
  - Blanket Bog: complex, regionally important; marked discrepancies between CS and QA; key definitions revised in 2007; further work proposed to refine definitions and back-coding.
  - Grassland classifications: Neutral vs Improved grassland showed overlap in species, leading to potential misallocation; balance observed across datasets.
  - Woodland definitions: Distinctions between Broadleaved, Coniferous, and the Woodland key caused some mismatches; field handbook clarifications were needed.
  - Upland mosaics: mosaicked habitats in upland squares posed matching challenges; mismatches often reflect mapping scale and habitat gradients rather than data errors.
  - Sand dune machair: Scotland-specific habitat caused anomalies; largely aligns with Neutral/Improved Grassland categories in practice.
  - Species-level concordance: 40% match across spatially matched polygons; specialist or mosaic habitats tended to produce lower species concordance.

- Implications for policy-relevant environmental monitoring
  - Overall positive alignment between QA and CS data supports the reliability of the 2007 mapping effort and its integration with national datasets.
  - The three QA approaches provide a robust framework for ongoing monitoring: aggregate validation, spatially explicit raster checks, and point-grid concordance.
  - Identified areas for definitional refinement and targeted training to reduce habitat-specific discrepancies.
  - Digital data collection and immediate QA feedback improve data timeliness, quality, and the ability to track changes over time.

- Recommendations and opportunities for analysts
  - Continue refining habitat definitions, particularly Blanket Bog, Neutral vs Improved Grassland, and woodland classifications, to reduce cross-dataset misallocations.
  - Maintain and expand digital QA workflows, including training to improve consistency in mosaicked upland habitats.
  - Leverage the demonstrated data consistency to enable more integrated analyses with other national spatial datasets and temporal monitoring.
  - Consider enhancements to 100-point and raster methodologies to handle mosaics and rare habitats more effectively.
  - Promote and facilitate access to QA and CS underlying data to enable broader scrutiny, replication, and re-use across organizations.