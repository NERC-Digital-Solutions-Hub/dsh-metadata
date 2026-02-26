# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

## Overview
- Presents the relationship between Broad Habitats (BHs) and LCM2000 Target Classes, Subclasses and Variants (Suclasses) as displayed in maps.
- Includes a comprehensive enumeration of habitat types and their coding across LCM2000, including cross-references to regionally broken coverage.
- Provides extensive area statistics (km²) for BHs, Subclasses, and Aggregates for England, Wales, Scotland, Northern Ireland, and the UK, based on LCM2000 and field survey (FS) data.
- Notable emphasis on how coastal/intertidal areas are treated and variability in coastal coverage.

## Data Structure and Classification
- LCM2000 uses a hierarchical classification:
  - Target Class (broad category)
  - Subclass (more specific category)
  - Variant (variant forms within a subclass)
- The table links each Broad Habitat to its corresponding LCM Target Class, Subclass, and Variant, with map display colours indicating Suclasses.
- Examples of habitat types covered include woodland (broadleaved, coniferous, mixed with yew), arable and horticulture, improved grassland, neutral/calcareous/acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, standing water and rivers, inland rock, built-up areas, supralittoral and littoral zones, and oceanic/seas categories.

## Spatial Coverage and Scale
- Total area for LCM2000 across the UK: 246,688 km² (UK LCM2000 total).
- Regional breakdowns (LCM2000 totals): England ~130,362 km²; Wales ~20,689 km²; Scotland ~77,898 km²; Northern Ireland ~17,739 km².
- Combined UK total for LCM2000 (England & Wales): 151,051 km²; UK total with all regions: 246,688 km².
- Table 5 presents per-habitat and per-subclass coverage (km²) from LCM2000 and from field survey (FS) for each region and the UK overall.
- FS totals are provided for many categories but are not consistently available (UK FS total listed as not available in the table).

## Validation with Field Survey (FS)
- Table 6 compares LCM2000 cover (uncalibrated) with FS estimates (Low/High) for major habitat categories, across England, Wales, Scotland, and GB, with 95% confidence.
- Examples of GB FS ranges (compared to LCM2000 figures):
  - Broadleaved/mixed/yew woodland: LCM2000 = 15,259 km²; FS Low = 12,750; FS High = 16,670.
  - Coniferous woodland: LCM2000 = 12,879 km²; FS Low = 10,672; FS High = 16,808.
  - Arable and horticulture: LCM2000 = 56,638 km²; FS Low = 47,944; FS High = 57,036.
  - Improved grassland: LCM2000 = 50,024 km²; FS Low = 50,536; FS High = 59,104.
  - Neutral grassland: LCM2000 = 10,770 km²; FS Low = 5,046; FS High = 7,214.
  - Calcareous grassland: LCM2000 = 10,647 km²; FS Low = 72; FS High = 1,228.
  - Acid grassland: LCM2000 = 14,483 km²; FS Low = 10,594; FS High = 15,306.
  - Bracken: LCM2000 = 1,892 km²; FS Low = 3,258; FS High = 5,522.
  - Fen/marsh/swamp: LCM2000 = 197 km²; FS Low = 4,138; FS High = 6,802.
  - Bog: LCM2000 = 5,134 km²; FS Low = 18,696; FS High = 25,664.
- The FS comparisons reveal substantial variability and indicate uncertainties between the LCM2000 calibration and field-derived estimates, highlighting the importance of documenting uncertainties and calibration status.

## Cross-Table Correspondences and Validation Insights
- Summary correspondence matrices (Tables 8–10) quantify how LCM2000 corresponds to the CS2000 field survey across various levels:
  - Per 1000 correspondences for Broad Habitats, Target Class, and Aggregate class levels.
  - Analyses cover Great Britain, England & Wales, and Scotland, with bootstrap-based confidence intervals.
- Notes indicate generalisation of urban areas and urban landscapes in some correspondences, and that results are weighted estimates using stratified bootstrapping (40 Land Classes).
- Tables illustrate where LCM2000 aligns well with field survey classifications and where discrepancies arise, aiding data stewards in communicating limitations to users.

## Implications for Data Stewardship and Metadata
- Data quality and provenance
  - LCM2000 data are uncalibrated with FS comparisons available, necessitating clear metadata on calibration status and known biases.
  - Differences between LCM2000 and FS should be documented, with rationale and notes on coastal variability and intertidal area inclusion/exclusion.
- Metadata and data lineage
  - Include fields for: LCM2000 Target Class, Subclass, Variant; region; area_km2 (LCM2000 and FS where available); FS Low/High; calibration status; confidence intervals; notes on coastal intertidal treatment; urban/generalisation flags.
  - Capture crosswalks to CS2000 and any other reference classifications used (e.g., notes in footnotes about mapping correspondences).
- data governance and maintenance
  - Track versioning of classification schemes (LCM2000 vs CS2000) and any future updates; document update cadence and data provenance.
  - Ensure users understand the areas where FS validation is available and where it is not; provide guidance on interpreting 95% confidence ranges.
- Discovery and accessibility
  - Provide clear documentation of table structures, units (km²), region definitions, and the meaning of Target Class/Subclass/Variant mappings.
  - Highlight coastal variability caveats and the potential need for region-specific interpretation when using the data for planning or ecological analyses.
- Usability and transparency
  - Include summaries of validation outcomes (e.g., general trends of agreement/disagreement across habitat types) to inform data users about reliability.
  - Offer guidance on appropriate use cases (e.g., large-scale planning, habitat distribution analyses) and cautions for fine-grained or intertidal zone work.

## Particular Challenges for Data Stewards
- Incomplete picture of user needs and priorities (aligning classification detail with user requirements).
- Timeliness and completeness of data intake from data creators/sharers, especially for complex coastal/intertidal areas.
- Managing multiple systems and formats, including non-interoperable variants and intertidal classifications.
- Handling large and heterogeneous datasets with diverse metadata requirements.
- Keeping up-to-date with outdated databases and ensuring robust crosswalks and interoperability with current standards.

## Endnotes
- Coastal coverage is variable due to tidal states and differences in inclusion/exclusion of offshore intertidal areas.
- Differences between LCM2000 and FS statistics are discussed in the text, with footnotes providing clarifications on definitions and scope.
- The document emphasizes the need for careful interpretation of habitat area data, particularly where validation data are sparse or where coastal and urban/generalization factors influence classification.