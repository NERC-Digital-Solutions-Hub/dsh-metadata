# Mapping Quality Assurance Exercise

- Purpose and context
  - 2007 Countryside Survey aimed to deliver high-quality, comparable habitat and landscape data in a geodatabase for rapid analysis.
  - Shift to digital mapping (Surveyor software) to reduce interpretation errors and enable field mapping with real-time data prompts.
  - QA process used early data checks via an interactive wiki and in-field QA visits to ensure protocol adherence.

- Data and scope
  - QA covered 23 1-km squares across GB, selected by Land Class and location, with areas common to both QA and survey data.
  - Data collected in the field with mandatory fields (e.g., dominant species) and visit status indicators; data uploaded to a wiki for early office checks.

- QA and data workflow
  - Field data -> geodatabase -> QA comparison against CS survey data.
  - Analyses conducted to assess accuracy across multiple data representations:
    - Aggregate areas/lengths/points per square
    - Rasterized habitat maps (10 x 10 m cells within each 1 km square)
    - 100-point grid cross-checks for Broad/Priority Habitats
    - Polygon-level species attributes and habitat-change coding
  - Data alignment used masks to exclude unsurveyed or refused areas to ensure comparability.

- Analysis approaches (4.x sections)
  - 4.1 Direct comparison of aggregate areas/lengths/points for whole squares (CS vs QA)
  - 4.2 Comparisons of raster data (dominant Broad Habitat per 10x10 m cell; spatial concordance)
  - 4.3 100-point grid overlay to assess point-level concordance across habitats
  - 4.4 Attribute comparisons for areas, linears, and points (reference IDs and species attributes)

- Key findings: habitat mapping and data agreement
  - Direct aggregate comparison (6.1)
    - 81% of squares had a Broad Habitat (BH) presence recorded by both CS and QA.
    - Mean differences between CS and QA BH proportions were generally small: mostly under 3% for many habitats; some higher deviations for Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban.
    - Indicates largely minor differences in habitat allocation, with notable issues in a few habitat types.
  - Raster data comparison (6.2)
    - Overall raster agreement across squares averaged about 76%, with some squares very high (e.g., 364, 488) and others lower (e.g., 261, 773).
    - Agreement by habitat varied; detailed per-square differences highlighted where habitat coding diverged.
  - 100-point grid concordance (6.3)
    - Most squares showed good concordance between QA and CS; some squares with substantial mismatches (e.g., 773 and 261).
    - Concordance by habitat generally high, but variations existed; discrepancies often tied to upland mosaics and complex habitat boundaries.
  - Species and polygon attributes (6.4)
    - 45% of QA polygons had at least one species listed matching a CS polygon at the same location.
    - Of spatially matched polygons, 77% had matching Broad Habitat; overall species concordance around 40% across habitats.
    - Higher species concordance for woodland and Improved Grassland; lower for Bracken and upland mosaics.
    - Species lists showed common species with variable agreement; dominant-species choices influenced habitat coding.

- Habitat-specific challenges and interpretations
  - Blanket Bog: substantial mis-matches with Dwarf Shrub Heath due to evolving definitions; upland peat and bog classifications were especially tricky; training and definition refinement recommended.
  - Upland mosaics: small-scale variability and mosaic maps led to mismatches when disaggregating mosaics into component BHs.
  - Neutral vs Improved Grassland: overlapping species and cover complicate distinct allocations; no systemic bias between CS and QA in this area.
  - Woodland definitions: field key defined coniferous vs broadleaf woodlands; some inconsistencies noted in how woodlands were categorized when mixed or mosaicked.
  - Sand Dune machair (Scotland): an anomaly where machair vegetation overlapped Neutral/Improved Grassland categories; location-specific, not widespread.

- Change recording (9)
  - 2007 introduced more detailed change codes: Real change, Error Change, No change.
  - Some surveyors struggled with the change field, but overall agreement between CS and QA on change coding was high for most habitat types.
  - Digital workflow enabled updating previous maps and adding change context, though it added complexity to the survey process.

- Efficiency and data quality observations
  - Surveyors used visit-status layers effectively; very little land left unvisited (typical low Not Visited figures; occasional Refused Access issues).
  - Mandatory attribute fields increased species recording and overall data completeness.
  - Early QA visits helped ensure adherence to protocols and improved data consistency across teams.

- End-state implications and recommendations
  - Digital data collection and wiki-based QA enhanced data quality and timeliness, enabling near-real-time QA and cross-dataset comparisons.
  - Remaining issues to address in future work:
    - Refine and harmonize definitions for challenging habitats (notably Blanket Bog and upland mosaics).
    - Improve guidance around shrub/woodland classifications and their back-allocation in complex landscapes.
    - Enhance training to reduce interpretation differences in problematic habitat boundaries and mosaics.
    - Consider further methodological refinements for urban vs grassland allocations where confusion persists.
  - Overall conclusion: QA shows strong overall agreement between survey data and QA data across many habitats, with manageable discrepancies that point to targeted areas for definitional clarity and training improvements.