# The Land Cover Map of Great Britain

- Overview
  - A land cover map produced from supervised maximum likelihood classifications of Landsat Thematic Mapper data.
  - Based on a 25 m grid, detailing 25 target cover-types plus an Unclassified category.
  - Combines summer and winter imagery to improve accuracy; about 88% of Britain classified from combined data; 0.4% obscured by cloud on both dates; offshore islands account for ~0.1%.

- Data, resolution and formats
  - Two primary data products:
    - 25-class dataset at 25 m resolution: each 25 m cell is labeled 1–25 (with 0 for Unclassified).
    - 1 km summary dataset: for each target class, a 1 km cell contains the percentage (0–100) of that class within the 1 km cell.
  - An alternative 17-class (key) dataset is provided for consistency, mapped from the 25-class set. The 17 classes are labeled A–Q in uppercase; 25-target classes retain numeric labels.
  - The 25-class data are standard; the 17-class data are provided as an option and used as the Countryside Information System standard.

- Classification accuracy and validation
  - Ground-truth data are limited; exact validation is challenging due to differing definitions and generalization.
  - Comparisons with independent ground data across 508 1 km squares show varying correspondences, depending on detail level and class definitions.
  - Major error sources:
    - Misclassification of mixed boundary pixels (about 40% of pixels touch a boundary).
    - Minor geometric misregistration can affect dissection or boundary alignment.
    - Time-based changes between surveys (e.g., pasture ploughed later) can affect agreement.
  - Overall accuracy estimates:
    - Realistic assessment around 80–85% when accounting for definition differences and temporal change.
    - If boundary pixels are excluded, correspondence increases to ~71%.
    - Including boundary pixels and temporal changes yields ~76% correspondence; with time-based changes considered, overall interpretation suggests typical accuracy in the 80–85% range.
  - Ground-truth-based assessments are inherently approximate due to definitional differences and data limitations.

- Land cover classes (25 target) and 17 key-class framework
  - 25 target cover-types: designed to be ecologically meaningful, consistently recognizable from Landsat imagery, and mappable at the 25 m scale.
  - 17 key classes: an aggregation of the 25 target classes to improve national consistency; useful when rarer classes are inconsistently mapped or when users require fewer categories.
  - The document provides detailed descriptions for each 25-class type (e.g., Sea/Estuary, Inland Water, Beach/Coastal Bare, Saltmarsh, Grass Heath, Pasture/Meadow/Amenity Grass, Moorland and Heath, Bracken, Scrub/Orchard, Deciduous and Coniferous Woodland, Tilled Land, Urban/Suburban Development, Inland Bare Ground, etc.), including spectral and ecological characteristics and notes on regional variations.
  - A crosswalk table links each of the 17 key classes (A–Q) to its corresponding 25 target class(es), enabling users to choose between higher-detail or more generalized outputs.

- Practical use and considerations for analysts
  - Two-tier classification approach:
    - Use the 25-class dataset for detailed, ecologically meaningful mapping.
    - Use the 17-key-class dataset for more consistent national comparability.
  - Data can be used in two formats:
    - Pixel-level 25 m data (values 1–25 or 0 for Unclassified).
    - 1 km summary data (per-class percentages within each 1 km cell).
  - Important caveats:
    - Some rarer classes may be mapped inconsistently across regions; regional masks or post-processing in GIS may be helpful.
    - Boundary pixel issues and temporal changes between imaging dates can influence accuracy; consider time-consistency when comparing over time.
    - Ground-truth comparisons are inherently imperfect due to differing definitions and measurement scales.

- Endnotes and references
  - The document references extensive methodological background and accuracy assessments (e.g., Congalton 1991; Fuller et al. 1989–1995; Wyatt et al. 1994; Townshend 1983).
  - Published supporting works detail classification methods, data availability, and cross-survey comparisons.

- Timing and authorship
  - Extracted from a 1995 release describing the 26 target land cover 1990 classes (with unclassified as 0, renumbered to 1–26 in downloadable data).
  - Associated with the Land Cover Map of Great Britain (LCMGB) work led by R. M. Fuller and colleagues at CEH Monks Wood.