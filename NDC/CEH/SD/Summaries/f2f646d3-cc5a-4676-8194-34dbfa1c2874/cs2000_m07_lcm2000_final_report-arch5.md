# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

- Purpose and scope
  - Provides a crosswalk between Broad Habitats (BHs) and the LCM2000 classification scheme, linking LCM Target Class, Subclasses, and Variants (with Suclasses shown by map colours).
  - Establishes how 22 broad habitats map onto LCM2000 categories to support integration, comparison, and reporting across datasets.

- Data content and structure
  - Crosswalk details for each BH, listing:
    - LCM Target Class
    - LCM Subclass
    - LCM Variants
    - Suclasses (represented by colours on maps)
  - Table 5 offers the coverage (in km2) of each LCM2000 Subclass and aggregated classes (bold) across the UK and constituent countries.
  - Table 6, Table 9, Table 10 present summary correspondence matrices (results per 1000) comparing LCM2000 with the CS2000 field survey:
    - Weighted estimates
    - Strata based on 40 Land Classes
    - Bootstrapped confidence intervals
  - Table 8, Table 9, Table 10 include generalised urban considerations, Target Class mappings, and Aggregate class level mappings to support interoperability and error assessment.

- Data provenance and methods
  - LCM2000 statistics are derived from a full count of cover on a 25 m grid.
  - FS (field survey) statistics are from Haines-Young et al. 2000.
  - Differences between LCM2000 and FS statistics are discussed in the text (footnotes reference where discrepancies arise).
  - Coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas.
  - Total coverage and counts differ by definitional scope of the FS population (e.g., Northern Ireland exclusions).

- Coverage and scope details
  - Table 5 provides UK-wide totals by habitat type (e.g., broad-leaved/mixed woodland, coniferous woodland, arable crops, improved grassland, neutral/calcareous/acid grasslands, bracken, bog, fen/marsh/swamp, standing water, built-up areas, etc.) and by country (England, Wales, Scotland, NI) with UK totals.
  - Includes both Target Class and finer-grained Subclasses/Variants, enabling both high-level summaries and detailed breakdowns.
  - Tables 6–10 present correspondences and cross-walks across multiple classification schemes (LCM2000, CS2000) and geographies (GB, England & Wales, Scotland, UK).

- Data quality, limitations, and caveats
  - Some cells contain n/a values or undefined/ambiguous entries reflecting gaps in data, alignment issues, or differences in classification application.
  Notable caveats:
  - Differences between LCM2000 and FS statistics require careful interpretation; explicit explanations are provided in the text.
  Coastal and urban generalisation uncertainties are acknowledged, particularly where urban areas or maritime zones affect classification counts.
  - Some NI data are incomplete or excluded from certain survey tallies.

- Governance and data stewardship implications
  - The document offers a rigorous crosswalk that supports dataset integration, discovery, and reuse by aligning habitat classifications across schemes.
  - Important metadata considerations:
    - Classification schema (LCM2000 Target Class, Subclass, Variant; CS2000 equivalents)
    - Spatial resolution and grid (25 m vs field survey units)
    - Geographic scope and any exclusions (e.g., NI exclusions)
    - Data sources (LCM2000 counts, FS, Haines-Young et al. 2000)
    - Calibration status and notes on differences between sources
  - Quality control needs:
    - Maintaining the crosswalk as a data dictionary
    - Documenting caveats and footnotes for end users
    - Recording uncertainty (bootstrapped CIs, per tables)
  - Data sharing and interoperability:
    - Ensure consistent application of the crosswalk across platforms and studies
    - Preserve provenance and versioning when updates to LCM2000/CS2000 schemes occur
    - Include urban-generalisation considerations in metadata where relevant

- Practical takeaways for data stewards
  - Use the BH-to-LCM2000 crosswalk as a reference for harmonising habitat data across datasets.
  - Preserve all provenance details, including grid size, time frame, and source documents (LCM2000 full-count grid, CS2000 field survey, Haines-Young et al. 2000).
  - Clearly document uncertainties, n/a entries, and the reasons for any data gaps or exclusions.
  - Maintain a robust data dictionary and crosswalk mappings to facilitate discovery, reuse, and accurate integration with CS2000 and related datasets.
  - Be mindful of coastal and urban generalisation issues when aggregating or comparing results across datasets or geographies.