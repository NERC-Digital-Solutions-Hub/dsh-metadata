# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

- Purpose and scope
  - Documents the mapping between LCM2000 data categories (Target class, Subclasses, Variants) and Broad Habitats (BHs) used in CS2000 field surveys.
  - Illustrates how habitats are represented in map displays and how they relate to LCM2000 classifications across England, Wales, Scotland, and Northern Ireland.

- How to read the mappings
  - Each row pairs an LCM2000 Target class with its Subclasses and Variants, showing how a given habitat is encoded in the LCM2000 schema and how it appears in map displays.

- Key habitat groups included
  - Broad-leaved woodland and mixed woodlands
  - Coniferous woodland
  - Arable and horticultural areas
  - Improved grassland, neutral/calcareous/acid grasslands
  - Bracken, dwarf shrub heath, and other heath/montane habitats
  - Fen, marsh, swamp, bog
  - Inland bare ground and various rock/shore habitats
  - Built-up areas, suburban/urban, and coastal/ supralittoral habitats
  - Supralittoral rock and sediment, littoral rock and sediment, and oceanic/seas categories

- Data tables referenced for GIS use
  - Table 5: Coverage (km2) of Subclasses from LCM2000 and of Aggregate classes (bold) from LCM2000 and field survey (FS) across the UK and constituent countries.
  - Table 6: LCM2000 cover (uncalibrated) for BHs by country, compared with FS field-survey estimates at 95% confidence (Low/High ranges).
  - Table 8: Summary correspondence matrix (results per 1000) comparing LCM2000 with CS2000 field survey squares in Great Britain; includes weighting by strata (40 Land Classes) and bootstrapped confidence intervals; results shown for Broad Habitats and various aggregation levels.
  - Table 9: Summary correspondence matrix (England & Wales) similarly structured to Table 8.
  - Table 10: Summary cross-tabulations for Scotland, with analogous formatting.
  - Footnotes: Metadata and methodological notes about scaling (per 1000 vs per 1000), bootstrapping, grid resolution (25 m LCM2000; 1 km FS references), and definitions of urban/generalisation implications.

- Geographic and total-scale highlights
  - Table 5 provides country-level and UK-wide totals for numerous habitat classes (e.g., broad-leaved/mixed woodland, coniferous woodland, arable/horticultural classes, improved grassland, neutral/calcareous/acid grasslands, bracken, peat/bogs, fen/marsh/swamp, built-up areas, coastal and marine-adjacent classes).
  - UK totals (LCM2000) for broad categories are presented (e.g., total woodland, arable/horticultural, improved grassland, neutral/calcareous/acid grasslands, urban built-up areas, coastal/marine interfaces), with FS totals provided where available.
  - Table 6 gives UK-wide LCM2000 cover for BHs and FS estimates with 95% CI; notable example: Broadleaved/mixed/yew woodland LCM2000 UK = 15,259; FS Low = 12,750; FS High = 16,670.
  - Tables 8–10 provide cross-walks of how often LCM2000 corresponded to CS2000 habitat classes per 1000, including urban generalisation effects and various aggregation levels, with country-specific breakdowns (England, Wales, Scotland, NI, GB).

- Data quality, calibration and caveats
  - LCM2000 is uncalibrated against CS2000 FS in Table 6; FS provides field-survey estimates with confidence intervals.
  - Differences between LCM2000 and FS are discussed in accompanying text and footnotes; coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas.
  - Total coverage varies with the FS population definition (1 km squares); in Northern Ireland some BHs may be excluded from survey.
  - Methodology notes: statistics based on a full count of cover on a 25 m grid (LCM2000); FS statistics follow Haines-Young et al. 2000; bootstrapping and weighting used to generate confidence intervals for cross-walks.

- GIS workflow implications
  - Use the 3-tier structure (Target class, Subclass, Variant) to design map symbology and interactive layers, while understanding how these align with CS2000 field data.
  - Leverage Table 5 to assess land-cover area distributions by habitat type and by country for aggregation and reporting.
  - Use Table 6 as a starting point for calibration against field-survey data and to quantify uncertainty in repertoire of habitat classes.
  - Apply Tables 8–10 cross-walks to translate between LCM2000 classes and CS2000 field categories when validating, harmonising, or merging datasets.
  - Be mindful of urban generalisation effects in cross-class comparisons and incorporate bootstrapped confidence intervals to communicate uncertainty in map-based products.

- Endnotes and limitations to consider
  - Footnotes explain differences between LCM2000 and FS data, coastal variability, and definitions affecting totals.
  - Results are presented as weighted estimates; some cells are not available (n/a) or are context-specific (e.g., UK vs country-level totals).
  - The crosswalks are modelled relationships based on 40 Land Classes and bootstrapped confidence measures; habitats with sparse field data may have higher uncertainty.

- Takeaway for map-making and analysis
  - The document provides a comprehensive crosswalk between LCM2000 map-based habitat classifications and CS2000 field-survey classes, with quantitative coverage by habitat type and country, plus calibrated-style correspondences and uncertainty measures that are essential for accurate GIS-based analysis, reporting, and decision support.