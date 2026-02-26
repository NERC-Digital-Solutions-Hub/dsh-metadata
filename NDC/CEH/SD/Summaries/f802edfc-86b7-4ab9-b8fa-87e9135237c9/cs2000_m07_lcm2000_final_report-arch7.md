# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

## Overview and purpose
- Presents a mapping between Broad Habitats (BHs) and the LCM2000 framework: Target Class, Subclasses, and Variants.
- Indicates how BHs are displayed in map colours and how variants relate to the overall classification.
- Supports GIS work by enabling map-based representation of habitat types across the UK.
- Notes that LCM2000 statistics use a 25 m grid; CS2000 field survey statistics (FS) are referenced from Haines-Young et al. 2000 and related sources.
- Highlights that coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas; NI data may exclude some BHs.

## Data structure and classification
- BHs are linked to LCM2000 at three levels:
  - Target Class
  - Subclass
  - Variant (displayed with map colours)
- Table entries show the many-to-one relationships between BHs and LCM2000 classes, including cross-references to variants such as broad vegetation types, arable categories, and natural features (e.g., broad-leaved/wet/dry woodland, arable crops, various water/peat/grassland types).
- The structure is designed to support GIS symbology and querying by BH category and by LCM2000 level.

## Coverage by country (LCM2000 vs field survey context)
- Table 5 provides the broad-area cover (km²) for BHs by country and aggregated UK totals:
  - England: LCM2000 total ~130,362 km²
  - Wales: LCM2000 total ~20,689 km²
  - Scotland: LCM2000 total ~77,898 km²
  - Northern Ireland: LCM2000 total ~17,739 km²
  - UK total (LCM2000): ~246,688 km²
- FS (field survey) coverage is reported where available (e.g., England & Wales FS total ~142,355; Scotland FS ~78,730; NI FS not always available). FS totals differ from LCM2000 totals due to definitions and sampling.
- The tables show numerous country- and BH-specific comparisons (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/Acid grasses, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing open water, Built-up/urban areas, etc.).

## Calibrated comparisons and uncertainty (LCM2000 vs FS)
- Table 6 compares uncalibrated LCM2000 cover with FS estimates at 95% confidence (low/high bounds) for Great Britain (England, Wales, Scotland) and Northern Ireland:
  - Example GB values (illustrative): 
    - Broadleaved/mixed/yew woodland: LCM2000 ~15,259 km²; FS Low ~12,750; FS High ~16,670
    - Coniferous woodland: LCM2000 ~12,879; FS Low ~10,672; FS High ~16,808
    - Arable and horticulture: LCM2000 ~56,638; FS Low ~47,944; FS High ~57,036
    - Improved grassland: LCM2000 ~50,024; FS Low ~33,314; FS High ~39,946
  - Across other BHs, FS estimates often fall within or near the FS confidence intervals, but there are notable deviations for several classes and countries.
- Footnotes emphasize that NI data may exclude some BHs, and total coverage varies with definitions; FS statistics reflect field survey conventions and bootstrapped confidence intervals.

## Correspondence between LCM2000 and CS2000 field survey (summary matrices)
- Tables 8–10 present summary correspondence matrices (results per 1000 or percent) comparing LCM2000 with CS2000 field survey squares in GB, England & Wales, and Scotland:
  - These matrices show how often LCM2000 Target Classes and Aggregates align with CS2000 categories, and how urban generalisation affects correspondences.
  - The results indicate variable correspondence rates across Broad Habitats, with some categories aligning better than others and notable effects when urban/generalisation adjustments are applied.
  - The matrices include cross-references to:
    - Boundary/linear features
    - Arable & horticulture
    - Improved grassland
    - Neutral, Calcareous, and Acid grasslands
    - Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog
    - Standing open water and rivers/streams, Montane habitats, Inland rock, Built-up areas and gardens, Supralittoral and Littoral components, Oceanic/Seas classifications
- Footnotes explain multiple crosswalks and mappings (e.g., CS2000 sub-categories to CS2000 labels), and generalisation of urban areas.

## Practical implications for GIS specialists
- Data integration:
  - When combining LCM2000 map products with CS2000 field data, expect partial alignment; use the summary correspondences to guide legend design and class reconciliation.
  - Be mindful of the 25 m LCM grid vs field survey units; apply appropriate aggregation or downscaling as required for map displays.
- Classification and symbology:
  - Use the BH-to-LCM2000 mappings to ensure consistent map symbology; variants are shown in map colours and should be treated as sub-classes within the main BH display.
  - For cross-border analyses (England, Wales, Scotland, NI), apply country-specific FS considerations and NI data caveats.
- Uncertainty and calibration:
  - FS confidence intervals (Table 6) provide a basis for uncertainty visualization; consider creating uncertainty rasters or confidence-aware maps where needed.
  - Recognise that coastal/BH extents vary with tidal states; ensure coastal classifications are clearly documented in map metadata.
- Quality assurance:
  - Expect ongoing data-cleaning and transformation needs to harmonise different resolutions and standards across datasets.
  - Early prototyping and user feedback are important to refine map-based data products for different audiences (policy colleagues, clients, public).

## Key takeaways for GIS use
- LCM2000 provides a comprehensive, map-ready framework linking broad habitats to target classes, with detailed subclass/variant relationships suitable for map displays.
- When comparing LCM2000 to CS2000 field data, there are notable differences by habitat type and country; credible interpretation requires considering 95% confidence intervals and country-specific caveats.
- Summary correspondence matrices reveal how well LCM2000 aligns with CS2000 categories and how urban generalisation affects the match; use these insights to inform data integration, legend design, and spatial analyses.