# Mapping Quality Assurance Exercise

- Aim and context
  - 2007 Countryside Survey produced high-quality habitat and landscape feature data compatible with earlier approaches, enabling fast analysis in a geodatabase alongside national datasets.
  - Shift to field digital mapping using Surveyor software to reduce interpretation errors, improve data clarity, and enable immediate data checks via a wiki.
  - QA integrated early in the process with field and office teams; three QA approaches used to compare surveyor-mapped data with QA-collected data.

- Scope and data management
  - QA covered 23 1km squares; squares selected by land class and location to represent GB diversity; focus on common surveyed areas when access was refused.
  - Data collected via standard Countryside Survey tablets; feeds into a single geodatabase; unsurveyed/refused areas excluded from analyses to ensure comparability.
  - Data were analysed at multiple scales and formats: aggregate (square-level), raster (10x10 m cells per square), and 100-point grid concordance; attributes (areas, lines, points) compared using reference IDs.

- Methodological approaches
  - Direct comparison: aggregate areas/lengths/points by square, land class, and Broad Habitat (BH).
  - Raster comparison: convert polygons to a 10,000-cell (10x10 m) grid per square, assign dominant BH, and compare QA vs surveyor data; sampling via resolution grids.
  - 100-point grid: overlay 10x10 point grid per square to assess spatial concordance of BH mapping; positives/negatives recorded to gauge agreement.
  - Attribute comparisons: generated reference ID layers to compare species attributes for matched polygons.
  - Surveyor efficiency: tracking visit status layers; analysis of not-visited vs refused access areas; assessment of species recording improvements due to mandatory fields.
  - Change recording: introduced explicit change codes (Real Change, Error Change, No Change) to document data updates and errors; evaluation of agreement on change coding between CS and QA.

- Key quantitative findings (overall patterns)
  - Coverage and general agreement
    - 81% of squares had BH recorded by both CS and QA teams; mean BH proportion differences were typically under 3.5% (often <1%) for many BHs.
    - Direct aggregate comparisons showed small differences in BH extents across most habitats; some BHs (e.g., Improved/Neutral Grassland, Bog, Dwarf Shrub Heath) exhibited higher variability.
  - Raster data concordance
    - Overall raster agreement across squares averaged around 76%, with several squares achieving high concordance (e.g., 364 = 98%, 488 = 94%, 359 = 69%, 261 = 49%, 773 = 23%).
  - 100-point concordance
    - Square-level concordance varied; strong concordance in some squares (355 ≈ 84%, 359 ≈ 92%, 364 ≈ 96%), but poor in others (261 ≈ 41%, 773 ≈ 19%).
  - Habitat-level patterns (Table-based insights)
    - Most BH/PH mappings showed good agreement across squares (e.g., Broadleaved woodland, Coniferous woodland, Arable/Horticulture, Improved Grassland).
    - Notable inconsistencies included Neutral vs Improved Grassland, Broadleaf vs Coniferous woodland, and upland mosaics where multiple BHs coexist in a single square.
    - Machair/machair-related machair habitats in Scottish squares caused anomalies, illustrating local habitat definition challenges.
    - Blanket Bog emerged as a major difficulty, with several mismatches between Dwarf Shrub Heath and Blanket Bog, influenced by field interpretation and evolving key definitions.
  - Species and polygon analyses
    - 1,081 QA polygons and 998 CS polygons; after spatial matching, 45% of QA polygons had at least one listed species matching the CS polygon in the same location.
    - Species concordance for matched polygons around 40%; QA tended to record more species, with common species (e.g., Lolium perenne) showing higher concordance.
    - For habitat-specific species concordance, some habitats (e.g., woodlands, Improved Grassland) showed higher matching of listed species than others (e.g., Bracken, Upland mosaics).
  - Change recording
    - Use of digital change codes generally aligned with QA expectations; higher agreement for linear and point features than for broad habitats due to inherent definitional ambiguities.
    - Tables 9.1–9.3 indicate broad agreement across habitat types and feature types, with some expected discrepancies in complex habitats or where definitions were updated between survey years.

- Habitat- and data-quality implications
  - Definitions and classification consistency
    - Issues with woodland definitions (Broadleaf vs Coniferous) and with the updated 2007 Blanket Bog descriptions highlight the need for ongoing standardization and training.
  - Upland and mosaic mapping challenges
    - Upland peatlands and mosaicked landscapes complicate strict BH allocations; mosaics were disaggregated for analysis, which may artificially increase mismatches.
  - Special-case habitats
    - Machair and other coastal/machair-like habitats caused local anomalies; underscores the need for region-specific guidance and robust keys.
  - Data capture and workflow advantages
    - In-field mandatory fields improved data completeness (e.g., more species recorded, consistent feature attributes), and wiki-based QA enabled early issue resolution.
  - Change-tracking value
    - Explicit change coding supports time-series integrity and data corrections; however, interpretation of change remains complex, particularly for habitat-level changes.

- Implications for GIS practice and recommendations
  - Digital field mapping and integrated QA workflows improve data quality and timeliness, supporting rapid GIS-enabled analyses and decision-making.
  - Maintain and update clear, regionally aware habitat definitions and keys; provide targeted training to reduce cross-team misclassification (e.g., Blanket Bog, upland mosaics, urban vs grassland).
  - Address data mosaic challenges by refining methods for disaggregation/mapping when habitats grade into one another; consider enhanced rules for mosaic areas.
  - Ensure consistent data standards across layers (areas, lines, points) and harmonize changes across time series to improve comparability.
  - Use rasterization and 100-point analyses as standard QA tools to identify squares with systematic discrepancies for targeted review.
  - Continue leveraging in-field change and species coding, but complement with post-field verification to improve species-level concordance.

- Notable methodological and results highlights for GIS practitioners
  - QA approaches demonstrated strong overall data consistency across aggregates, rasters, and 100-point grids, with some squares requiring closer review.
  - The digital workflow reduced interim digitisation error and improved data reliability, while revealing nuanced challenges in habitat definitions and upland mosaics.
  - The combination of direct attribute comparisons, raster-based extents, and point-grid concordance provides a comprehensive framework for GIS QA in large-scale habitat mapping projects.