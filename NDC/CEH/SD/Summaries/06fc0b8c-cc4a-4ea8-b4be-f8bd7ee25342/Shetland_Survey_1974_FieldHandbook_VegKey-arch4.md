# Explanation of Ecological Type Summaries

## Purpose and Scope
- Provides an introduction to fuller ecological type summaries and a rapid method to check affinities of a given plot.
- Focuses on a standardized typology of vegetation types, detailing dominant and indicator species, environmental context, and occurrence across islands.

## Structure of Type Summaries
- Types are labeled Type 1 through Type 32 (and related variants), each describing:
  - Major cover species (dominant plants)
  - Selective (indicator) species with frequency notes
  - Presence or absence of bare ground
  - Indicator groups (A, B, C, etc.) treated as constants
  - Typical or average occurrence and geographic distribution (e.g., mainland, specific islands)
  - Relationships to habitat features (peat depth, soil moisture, pH) and environmental conditions
- A GLYPH scoring system is used to quantify indicator species:
  - Positive and negative indicator species are assigned GLYPH values
  - Type classifications are influenced by thresholds (e.g., Score +1, +2, etc.)
- Environmental parameters accompany types:
  - Soil depth categories (e.g., shallow, medium, deep)
  - Wetness/soil moisture index (Dry, Damp, Very Wet, Submerged)
  - pH ranges (e.g., around 4.3–6.3, with typical averages per type)
- Occurrence categories describe how commonly each type occurs:
  - Limited occurrence
  - Average occurrence
  - Widespread occurrence
  - Constant species groups or plots across the surveyed area

## Environmental and Soil Context
- Types are linked to specific soil and hydrological conditions:
  - Peat depth and whether peat is deep, damp, or alternating with drier areas
  - Soil moisture and water presence (streamsides, ditches, pools)
  - pH ranges from acidic to near-neutral, with average values specified per type
- Vegetation often associated with particular substrate and landscape features:
  - Eroded peat surfaces, bare peat patches, water channels
  - Rocky outcrops, sea proximity, marshy conditions, and peat diggings
- Species groups (A, B, C, D, F, G, etc.) are treated as constants and help define type boundaries

## Indicator Species and GLYPH Scoring
- Indicator species are categorized as positive or negative for Type assignment
- GLYPH scoring provides a quantitative basis for classification:
  - Scores from +1, +2, etc., or negative values influence Type designation
  - Specific Type numbers are associated with ranges of GLYPH scores (e.g., Type 2, Type 5, Type 10, Type 15, Type 22, Type 29, etc.)
- Indicator species lists are provided for each type, including common and selective taxa (e.g., Cladonia species, Sphagnum, Calluna, Eriophorum, Carex, Drosera, etc.)

## Geographic Occurrence and Distribution
- Types vary in geographic scope:
  - Some are absent from certain islands (e.g., Yell, Unst) or restricted to coastal/maritime areas
  - Others are widespread across the archipelago, with occasional absence from more remote locations
- Occurrence categories help prioritize surveying and data collection efforts

## How to Use the Type System in Practice
- To classify a plot:
  - Identify dominant cover species and compare with Type descriptions
  - Check for presence and frequency of indicator species with GLYPH scores
  - Assess environmental context (peat depth, wetness, pH) and match to Type environmental profiles
  - Consider geographic distribution and the constants (A, B, C, etc.) associated with each Type
- Use as a basis for mapping vegetation types, monitoring habitat change, and informing conservation or management decisions

## Data Leader Considerations
- Data standardization and governance
  - Adopt a consistent schema for TypeID, Type name, dominant and indicator species, GLYPH scores, and environmental fields
  - Maintain versioned Type lists and clear provenance for each classification
- Metadata and data quality
  - Capture metadata for pH, soil depth, wetness index, and other environmental parameters
  - Document survey methods, taxonomic references, and geographic scope (which islands or regions)
- Discoverability and collaboration
  - Centralize Type summaries to enable cross-team and cross-partner data sharing
  - Establish common definitions for terms like "major cover species," "indicator species," and GLYPH scoring
- Data model and analytics
  - Suggested fields: TypeID, TypeName, MajorCoverSpecies, IndicatorSpecies (with GLYPH), BareGroundPresent, OccurrenceCategory, GeographicDistribution, SoildDepthCategory, WetnessIndex, pH, HabitatNotes, ConstantsA_B_C_D, ReferencePlotIDs
  - Enable cohort analyses to track Type prevalence over time and across locations
  - Integrate with user needs by supporting feedback loops to refine Type assignments and update classifications as data quality improves