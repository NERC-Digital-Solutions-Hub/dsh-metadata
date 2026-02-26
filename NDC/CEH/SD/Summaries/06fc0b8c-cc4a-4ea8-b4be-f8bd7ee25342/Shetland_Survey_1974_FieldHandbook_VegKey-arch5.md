# Explanation of Ecological Types

- Overview
  - Presents a standardized, phrase-based taxonomy of vegetation types across island plots.
  - Aims to enable rapid checking of affinities between datasets and to support discovery and reuse.
  - Uses standardized phrases rather than figures where possible; includes environmental context (pH, soil depth, and soil moisture) alongside species composition.

- Data Model and Metadata
  - 32 discrete vegetation Types (Type 1 through Type 32), each with:
    - Heterogeneity level (low, average, high) and average species complement.
    - Major cover species (dominant species driving the type).
    - Indicator species (positive, negative) with scoring (GLYPH values) that contribute to Type assignment.
    - Species groups (A, B, C, D, etc.) that are constants for the type.
    - Typical occurrence (limited, average, widespread) and geographic distribution notes (e.g., absent from certain islands).
    - Habitat associations (peat depth, moisture/wetting, and surface characteristics) and environmental conditions (pH ranges, peat type).
  - Environmental parameters captured per type:
    - Soils: peat depth categories (shallow, medium, deep; with some plots >50 cm).
    - Wetness: soil moisture index with categories (Dry = 0, Damp = 1, Very Wet = 3, Submerged = 4).
    - pH: ranges generally around 4.3 to 6.3, with typical values noted per type.
  - Indicator framework:
    - Positive and negative indicator species lists, with scoring thresholds that map to Type assignments.
  - Geographic scope:
    - Descriptions reference island-wide occurrence patterns and notable absences (e.g., Unst, Yell, etc.), indicating spatial applicability and transfer considerations.

- Environment and Species Indicators
  - Major cover species drive Type characterization (e.g., Calluna, Eriophorum angustifolium, Drosera rotundifolia, etc.).
  - Indicator species provide diagnostic signals for Type classification (with explicit positive/negative designations and score thresholds).
  - Some Types emphasize particular habitat features (e.g., marshy conditions, streamsides, rock outcrops, peat depth, and proximity to sea).

- Type Descriptions (Overview)
  - Types are described as variations around core habitat and species assemblages, with cross-references indicating related types (e.g., similar to Types X and Y).
  - Common themes include:
    - Dominance of Calluna vulgaris and associated bryophyte/lichen communities.
    - Variation in peat depth and moisture, from deep wet peat to damp shallow soils.
    - Gradients of heterogeneity and species richness.
    - Coastal and inland distributions with occasional regional absences.
  - Each Type provides a compact narrative about likely habitat, typical occurrence, and key diagnostic species.

- Data Governance and Stewardship Considerations
  - Use as a controlled vocabulary to standardize vegetation-type coding across datasets.
  - Require consistent taxonomic naming and harmonization of indicator species lists to maintain interoperability.
  - Metadata should document Type definitions, environmental context (pH, depth, moisture), and occurrence patterns to support reproducibility.
  - Versioning and provenance tracking needed to manage updates to Type descriptions or indicator lists.
  - The scoring framework (GLYPH values) should be implemented with clear rules to assign a Type from observed data.

- Practical Implications for Data Sharing and Discovery
  - Data collection workflows should capture:
    - Species inventories (major, indicator, and constant groups).
    - Environmental measurements (peat depth, soil moisture, pH).
    - Spatial context and island-specific occurrence notes.
  - Datasets should be annotated with Type labels and the rationale (indicator signals) to support re-use and cross-dataset comparisons.
  - Data portals/catalogues can leverage the Type taxonomy to enable rapid affinity checks and dataset discovery across platforms with a shared vocabulary.

- Key Challenges
  - Incomplete understanding of user needs may hinder effective Type selection and metadata capture.
  - Timely access to data from field collection is necessary to apply Type classifications accurately.
  - Harmonizing data across many systems and formats, especially given rich indicator lists and scoring rules.
  - Managing data for large or complex datasets, including lengthy indicator tables and regionally varying occurrences.